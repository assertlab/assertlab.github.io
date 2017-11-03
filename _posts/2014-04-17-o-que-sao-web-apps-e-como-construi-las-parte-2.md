---
layout: post
title: "O que são Web Apps e como construí-las. (parte 2)"
categories: Pesquisa
tag: mestrado
---

_By By Misael Neto in [Hyper Reactive](http://hyperreactive.com/){:target="_blank"}_

No post anterior falamos a respeito de Web Apps e suas características básicas. Também falamos de algumas das vantagens em se adotar um modelo de Single-page application para desenvolver esse tipo de aplicação. Hoje falaremos sobre as dificuldades que podem aparecer ao se adotar esse paradigma e como contorná-las. Para isso criaremos uma aplicação que ficará hospedada nesse endereço: <http://case.hyperreactive.com>. O código fonte ficará aqui <https://github.com/misawsneto/hyperreactive>.

Eu escolhi um framework para desenvolvimento de aplicações web chamado [Play!](https://www.playframework.com/){:target="_blank"}. É um framework Java/Scala bastante fácil de aprender, manipular, implantar (fazer deploy). Esse framework é mantido pelo pessoal do Typesafe, os mesmos caras por trás da linguagem de programação Scala e do middleware orientado a eventos chamado [Akka](https://akka.io/){:target="_blank"} (mais sobre programação orientada a eventos [aqui](http://hyperreactive.com/2013/12/o-que-e-event-driven-architecture-e-o-modelo-de-atores-de-hewitt/){:target="_blank"}).

Bom, um dos problemas que emergem quando se constrói uma Single-page application utilizando a técnica citada no post anterior tem a ver com o endereçamento das páginas. A principal função dos browsers é apresentar o conteúdo retornado quando se faz uma requisição HTTP do tipo GET para a url definida na barra de endereços. Outra função fundamental do browser é manter um histórico de navegação e permitir que o usuário navegue entre as páginas deste histórico. Um browser não é um browser se não executar essas tarefas. Uma vez que uma Web App controla a navegação entre as páginas por meio de Ajax ela também deve controlar o histórico de navegação. Pense bem, o método descrito no post anterior injeta páginas dentro de uma div, mas até onde o browser consegue perceber, não há mudança de páginas (o endereço não muda).

> <http://hyperreactive.com/2014/04/o-que-sao-web-apps-e-como-construi-las-parte-2/>