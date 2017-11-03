---
layout: post
title: "Uma abordagem para o balanceamento de carga de servidores de busca em sistemas de armazenamento de dados P2P JXTA"
categories: Pesquisa
tag: doutorado
---

antes de iniciarmos a principal discussão que motiva este blog, precisamos entender quais as tecnologias, componentes e coisas que apoiarão este trabalho. o primeiro deles inicia-se com algo não tão novo conhecido como [redes peer-to-peer (p2p)](http://bit.ly/1bGQGDD){:target="_blank"} e outras coisas mais…

napster, kazaa, torrent, gnutella, … todos possuem um modelo de comunicação em comum, alguns totalmente puros e outros nem tanto [hibridos], alguns se deram bem por um tempo, outros, continuam até hoje em pleno funcionamento.

para se criar estas redes no braço, existem frameworks que abstraem a implementação baixo nível, conhecidos como p2p overlay networks. em java, no início do milênio, foi criado um desses de nome jxta, sob a orientação de dois caras: [bill jow e mark clark](http://bit.ly/1awHQJ1){:target="_blank"}. outros frameworks para desenvolver aplicações em redes de p2p e um comparativo sob as duas categorias: estruturadas e não-estruturadas podem ser vistas [aqui](http://bit.ly/1iDsFWC){:target="_blank"}.

então o objetivo inicial deste blog é apresentar uma proposta onde por meio da utilização de computadores conectados, sem um servidor, em um modelo totalmente descentralizado, seja possível doar espaço ocioso para alguém armazenar arquivos. até agora isso não é novidade alguma, tem gente que doa o tempo ocioso do seu computador para curar doenças, estudar o aquecimento global, o caso do [BOINC](http://bit.ly/1iDrMgB){:target="_blank"}.

o nome desta proposta: an architectural proposal for a decentralized p2p cloud storage framework. ok, mas existem diversas empresas vendendo este produto: [cloud storage](http://bit.ly/KqZ58I){:target="_blank"}, aqui tem as 10 melhores, mas, quem garante que seus dados estão seguros lá?

[vale lembrar que](http://bit.ly/1hofqZs){:target="_blank"} você pode não ser o dono dos seus dados, mesmo que você cancele o serviço. caiu na net!!! pra finalizar, tem uns caras há algum tempo [fazendo p2p cloud storage](http://bit.ly/1exRAFU){:target="_blank"}, uns tempos atrás no modelo p2p, depois, em modo mais centralizado. por que eles desistiram da primeira opção, vamos verificar mais lá na frente.

fora eles, [quem brinca com essa abordagem hoje](http://bit.ly/19V9QsN){:target="_blank"}, p2p híbrido, com alta disponibilidade e baixo consumo de recursos. isso foi o esquente...

Texto escrito por [Anderson Fonseca e Silva](https://andersonfonseka.blogspot.com.br/){:target="_blank"}.