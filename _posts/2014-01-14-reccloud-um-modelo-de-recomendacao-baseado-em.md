---
layout: post
title: "RecCloud: Um Modelo de Recomendação Baseado em Nuvem"
categories: Pesquisa
tag: mestrado
---

Há mais informação no mundo do que a nossa capacidade, humana, de processá-la [2]. Vivemos numa era de efervescência informacional, a cada dia se produz mais&nbsp;informação e, geralmente, estas informações são armazenadas em meios digitais. O tamanho desse “_universo digital_" cresce de forma exponencial. Segundo relatório publicado pela EMC Corporation [1], em 2005, o volume de dados chegou a 130 exabytes; em 2010, superou 1 zettabyte e a previsão é que em 2015 chegue a quase 8 zettabytes, conforme mostrado na Figura abaixo.

![]({{ BASE_PATH }}/images/2014-01-14-reccloud-um-modelo-de-recomendacao-baseado-em/figura1.png)

Este “_universo digital_” citado em Gantz e Reinsel [1] expande e se torna cada vez mais complexo a tarefa de filtragem de conteúdo e busca por conteúdo relevante que atenda as preferências do usuário. Parte deste “_universo digital_” está sendo armazenado em ambientes de armazenamento em nuvem, ocasionando a criação de grandes massas de dados nesses sistemas. As massas de dados geradas se tornaram humanisticamente impossíveis de serem processadas. Este cenário é contrário à demanda tecnológica do século XXI, que é encontrar e extrair informações em tempo hábil no meio dessa quantidade de informações, uma opção que atende a este questionamento são os sistemas de recomendação.

Ao analisar a literatura e os sistemas de armazenamento em nuvem mais populares e utilizados atualmente, observamos que, no geral esses sistemas não fornecem ao usuário o serviço de recomendação de arquivos. Na maioria dos sistemas de armazenamento em nuvem, a filtragem de conteúdo é realizada por sistemas de busca, onde o usuário fornece termos chaves e o sistema retorna arquivos similares aos termos apresentados pelo usuário. Por outro lado, a enorme quantidade de sistemas de recomendação que rodam em nuvem, não utilizam características da nuvem na geração de suas recomendações. Esses sistemas normalmente têm como objetivo recomendar itens que atendam as preferências dos usuários, sem considerar requisitos do ambiente.

Neste trabalho investigamos a utilização de características da nuvem que possam ser usadas no processo de recomendação de arquivos em ambiente de armazenamento em nuvem. Com o aumento substancial da utilização de ambientes de armazenamento em nuvem, o nosso objetivo é que esse novo modelo tire proveito das vantagens oferecidas pela utilização de ambientes de armazenamento em nuvem, auxiliando o usuário na filtragem de conteúdo que atenda suas preferências, e amenizar o tempo gasto nesta tarefa e no download de arquivos recomendados.

O modelo de recomendação modelado neste trabalho é formado pela técnica de recomendação baseada em conteúdo, combinado a características da nuvem. O modelo de recomendação proposto é composto por cinco fatores, os fatores que serão utilizados no processo de recomendação, são oriundos da nuvem, e de metadados dos arquivos armazenados em nuvem. Os fatores propostos foram definidos a partir da observação de ambientes de armazenamento em nuvem e quais as prioridades de usuários nesses ambientes. Os fatores são:

* Similaridade
* Disponibilidade
* Taxa de Download
* Tamanho do arquivo
* Relevância do arquivo

Na Figura 2, apresentamos o processo de recomendação completo do modelo RecCloud.

![]({{ BASE_PATH }}/images/2014-01-14-reccloud-um-modelo-de-recomendacao-baseado-em/figura2.png)

Na Figura 2, o usuário elicita suas preferências através do “_Arquivo Y_”, em seguida o SR calcula a recomendação. A partir do cálculo de cada fator, é gerada a recomendação ao usuário, o arquivo “_X_”, que estava disponível na nuvem é recomendado ao usuário. 

Esta pesquisa encontra-se em processo de avaliação. Para avaliação do modelo proposto serão utilizadas 5 (cinco) métricas, definidas a partir da análise da literatura. As métricas escolhidas são:

**Precisão**: Proporção entre o número de arquivos relevantes recomendados e o número total de arquivos recomendados.

**Recall**: Proporção entre o número de arquivos recomendados e o número de arquivos relevantes utilizados na avaliação.

**F-Measure**: Média harmônica ponderada da precisão e recall.

**Tempo gasto no download**: Tempo gasto para realizar o download de um arquivo recomendado.

**Avaliação do conteúdo recomendado**: Avaliação do conteúdo recomendado em relação às preferências do solicitante.

Referências

1. Gantz, J. and Reinsel, D. (2011). Extracting value from chaos state of the universe: An executive summary. 1-12.
2. Lopes, A. R. S. (2012). Sistemas de Recomendação Utilizando Similaridade Globais para Aliviar o Problema da Esparcidade. Dissertação de Mestrado, Universidade Federal de Pernambuco (UFPE).

Texto escrito por _Ricardo Batista Rodrigues_ (rbr at cin.ufpe.br)