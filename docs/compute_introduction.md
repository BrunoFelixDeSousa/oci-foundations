# Introdução ao Compute

O serviço **OCI Compute** oferece:
- Máquinas virtuais
- Servidores bare metal (servidor completo dedicado a você)
- Hosts dedicados (uma máquina bare metal onde você pode rodar VMs)

As três características definidoras desse serviço incluem:
- **Escalabilidade**
- **Alto desempenho**
- **Preços mais baixos**

## Shapes Flexíveis

**Shapes flexíveis** significa que você tem flexibilidade para escolher a configuração que deseja.

Você pode escolher:
- **Oracle Cloud Processor Units (OCPUs)**
- **Memória**

**Nota**: O número de NICs virtuais e físicas não são parâmetros personalizáveis para instâncias de compute com shapes flexíveis.

Na nuvem, existe o conceito de **T-shirt sizing**, ou tamanhos de camisas, onde você tem formas pequenas, médias e grandes, e seu aplicativo precisa se ajustar a essas formas. Às vezes, você acaba superdimensionando ou subdimensionando, e precisa passar pelo processo doloroso de mudar o tipo da sua máquina. Com shapes flexíveis, você não precisa fazer isso.

## Qual é a diferença entre Dedicated Host e VMs?

As **VMs** são compartilhadas e multi-tenant, o que significa que o host pode estar rodando VMs de vários clientes. Já alguns clientes preferem um **dedicated host**, onde podem rodar suas próprias VMs, sem VMs de outros clientes sendo executadas ali.

## Opções de Processadores

A OCI é uma das duas provedores de nuvem a oferecer opções de processadores:
- **AMD**
- **Intel**
- **Ampere** (processador baseado em ARM)

## VMs Preemptáveis

**VMs preemptáveis** são VMs de baixo custo e curta duração, adequadas para jobs em lote e cargas de trabalho tolerantes a falhas. Elas são semelhantes às instâncias regulares, mas com um custo 50% mais baixo. Você pode usá-las para reduzir ainda mais os custos.