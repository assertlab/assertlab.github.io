---
layout: post
title: "Introdução ao desenvolvimento de Máquinas Sociais hiper-escaláveis"
categories: Mestrado
---

A evolução atual da máquina de turing e sua complexidade são incentivadas por desafios que confrontam os ambientes computacionais. Dentre os inúmeros fatores, temos mudança de requisitos dos usuários (pessoas que usavam PCs preferem a mobilidade de  smartphones), as leis de Moore [1] e Amdahl [2] que desafiam o desenvolvimento de algorítmos, a falta de viabilidade financeira, falta de maturidade de modelos e processos, ou o crescimento instantâneo e exponencial de serviços (spikes).

Big Players como Google, Netflix, Amazon.com ou Twitter têm se encontrado em um mundo único de inovações devido a singularidade de seus cenários alavancados por um dos maiores desafios da computação: o crescimento.

Seja devido ao sucesso de um serviço homogêneo disponibilizado através de plataformas como Twitter e Netflix, a expansão global de lojas virtuais como a Amazon.com ou o crescimento rápido de empresas de apostas como a Paddy Power com turnover de 6 Billhões de euros por volta de 2015,  a resposta para o fator crescimento o é desenvolver sistemas distribuídos escaláveis [3].

Escalabilidade é a capacidade que um sistema tem de adicionar mais recursos a fim de atender a necessidade de uma carga de trabalho maior [4]. Além disso, é preciso que tais sistemas apresentem respostas adequadas à solicitações on-demand. Portanto, que também sejam elásticos. Nossa pesquisa visa diretamente lidar com sistemas distribuídos que adotam alta escalabilidade e elasticidade como propriedades fundamentais em sua composição.

Inicialmente, entendemos que para construir tais sistemas é necessária a definição de um elemento básico de software que possa ser adicionado ou removido do ambiente a fim de possibilitar alta escalabilidade e eslasticidade ao sistema. Para representar tal elemento utilizamos o conceito de máquinas sociais devido a seu foco no inter-relacionamento entre os elementos que compõem uma arquitetura [5].

Também, entendemos que o elemento básico dessa arquitetura (a máquina social) deve ser delimitado pelo dominio real do problema. Exemplificando, teríamos uma máquina social A responsável pelo departamento de CDs e outra máquinas social B responsável pelo departamento de livros. Partindo da premissa que ha apenas essas 2 instâncias heterogêneas ativas no ambiente, caso a quantidade de trabalho aumentasse além da capacidade da máquinas social A (CDs), bastaria inserir uma nova instância no sistema [7].

Acerca de sistemas distribuídos monolíticos já existentes, estamos trabalhando no desenvolvimento de uma melhor estratégia para o desmembramento dos “domínios reais” existentes e transformando-os em máquinas sociais. Atualmente estamos usando uma solução opensource a fim de validar o conceito através de um problema real.

Até o momento esse estudo visa contribuir com o desenvolvimento de novas tecnologias e simplificar o desenvolvimento de aplicações distribuídas escaláveis através da definição de conceitos, estratégias, e uma arquitetura hiper-escalável.

1. Green, C.; The end of Moore’s Law? Why the theory that computer processors will double in power every two years may be becoming obsolete. URL:  <http://www.independent.co.uk/life-style/gadgets-and-tech/news/the-end-of-moores-law-why-the-theory-that-computer-processors-will-double-in-power-every-two-years-10394659.html>
2. Herlihy, Maurice and Shavit, Nir; The art of multiprocessor programming. Elsiever 2008
3. Vogels, Werner. A Conversation with Werner Vogels. ACM QEUE 2006.
4. Lins, Helaine S. Análise da Completude dos Relatos de Experimentos em Elasticidade na Computação em Nuvem: Um Mapeamento Sistemático. Dissertação de mestrado, UFPE 2015.
5. Buregio, V. The Emerging Web of Social Machines. <http://vanilson.com/2013/03/10/142/>.
6. Wikipedia. Monolithic system. <https://en.wikipedia.org/wiki/Monolithic_system>
7. ABBOTT, ML; FISHER, M.T. THE ART OF SCALABILITY: Scalable Web Architecture, Processes, and Organizations for the Modern Enterprise