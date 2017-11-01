---
layout: post
title: "Algoritmos de detecção de resistência a drogas do HIV e porquê devemos otimizá-los"
categories: Pesquisa
tag: doutorado
---

A manipulação de dados biomoleculares pode apresentar características tratadas em computação como problemas de Big Data. Estes, são comumente armazenados em grandes bases de dados estruturadas ou não, apresentam certo grau de complexidade e as técnicas tradicionais de gerenciamento e processamento desses dados podem não ser muito úteis. Sobretudo para os casos em que existem inconsistências e a possibilidade de combinações imprevisíveis.

Segundo Prajapati (2013), a caracterização enquanto Big Data vem dos requisitos de volume, velocidade e variedade. Essas características são encontradas na interpretação de resistência a drogas do Vírus da Imunodeficiência Humana (HIV).

Existem diversos algoritmos que se propõem a fazer essa interpretação de resistência a drogas para o HIV. O [HIValg](https://hivdb.stanford.edu/hivalg/by-sequences/){:target="_blank"}, mantido pela Universidade de Stanford, permite que sequencias de código genético viral sejam avaliadas quanto a resistência a drogas pelos algoritmos HIVdb (da própria Standford), Rega e ANRS. Essa análise é feita a partir da manipulação de uma sequência de 9181 caracteres que é cortada e comparada com milhares de sequências de mesmo tamanho presentes nas bases de dados desses algoritmos.

Partimos da premissa de que a performance desses algoritmos é satisfatória para a análise de apenas uma sequência genética por vez. No entanto, o mesmo não acontece de forma escalável para a análise de várias sequências ao mesmo tempo devido à natureza de alto consumo de recursos computacionais da realização de operações com grandes cadeias de caracteres e dado o contínuo aumento dessas bases de dados com de códigos genéticos do HIV.

O objetivo de nossa pesquisa é otimizar o tempo e o consumo de recursos computacionais do algoritmo de interpretação de resistência a drogas Rega, utilizando técnicas de manipulação e gerenciamento de Big Data. Considerando como recursos computacionais a o consumo de tempo de processamento e memória RAM, observando para que não haja prejuízo da corretude das análises.

Os benefício dessa otimização é uma provável redução de tempo e custo para a realização de pesquisas científicas sobre a resistência a drogas do HIV. Essa resistência tem aumentado o número de mortes por AIDS em 14% para pacientes em tratamento. O índice de resistência às drogas utilizadas como terapia inicial tem sido de 9% na Polônia (Parczewski, 2014), 11.7% na França (Frange, 2015), de até 64% na Libéria (Loubet, 2015) e de 35% do Brasil (De Souza, 2015).

Um provável caminho para se chegar a esta otimização é a utilização de tecnologias como o Apache Hadoop, que é um framework para pesquisa e processamento de Big Data em clusters de servidores. A segunda versão deste framework deixa o gerenciamento de recursos e o apontamento de responsabilidades para ferramentas como YARN e Mesos. Outra ferramenta útil a este contexto é o Spark, que provê um engine de execução para o processamento de grandes quantidades de dados manipulados em memória de forma paralela utilizando diversas linguagens de programação.

**Referências**

* De Souza Cavalcanti, J., Ferreira, J. L. D. P., Guimaraes, P. M. D. S., Vidal, J. E., & Brigido, L. F. D. M. (2015). High frequency of dolutegravir resistance in patients failing a raltegravir-containing salvage regimen. Journal of Antimicrobial Chemotherapy, 70(3), 926–929. <http://doi.org/10.1093/jac/dku439>
* Frange, P., 1, 2, * L. A., 3, Descamps, D., 4, 5, … Wirden, M. (2015). HIV-1 subtype B-infected MSM may have driven the spread of transmitted resistant strains in France in 2007– 12: impact on susceptibility to first-line strategies ´, (February), 2084–2089. <http://doi.org/10.1093/jac/dkv049>
* Loubet, P., Charpentier, C., Visseaux, B., Borbor, a., Nuta, C., Adu, E., … Descamps, D. (2015). Prevalence of HIV-1 drug resistance among patients failing first-line ART in Monrovia, Liberia: a cross-sectional study. Journal of Antimicrobial Chemotherapy, (February), 1881–1884. <http://doi.org/10.1093/jac/dkv030>
* Parczewski, M., Leszczyszyn-Pynka, M., Witak-J dra, M., Maciejewska, K., Rymer, W., Szymczak, a., … Urba ska, a. (2014). Transmitted HIV drug resistance in antiretroviral-treatment-naive patients from Poland differs by transmission category and subtype. Journal of Antimicrobial Chemotherapy, 70(1), 233–242. <http://doi.org/10.1093/jac/dku372>
* Prajapati, V. (2013). Big data analytics with R and Hadoop. Packt Publishing Ltd.