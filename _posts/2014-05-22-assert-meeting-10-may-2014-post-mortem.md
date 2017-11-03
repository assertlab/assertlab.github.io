---
layout: post
title: "ASSERT Meeting (10-May-2014) Post Mortem"
categories: Pesquisa
tag: seminario
---

No último sábado, 10/05/2014, ocorreu no [**Centro de Informática**](http://www.cin.ufpe.br){:target="_blank"} da UFPE o primeiro de uma série de seminários sobre os projetos que estão sendo desenvolvidos pelos membros do ASSERT Lab.
Inaugurando a série, o Doutorando Kellyton Brito apresentou o status do seu trabalho, discutindo as publicações recentes [1][2][3] e apresentando a previsão das próximas etapas de sua pesquisa.
Os slides usados na apresentação podem ser consultados em <http://pt.slideshare.net/kellytonbrito/assert-workshop-dados-abertos>.

Após a apresentação, houve uma rica discussão envolvendo os presentes, aos quais o autor agradece a presença e as contribuições.

Em seguida, o mestrando Saulo Medeiros de Araujo apresentou o estado atual de sua pesquisa, orientada pelo professor Silvio Meira, mas que também conta com valiosas contribuições dos professores Kiev Gama e Nelson Rosa. A pesquisa parte da premissa de que o desempenho de sistemas intensivos em E/S pode ser aumentado significativamente explorando-se as oportunidades que estes sistemas costumam oferecer para a execução concorrente de operações de E/S. Apesar deste enorme potencial, operações de E/S são executadas concorrentemente apenas em sistemas altamente especializados, tais como aqueles que efetuam computações científicas. Isto acontece porque programar a execução concorrente de operações de E/S a partir dos mecanismos mais difundidos para tal (primitivas síncronas de E/S com programação multithreaded e primitivas assíncronas) é significativamente mais difícil do que programar a execução sequencial destas operações.

O primeiro resultado obtido pela pesquisa é um framework para a linguagem Java chamado Afluentes (disponível em <https://github.com/afluentes>), que permite ao programador coordenar a execução tanto de métodos síncronos quanto a de métodos assíncronos através da composição de métodos, facilitando o desenvolvimento de sistemas que executam operações de E/S concorrentemente.

Afluentes foi avaliado através de experimentos realizados em um sistema web que interage com um banco de dados relacional. Nestes experimentos, o tempo gasto pelo sistema para responder a uma requisição foi mensurado com o sistema submetendo consultas ao banco de dados sequencialmente e também concorrentemente. Os resultados obtidos são animadores, mostrando que, de fato, a execução concorrente de operações de E/S aumenta significativamente o desempenho de sistemas intensivos em E/S.

Ao final da apresentação, o público teceu críticas e sugestões ao estado atual da pesquisa, contribuindo para delinear seus próximos passos.

Mais informações podem ser obtidas em [4] e os slides da apresentação estão disponíveis em: <http://www.slideshare.net/saulomaraujo/afluentes-concurrent-io-made-easy-with-lazy-evaluation>.

1. Experiences Integrating Heterogeneous Government Open Data Sources to Deliver Services and Promote Transparency in Brazil. Artigo aceito para publicação na 38ª Annual International Computers, software & Applications Conference Special Sessions 2014 (COMPSAC), em Västerås, Sweden 21–25 Jul, 2014;
2. Using Parliament Brazilian Open Data to Improve Transparency and Public Participation in Brazil. Artigo aceito para publicação na International Digital Government Research Conference (2014), em Aguascalientes City - Mexico, 18–21 Jun, 2014;
3. Brazilian Government Open Data: Implementation, Challenges, and Potential Opportunities. Artigo também aceito para publicação na International Digital Government Research Conference (2014), em Aguascalientes City - Mexico, 18–21 Jun, 2014;
4. Araujo, Saulo Medeiros de, Kiev Santos da Gama, Nelson Souto Rosa, and Silvio Lemos Meira. “Afluentes Concurrent I/O Made Easy with Lazy Evaluation.” In Parallel, Distributed and Network-Based Processing (PDP), 2014 22nd Euromicro International Conference on, pp. 279-287. IEEE, 2014.