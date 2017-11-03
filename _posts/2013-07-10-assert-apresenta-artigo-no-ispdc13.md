---
layout: post
title: "ASSERT apresenta artigo no ISPDC’13"
categories: Artigos
tag: conferencia
---

Entre os dias 27 e 30 de junho o estudante de doutorado Francisco Airton participou do [12th International Symposium on Parallel and Distributed Computing – ISPDC 2013](http://ispdc.hpc.pub.ro/) na cidade de Bucareste na Romênia. O evento ;(patrocinado pela IEEE) é classificado como Qualis B2 de acordo com a CAPES, e na ocasião representando os autores Francisco Airton, Paulo Silveira, Vinicius Garcia, Fernando Trinta e Rodrigo Assad, apresentou o trabalho entitulado “_Monext: An Accounting Framework for Infrastructure Clouds_” que é parte dos resultados do seu mestrado.

Este trabalho é financiado pelo ;Centro de Pesquisa e Desenvolvimento em Tecnologias Digitais para Informação e Comunicação (CTIC) do Ministério de Ciência e Tecnologia do Brasil (MCT), processo número 68/2011. Adicionalmente, este trabalho é apoiado pelo [Instituto Nacional de Ciência e Tecnologia (INCT) para Engenharia de Software (INES)](http://www.ines.org.br/), financiado pelo CNPq e FACEPE, processos número 573964/2008-4 and APQ-1037-1.03/08.

O evento é bem multidisciplinar e abordou temas relacionados à computação distribuída e paralela no tocante a seis trilhas:

1.  Task Scheduling and Load Balancing
2.  Performance Management in Parallel and Distributed Systems
3.  Cloud and Mobile Computing
4.  Distributed Software Components
5.  Collaborative Computing
6.  Parallel Programming

Francisco apresentou o framework Monext na trilha “Task Scheduling and Load Balancing”. Essa ferramenta visa realizar tarifação de IaaS em nuvens privadas ou públicas aplicando políticas próprias fazendo uso de uma linguagem específica de domínio. Para saber mais sobre o trabalho acesse a [página da ferramenta](http://cin.ufpe.br/~faps/monext/). Na ocasição a platéia se interessou mais pela DSL indagando sobre a sua extensibilidade.

![image](https://github.com/assertlab/assertlab.github.io/blob/master/_posts/2013-07-10-assert-apresenta-artigo-no-ispdc13/foto1.jpg?raw=true)

Na trilha "Cloud and Mobile Computing" o professor pesquisador Dan Grigoras da universidade de Bucareste apresentou o estado da arte e futuras direções em Mobile Cloud (linha de pesquisa na qual Francisco visa seguir atualmente) e defendeu a ideia de que todas as técnicas de evolução de aplicações mobile que interagem com nuvens devem tentar ser direcionadas à melhoria da experiência do usuário, delimitando métricas que transpareçam a satisfação do mesmo. Esta apresentação foi de suma importância para Francisco, pois pôde discutir posteriormente com Grigoras possíveis facetas de pesquisa a serem exploradas. Neste ambiente, Francisco também conheceu de perto o trabalho em Mobile Cloud realizado por Alexandru Olteanu, estudante PhD em fase final de trabalho em que como pesquisador desenvolve estudos na subárea denominada offloading de aplicações e como professor aplica uma metodologia de ensino de programação através da construção de apps mobile. Na foto abaixo, um grupo de alunos de graduação que estavam participando de um escola de verão em mobile programming na semana da conferência.

![image](https://github.com/assertlab/assertlab.github.io/blob/master/_posts/2013-07-10-assert-apresenta-artigo-no-ispdc13/foto2.jpg?raw=true)

Dentre as keynotes, duas chamaram mais a atenção por correlação ao trabalho de Francisco, a primeira ministrada por Iosif Legrand por incluir mecanismos de monitoramento de infraestrutura e a segunda de Thilo Kielmann por ter uma certa relação com o projeto [JiTCloud](http://jitclouds.lsd.ufcg.edu.br/site/index.php/en/) (no qual teve construção participativa do grupo ASSERT).

Iosif Legrand é um engenheiro pesquisador no Instituto de Tecnologia da Califórnia desde 1998, trabalhou muitos anos envolvendo física e energia nuclear, sendo que atualmente coordena uma série de projetos de software em computação distribuída. No ISPDC Iosif apresentou um keynote entitulado "Monitoring and Control of Large Scale Distributed Systems" onde ele chama de [MonALISA ](http://monalisa.caltech.edu/monalisa.htm) um framework que fornece um sistema de serviço distribuído capaz de controlar e otimizar aplicações de larga escala e dados intensivos. Seu campo inicial de atuação são os sistemas de rede, suporte de processamento e análise de dados. A estratégia do trabalho dele é tentar satisfazer as demandas de aplicações de uso intensivo de dados tornando mais sinérgicas as interações entre os aplicativos, computação, armazenamento e infra-estrutura de rede.

Thilo Kielmann é um professor de computação na universidade de Amsterdam na Holanda. Ele investiga sistemas de larga escala focando em clusters, clouds e grids. No ISPDC ele falou sobre um trabalho mais relacionado ao o que Francisco trabalhou no mestrado que é tarifação, porém focando em custo. Kielmann apresentou o keynote entitulado "Cost-efficient Task Farming with ConPaaS". [ConPaas](http://www.conpaas.eu/) permite aos usuários executar "sacos de tarefas" (Bags of Tasks) de acordo com um orçamento definido pelo usuário. Usando uma amostra de tarefas, ConPaas estima os custos para executá-las em diferentes ofertas de nuvem (provedores). O serviço oferece ao usuário uma escolha de opções antes da execução e agenda horários para isto de acordo com as preferências do usuário. O serviço não exige a priori informações sobre o tempo de conclusão da tarefa. Este trabalho open-source se mostrou bastante maduro e pode ser usado tanto na Amazon EC2 quanto no OpenNebula atualmente. Foi notado que pode-se fazer uma relação do ConPass com o trabalho JiTCloud uma vez que o objetivo de ambos é trabalhar com bags of tasks de forma elástica, no entanto o ConPaaS apenas dá um direcionamento de onde e quando executar limitado a algumas nuvens e o JiTCloud é uma nuvem por si só que procura executar estas tarefas em nuvens privadas (a princípio).