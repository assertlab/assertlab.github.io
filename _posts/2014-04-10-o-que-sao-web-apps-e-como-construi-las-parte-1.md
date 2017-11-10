---
layout: post
title: "O que são Web Apps e como construí-las. (parte 1)"
categories: Pesquisa
tag: mestrado
---

_By By Misael Neto in [Hyper Reactive](http://hyperreactive.com/){:target="_blank"}_

Eu tenho visto cada vez mais Aplicações Web com características de softwares Desktop. A internet das páginas estáticas já se foi há muito tempo. Recentemente esbarrei em um “novo” padrão de desenvolvimento web chamado Web Components. Eu não fazia ideia do que se tratava e resolvi pesquisar…. vejam [aqui](https://www.youtube.com/watch?v=fqULJBBEVQE){:target="_blank"} e [aqui também](https://css-tricks.com/modular-future-web-components/){:target="_blank"}. Padrões como Web Componentes e bibliotecas javascript como [embem.js](https://emberjs.com/){:target="_blank"}, [angular.js](https://angularjs.org/){:target="_blank"}, [react](https://reactjs.org/){:target="_blank"} tem se tornado bastante populares e fazem parte de um conjunto de ferramentas de vanguarda que facilitam o processo de criação de Web Apps. Mas o que são Web Apps (ou o que não são)?

Web App é um termo genérico que representa uma grande variedade de sistemas. _Tweetdeck_, [Gmail Web](https://mail.google.com/){:target="_blank"}, [Trello](https://trello.com/){:target="_blank"} e outros podem ser considerados Web Apps. Neste post vamos definir Web Apps como sendo softwares que são executados e apresentados em browsers e restringir o escopo de estudo sobre Web Apps a partir de uma característica fundamental: [Single-page application](https://en.wikipedia.org/wiki/Single-page_application){:target="_blank"}. Estudo? Sim! Fui aceito no mestrado em Engenharia de Software pela Universidade Federal de Pernambuco. Nos próximos meses (6 ~ 8) a maioria dos posts (não todos) deste blog serão relacionados a construção de sistemas web, arquitetura de software orientada a eventos, sistemas tempo real... Mas voltando ao que importa;

Single-page applications são sites, sistemas, aplicações que possuem apenas uma página. Esse tipo de aplicação utiliza AJAX (_asynchronous javascript and xml_) para alterar , dinamicamente, o conteúdode uma página. _That’s old news_... A dificuldade está em construir TODA uma aplicação utilizando essa mecânica de modo que, uma vez carregada a página inicial, toda a navegação subsequente (mudança de páginas, carregamento de conteúdo, absolutamente) utilize um processo de carregamento assíncrono das páginas. Difícil de entender? Vou explicar melhor… imagine que um sistema de cadastro de estoque qualquer possua 5 páginas: página principal, edição de perfil de usuário, cadastro de produtos, listagem de todos os produtos e detalhamento do produto. Não é difícil imaginar que cada uma dessas páginas é bem distinta das outras. Uma vez que as páginas são diferentes umas das outras, qual é a melhor forma de arquitetar esse sistema de estoque utilizando o paradigma de Single-page layout? Uma maneira é fazer com que cada página seja injetada (via ajax) dentro de um elemento DIV. Por exemplo:

![]({{ BASE_PATH }}/images/2014-04-10-o-que-sao-web-apps-e-como-construi-las-parte-1/codigo1.png)

O código acima contém uma div com id=”content-wrapper”. Nosso objetivo é fazer com que todas as páginas sejam carregadas, de maneira dinâmica (via ajax), dentro dessa div. Para isso, precisamos modificar o comportamento dos links que levam a outras páginas. Por exemplo:

![]({{ BASE_PATH }}/images/2014-04-10-o-que-sao-web-apps-e-como-construi-las-parte-1/codigo2.png)

O que o código acima faz é modificar o comportamento dos links cuja classe é ajaxlink. Estou utilizando a biblioteca JQuery para associar uma função anônima ao evento de clique de botão: `$(‘body’).on(‘click’, ‘a.ajaxlink’, function(e)`. Quando um link como este...

![]({{ BASE_PATH }}/images/2014-04-10-o-que-sao-web-apps-e-como-construi-las-parte-1/codigo3.png)

...for clicado, o função anônima acima será executado. A primeira instrução é armazenar a url contida no link em uma variável chamada url. Em seguida, faz-se uma requisição ajax para resgatar a página em questão usando o método `$.ajax()`. Um dos parâmetros passados para o método $.ajax() é justamente a url do link clicado. Os outros parâmetros são o tipo da requisição, neste caso GET e também a função a ser executada caso a requisição ao servidor seja bem sucedida. Quando o servidor responder a requisição, o método success será executado e a página será injetada dentro da div. Por fim a função anônima retorna o valor false indicando que o comportamento padrão de clique no link não seja disparado (o browser não fará o processo natural de navegação, isso fica a cargo de nossa função anônima). Existem alguns benefícios em adotar essa abordagem:

1. Os arquivos `javascript` e `css` só precisam ser carregados uma úinica vez. Tudo bem, tudo bem, é possível utilizar mecanismos de cache para evitar que o browser faça diversas transferências com o servidor. Porém, como cada página geralmente possui arquivos `.js` e .`css` próprios, o usuário ainda terá que esperar um primeiro carregamento das páginas. Esse fato combinado ao tempo de recarregamento de página transmite uma experiência de navegação ruim para o usuário.
2. O browser só precisa carregar a página uma única vez. Na verdade, não é bem assim. Mas o usuário tem a percepção de que é. Isso porque, uma vez que a página principal e todos os arquivos javascript e css são carregados, não há necessidade de recarregamento da página como um todo. Isso permite que o programador controle a experiência de transição de páginas, por exemplo, esmaecendo a página durante o processo de transição para a página seguinte ( `.fadeIn() & .fadeOut()` do JQuery) ao invés da transição nada agradável que browsers fornecem.

É possível realizar tarefas ainda mais complexas. Vejam este [post](https://signalvnoise.com/posts/3697-server-generated-javascript-responses){:target="_blank"} do pessoal do **37signals**. Não entrarei em detalhes, mas recomendo a leitura.

Ao utilizar uma navegação do tipo _Single-page_ deve-se carregar apenas os recursos apropriados para a injeção dos elementos em questão. Logo, para cada requisição assíncrona (ajax) o servidor deve retornar apenas o bloco de código HTML necessário para exibição do conteúdo em questão. Os _“imports”_ `javascript`, css já foram carregados assim como os elementos `html`, `head`, `body`...

O próximo post falará mais a respeito de _Single-page Applications_ e as dificuldades que emergem quando se tenta implementar esse paradigma.

Mais informações: <http://hyperreactive.com/>