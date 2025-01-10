[⬅️ Voltar para o README](../README.md)

# Serviço de Banco de Dados MySQL na Nuvem

As duas principais características definidoras do Serviço de Banco de Dados MySQL na Nuvem são o recurso de **alta disponibilidade**, que você deve definitivamente usar em produção, e o **HeatWave**, que permite realizar transações OLAP e OLTP usando o Serviço de Banco de Dados MySQL na Nuvem.

## Alta Disponibilidade

A alta disponibilidade basicamente oferece tolerância a falhas. Ela traz muitos benefícios, como failover automático, aumento de tempo de atividade e zero perda de dados.

Com a opção de instância única, você tem um sistema de banco de dados MySQL único, respaldado pelo volume de bloco resiliente e seguro do OCI. Esta opção é boa para ambientes de desenvolvimento e testes. No entanto, se você estiver rodando em produção, realmente vale a pena optar pela opção de alta disponibilidade. Essa opção permite que os aplicativos atendam a requisitos mais altos de tempo de atividade e tolerância a perda de dados zero.

Ao selecionar a opção de alta disponibilidade, um sistema de banco de dados MySQL com **três instâncias** é provisionado em diferentes domínios de disponibilidade ou diferentes domínios de falha. Os dados são replicados entre as instâncias.

## HeatWave

HeatWave é um novo acelerador de consulta de alto desempenho integrado em memória para o Serviço de Banco de Dados MySQL, que acelera o desempenho do MySQL em uma ordem de magnitude para consultas analíticas e transacionais. O HeatWave escala para milhares de núcleos.

O Serviço de Banco de Dados MySQL com HeatWave é o único serviço disponível no mercado que permite aos administradores de banco de dados e desenvolvedores de aplicativos executar cargas de trabalho OLTP e OLAP diretamente de seu banco de dados MySQL. Isso elimina a necessidade de movimentação de dados complexa, demorada e cara, além da integração com um banco de dados de análises separado. Este serviço é otimizado e disponível exclusivamente na Oracle Cloud Infrastructure.

O MySQL HeatWave usa um mecanismo de **armazenamento de dados em memória** para fornecer execução de consultas de alto desempenho. Isso é alcançado armazenando os dados em um formato colunar na memória, o que permite acesso e processamento mais rápidos dos dados durante a execução das consultas, especialmente para cargas de trabalho OLAP.

O MySQL HeatWave é um acelerador de consulta integrado para o serviço de Banco de Dados MySQL na Oracle Cloud Infrastructure. Ele aumenta significativamente o desempenho do MySQL, permitindo que ele execute de maneira eficiente consultas OLAP (Processamento Analítico Online), que são consultas complexas que analisam grandes volumes de dados para descobrir insights de negócios.

![MySQL HeatWave](../images/heatwave.png)