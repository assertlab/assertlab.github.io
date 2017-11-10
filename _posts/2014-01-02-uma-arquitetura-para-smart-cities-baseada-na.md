---
layout: post
title: "Uma arquitetura para Smart Cities baseada na Internet of things"
categories: Pesquisa
tag: mestrado
---

De acordo com relatório divulgado pela UNESCO [Nations, U. (2007)], por volta de 1950, 30% da população mundial vivia em áreas urbanas e em 2010 esta porcentagem subiu para 50%. Estima-se que em 2050 a porcentagem de pessoas vivendo nos grandes centros urbanos será de 70%. Além disso, 10% da população mundial vive nas 30 principais metrópoles [Dobbs, R. and Institute, M. G. (2011)]. No cenário nacional, segundo a pesquisa realizada pelo Instituto Brasileiro de Geografia e Estatística (IBGE), publicada no [Diário Oficial da União](http://saladeimprensa.ibge.gov.br/noticias?view=noticia%5C&amp;idnoticia=2204), em julho de 2012 o Brasil chegou a 193.946.886 habitantes, que representa um aumento de aproximadamente 1,65% em relação ao ano de 2010.

Este crescimento populacional é natural, pois é justamente nas cidades onde há mais oportunidades econômicas.&nbsp; Este fato tem originado grandes desafios para os gestores das cidades. Problemas relacionados ao tráfego, segurança, consumo de água e energia, dentre outros, têm sido cada vez mais difíceis de serem administrados.

Dessa forma, o conceito de Cidades Inteligentes (CI) surge a partir da necessidade de combinar Tecnologia da Informação e Comunicação (TIC) com esses aspectos operacionais das cidades [Li, X., Lu, R., Liang, X., Shen, X., Chen, J., and Lin, X. (2011)] visando otimizar a qualidade de vida dos cidadãos. Apesar dessa necessidade, não há um consenso a respeito da definição deste conceito, nem quanto ao ambiente mais adequado para empregá-lo.

Existem algumas iniciativas isoladas que visam tratar alguma defâsagem urbana. As iniciativas vão de aplicativos como [Waze](https://www.waze.com/), um serviço que mistura geolocalização no celular com indicações do fluxo e problemas de trânsito via smartphones, até governamentais, como [Centro de Operações da prefeitura do Rio de Janeiro](http://www.rio.rj.gov.br/web/corio), que integra órgãos que produzem informações úteis sobre a cidade.

Porém, estas iniciativas podem ser consideradas apenas o começo da implementação de uma CI. Além disso, para de fato estabelecer uma SC é necessário que estas iniciativas estejam integradas em um mesmo ambiente, seja compartilhando informações ou até mesmo para facilitar a definição da estratégia de atuação.

Neste contexto, surge a necessidade de uma arquitetura capaz de integrar os recursos de uma cidade. Nesse sentido, um recurso pode ser qualquer objeto distribuído em uma rede, constituindo a Internet das Coisas (IoT). Um exemplo destes recursos são os fornecedores de dados, como um ônibus, perfil de uma rede social, smartphone ou até mesmo outro sistema. Esta arquitetura deve permitir que os dados desses recursos fossem combinados de forma a obter uma informação mais completa sobre determinado evento na cidade.

Para a concepção da proposta deste trabalho, foram realizadas duas revisões da literatura: Revisão Sistemática e Revisão Exploratória. Esta duas revisões foram necessárias devido ao contexto de mercado que envolve as duas grandes áreas de pesquisa: Cidades Inteligentes e Internet das Coisas. 

A partir destas revisões, um conjunto de requisitos que uma arquitetura para Cidades Inteligentes deve atender. A Tabela 1 apresenta estes requisitos.

![image]({{ BASE_PATH }}/images/2014-01-02-uma-arquitetura-para-smart-cities-baseada-na/tabela1.png)

Ao analisar esta tabela, percebe-se que a Revisão Exploratória foi mais eficaz. Porém, devido à falta de um processo formal que possa ser repetido, este fato não deve ser considerado que as Revisões Exploratórias são mais eficientes que as Revisões Sistemáticas.

A partir destes requisitos, a proposta deste trabalho foi definida, exemplificada na Figura 1.

![image]({{ BASE_PATH }}/images/2014-01-02-uma-arquitetura-para-smart-cities-baseada-na/figura1.png)

Após o estabelecimento da proposta, foi necessário avaliá-la. Para tal, vários métodos de avaliação disponíveis na arquitetura foram estudados, porém nenhum deles atendia o contexto deste trabalho. Logo, foi realizada a adaptação de dois métodos amplamente utilizados na liteturatura (SAAM e ATAM) para ser executado remotamente.

Inicialmente uma equipe totalmente multidisciplinar de 16 pessoas foi construída. Em seguida, esta equipe realizou três reuniões remotas na qual cada etapa do método de avaliação foi executada, que incluiu a proposta de cenários de utilização da arquitetura e avaliação da adequação destes cenários.

A Figura 2&nbsp;apresenta o resultado da adequação de cada cenário, de acordo com a visão da equpe de avaliação. Nesta figura, os cenários mais prioritários estão organizados da esquerda para direita (C1 até C14).

![image]({{ BASE_PATH }}/images/2014-01-02-uma-arquitetura-para-smart-cities-baseada-na/figura2.png)

Conforme se pode notar, na opinião dos participantes, a arquitetura atendente de forma EXCELENTE três cenários. O primeiro cenário (C2) é relacionado aos mecanismos de distribuição de dados implementados no MGDD , principalmente a utilização da _DHT_ de dados. Já o segundo cenário (C4) foi obtido a partir da implementação do padrão _publisher-subscriber_ também no MGDD. Por fim, o último cenário avaliado positivamente é oriundo do modelo de abstração e da flexibilidade implementada no MAC.

Já a maioria dos cenários foi considerada SATISFATÓRIO, pelos participantes da avaliação. Este resultado indica que a arquitetura, em uma primeira instância, atende a um conjunto de contextos de utilização. Por outro lado, este resultado também indica que a arquitetura deve ser aprimorada para atender de forma segura e eficiente os demais contextos.

Além disso, dois cenários foram classificados como PÉSSIMO. O primeiro (C9) está relacionado à inserção de algum mecanismo de tolerância a falhas. O outro cenário (C14) corresponde às políticas de privacidade de dados utilizadas pela arquitetura. De fato, estes dois cenários não foram previstos inicialmente. No caso do cenário C9, não foi encontrado nenhum mecanismo semelhante nas abordagens encontradas na literatura. Por fim, como a arquitetura proposta mostrou-se modular, para trabalhos futuros serão incluídos dois componentes para mitigar essas deficiências.

De uma forma geral, estes resultados mostram que a arquitetura pode e deve ser utilizada em um contexto real, para, de fato, verificar a adequação da arquitetura ao contexto de Cidades Inteligentes e Internet das Coisas.

A Tabela 2 resume os próximos passos deste trabalho.

![image]({{ BASE_PATH }}/images/2014-01-02-uma-arquitetura-para-smart-cities-baseada-na/tabela2.png)

**Referências**:
Nations, U. (2007). World population prospects: The 2006 revision and world urbanization prospects. Technical report, United Nations, New York.
Dobbs, R. and Institute, M. G. (2011). Urban World: Mapping the Economic Power of Cities. McKinsey Global Institute.
Li, X., Lu, R., Liang, X., Shen, X., Chen, J., and Lin, X. (2011). Smart community: an internet of things application. IEEE Communications Magazine, 49(11), 68–75.

Post originalmente publicado por [Gustavo Henrique Rodrigues Pinto Tomas](http://www.gustahrodrigues.com/)