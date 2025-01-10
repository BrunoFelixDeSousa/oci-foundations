# Oracle Container Engine for Kubernetes (OKE)

VMs:
- Maior utilização dos recursos subjacentes
- Maior espaço em disco
- Maior tempo de inicialização

Containers:
- Tempo de inicialização mais rápido
- Leves
- **Portáteis** (principal razão)

![Diferenças entre VMs e Containers](../images/vms_vs_containers.png)

## Orquestração de Containers

**Docker** é usado para gerenciar e criar os containers.

**Kubernetes** é um sistema open-source para automatizar a implantação, escalonamento e gerenciamento de aplicativos conteinerizados.

Quais são algumas das vantagens?

1. Você pode executar aplicativos conteinerizados de **qualquer escala** sem tempo de inatividade.
2. Você pode **auto-recuperar** aplicativos, proporcionando resiliência.
3. Você pode **auto-escalar** aplicativos conteinerizados, garantindo a utilização ideal.
4. **Simplifica significativamente a implantação** em grande escala.

## OKE

**OKE** é um serviço Kubernetes totalmente gerenciado, escalável e altamente disponível. Ele é baseado no sistema open-source Kubernetes. Possui muitos recursos para desenvolvedores, como criação de clusters com um clique, suporte a API CLI e suporte para execução em instâncias baseadas em ARM e GPU.

![Componentes de um Cluster](../images/oke.png)

Ao criar um novo cluster com o OKE, você pode especificar o tipo de cluster a ser criado. Existem dois tipos de clusters:
1. **Clusters aprimorados**: eles oferecem todos os recursos disponíveis e vêm com um SLA financeiro respaldado.
2. **Clusters básicos**: eles oferecem funcionalidades essenciais, mas sem os recursos aprimorados. Eles têm um Objetivo de Nível de Serviço (SLO) financeiro, mas não um SLA respaldado financeiramente como o cluster aprimorado.

Ao criar um pool de nós para o seu cluster Kubernetes, você também tem duas opções:

1. Criar um **nó virtual**: o software Kubernetes é atualizado, os patches de segurança são aplicados respeitando os requisitos de disponibilidade de aplicativos, mas isso é feito pela Oracle. Você só pode criar nós virtuais e pools de nós virtuais em clusters aprimorados.
2. Criar um **nó gerenciado**: você é responsável por gerenciar os nós, atualizar o Kubernetes nos nós gerenciados e gerenciar a capacidade do cluster. Ao contrário dos nós virtuais, você também pode criar nós gerenciados em clusters básicos, bem como em clusters aprimorados.

![Tipos de nós de cluster](../images/cluster_nodes.png)