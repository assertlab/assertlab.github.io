---
layout: post
title: "Defesa de Dissertação de Mestrado Nº 1.309"
categories: Defesa
tag: mestrado
---

## Pós-Graduação em Ciência da Computação – UFPE

### Defesa de Dissertação de Mestrado Nº 1.309

* Aluno: Paulo Fernando Almeida Soares
* Orientador: Prof. Silvio Romero de Lemos Meira
* Co-orientador: Prof. Vinicius Cardoso Garcia
* Título: Dedupeer: Deduplicação de Arquivos Através de um Algoritmo de Processamento Particionado
* Data: 27/08/2013
* Hora/Local: 15:00h à Auditório

Banca Examinadora:

* Prof. Vinicius Cardoso Garcia ( CIn / UFPE)
* Prof. Manoel Gomes de Mendonça Neto (Departamento de Ciência da Computação/ UFBA)
* Prof. Rodrigo Elia Assad (Departamento de Estatística e Informática / UFRPE)

RESUMO:

_A deduplicação é uma técnica de compressão de dados sem perda que elimina dados redundantes tanto intra-file como inter-file, diferente de ferramentas de compressão de dados como o gzip que só eliminam a redundância intra-file. A deduplicação reduz a necessidade de armazenamento através da eliminação de blocos de dados redundantes._

_Na deduplicação, todos os blocos de dados que estão duplicados em um sistema de armazenamento podem ser reduzidos à uma única cópia, esses blocos desalocados pela deduplicação são transformados em referência para o que foi mantido no sistema._

_Técnicas de deduplicação começaram a ser estudadas para sistemas de armazenamento comerciais em meados de 2004. Hoje, os principais sistemas de armazenamento de dados usam deduplicação, mas os algoritmos implementados e as técnicas utilizadas_

_não são detalhadas publicamente. Existem alguns trabalhos acadêmicos focados na implementação de algoritmos de deduplicação, mas eles são raros e não são voltados para a sua utilização em sistemas de armazenamento existentes. O principal objetivo deste trabalho é criar um algoritmo para deduplicação de arquivos no cliente de forma remota, através de processamento particionado e utilizando comparação por fingerprints. Este algoritmo foi incorporado em um componente de software com interface interoperável para facilitar a utilização em qualquer sistema de armazenamento de dados e beneficiá-los com economia de armazenamento, e na transferência de dados no caso dos sistemas de armazenamento distribuídos._

_Além do componente de software, foi desenvolvido também um sistema de armazenamento com gerenciamento de dados baseado no Apache Cassandra, o que o torna capaz de ser distribuído, com o objetivo de validar o algoritmo de deduplicação. A integração do componente de software com o sistema de armazenamento foi implementada e avaliada neste trabalho._

Palavras-chave: Deduplicação, compressão de dados, economia de armazenamento, sistemas de armazenamento de dados