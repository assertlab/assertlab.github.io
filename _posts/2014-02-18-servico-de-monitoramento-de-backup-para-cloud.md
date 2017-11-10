---
layout: post
title: "Serviço de monitoramento de backup para Cloud Storage em uma arquitetura P2P"
categories: Pesquisa
tag: mestrado
---

O aumento da quantidade de dados produzida pelos usuários domésticos através da popularização de dispositivos de produção de conteúdo desafia as empresas de TI a disponibilizarem e gerirem esses dados de forma ubíqua. Nesse contexto, surgi os sistemas de armazenamento de dados em nuvem (cloud storage). Dentre o sistemas mais conhecidos neste modelo podemos citar Amazon S3[1], AllMyData[2] e Rackspace[3].

Visando garantir transparência e qualidade do serviço fornecido ao usuário é necessário à definição de uma SLA (Service Level Agreements). SLA é um acordo entre o serviço web fornecedor e serviço web usuário que especifica o nível garantido de qualidade de serviço e as propriedades funcionais de um serviço web. Devido a natureza dinâmica da cloud, o monitoramento continuo dos atributos de Qualidade de Serviço (QoS) é necessário para a implementação de SLAs. Portanto para acompanhamento e cumprimento do acordo, são definidos estratégias de monitoramento dos recursos utilizados. Este trabalho trata exatamente de monitorar alguns atributos responsáveis por definir um mínimo de qualidade no serviço de backup, estes são: o tempo do backup, tamanho do arquivo e quantidade de peers que este arquivo esta sendo replicado.

Além disso, o agente de monitoramento desenvolvido deverá seguir algumas premissas básicas: pouco invasivo, para que não dependa de código interno da aplicação cliente; rápida, para que o usuário não sofra com longas esperas de processamento; poucas mensagens enviadas, as mensagens devem ser as mais compactas possíveis, para que não sobrecarregue o trafego de rede; o mais genérico possível, para que possa ser utilizado em outras cloud storage; e canal de envio de mensagens assíncrono, para não precisar aguardar de respostas sobre envio de mensagem.

Como pode ser visto na arquitetura da Figura 1 o agente é outro componente externo a aplicação cliente, esta o notificando sempre quando a aplicação estiver inativa, para que, desta forma, o agente possa fazer a leitura dos dados que constam no log, mapeá-los e enviar para a fila de mensagem. Enquanto isso, o Administrator fica aguardando a chegada das novas mensagens para consumi-las, tratar os dados e salva-los no banco de dados e, posteriormente, os gráficos serem gerados.

![]({{ BASE_PATH }}/images/2014-02-18-servico-de-monitoramento-de-backup-para-cloud/figura1.png)

O usuário ao utilizar a aplicação cliente e realizar backup, todos os dados de cada backup estarão sendo inseridos no arquivo de log, sendo todos capturados a partir de algumas variáveis definidas no inicio do método run e capturados mais tarde os valores no final do método depois de ter decorrido o backup, por exemplo, o tempo de inicio e fim que são capturados de acordo o horário do sistema. Depois disso, e de todos os dados capturados, foi utilizado o padrão de projeto observer para quando o usuário finalizar a aplicação cliente, o modulo do agente ser notificado e disparar, em seguida, um chamada ao método run, que lerá o log, mapeando-o para um objeto BackupData que será enviado via mensagem para a fila do ActiveMQ. A aplicação de administração utilizando a classe ListenerBackupData, na qual foi sobrescrito o método onMessage, “escuta” a fila de mensagem, para que quando chegue uma nova, ele possa recebê-la automaticamente. Este método pega os dados da mensagem e insere no banco de dados, para mais tarde ser útil como um histórico para um administrador do sistema e gerar os gráficos demonstrando o comportamento do backup de acordo com a velocidade para cada quantidade de peers utilizados. Como pode ser visto na Figura 2.

![]({{ BASE_PATH }}/images/2014-02-18-servico-de-monitoramento-de-backup-para-cloud/figura2.png)

Desta forma, o agente de monitoramento demonstrou ser capaz de medir e analisar os atributos de desempenho da funcionalidade do backup. Entretanto, garantir somente o backup na aplicação de cloud storage não é o suficiente para assegurar a qualidade do sistema. Além desta, é necessário outros parâmetros como melhor localização dos dados, recuperação dos dados, escalabilidade, segurança e rendimento do sistema [4].

Referências

1. DECANDIA G., HASTORUN D., JAMPANI M., KAKULAPATI G., LAKSHMAN A., PILCHIN A., SIVASUBRAMANIAN S., VOSSHALL P. and VOGELS W.; Dynamo: Amazon’s Highly Available Key-value Store, Amazon.com 2011
2. rackspace. URL: <http://www.rackspacecloud.com/tools/category/applications/cloud-filespartners/filesystems/>. Último acesso em 18/12/2012
3. Nimbus is cloud computing for science. URL: http://www.nimbusproject.org/. Último acesso em 20/12/2010.
4. Mohammed Alhamad, Tharam Dillon, Elizabeth Chang.Conceptual SLA framework for Cloud Computing.4th IEEE International Conference on Digital Ecosystems and Technologies. 2010, pp: 606-610.

Texto escrito por: Saulo de Tarso Oliveira da Silva (stos “at” cin “dot” ufpe “dot” br)