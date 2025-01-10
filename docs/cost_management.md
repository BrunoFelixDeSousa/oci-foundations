# Gerenciamento de Custos

A OCI oferece diferentes ferramentas para gerenciar custos.

A primeira ferramenta são os **Orçamentos OCI**. Você pode usar orçamentos para acompanhar os custos na sua tenancy. Após criar um orçamento para um compartimento, você pode configurar alertas que irão notificá-lo se o orçamento estiver previsto para ser excedido ou se o gasto ultrapassar um valor específico.

A segunda ferramenta é a **Análise de Custos**. Você pode analisar seus custos após tê-los gasto, mas é uma boa maneira de olhar para os custos passados e fazer mudanças para o futuro. Se houver elementos que você deseja mudar, essa é uma ótima maneira de fazer isso.

Também existem **Relatórios de Uso**. Atualmente, os Relatórios de Uso são baixados na forma desses arquivos CSV, e são gerados diariamente. Eles mostram os dados de uso para cada recurso na sua tenancy. Os arquivos CSV são armazenados em um bucket de armazenamento de objetos acessível usando uma política de cross-tenancy, para que você possa olhar não apenas para a sua tenancy, mas também para várias tenancies, caso múltiplas tenancies estejam sendo usadas.

Há também **Limites de Serviço**, a ferramenta para definir seus limites, cotas e uso. Assim como em qualquer nuvem, a OCI limita quantos recursos você pode executar em uma tenancy tradicional para evitar problemas como fraudes e abusos. Se você estiver usando compartimentos, tem a capacidade de configurar **Cotas de Compartimento**.

## Notas

Na Oracle Cloud Infrastructure, você pode configurar alertas por e-mail para receber notificações quando os limites do orçamento forem atingidos. Esses alertas ajudam os clientes a se manterem informados sobre seus gastos e a tomarem ações adequadas para gerenciar seus custos.

Os limites de serviço são os limites máximos definidos pela Oracle para o número de recursos que você pode criar em uma região ou tenancy, enquanto as cotas de compartimento são os limites máximos definidos pelos usuários para o uso de recursos dentro de compartimentos específicos. A diferença é que os limites de serviço são definidos pela Oracle e se aplicam a uma tenancy em uma região, enquanto as cotas de compartimento são definidas pelos usuários e se aplicam a compartimentos específicos.