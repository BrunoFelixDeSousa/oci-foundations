# Arquitetura da Oracle Cloud Infrastructure (OCI)

## Principais conceitos da Arquitetura Física da OCI:

- **Regiões**: área geográfica localizada que contém um ou mais Domínios de Disponibilidade (Availability Domains).
- **Domínios de Disponibilidade (AD)**: centros de dados tolerantes a falhas localizados dentro de uma região, conectados entre si por uma rede de baixa latência e alta largura de banda.
- **Domínios de Falha (FD)**: agrupamento de hardware e infraestrutura dentro de um domínio de disponibilidade para fornecer antiafinidade (ou seja, um *centro de dados lógico*).

Uma **região OCI** é composta por um ou mais domínios de disponibilidade isolados e interconectados. Cada domínio de disponibilidade é uma localização física separada dentro de uma região. O número de domínios de disponibilidade por região pode variar: algumas regiões têm três domínios de disponibilidade, enquanto outras têm apenas um.

**Domínios de falha** fornecem proteção para suas aplicações e instâncias contra falhas de hardware inesperadas ou interrupções de rede dentro de um domínio de disponibilidade. Eles garantem **antiafinidade**: cada domínio de falha opera em seu próprio conjunto de hardware físico, de modo que uma falha em um domínio de falha não afeta instâncias em outros domínios de falha.

Um **domínio de falha** é uma subdivisão de um domínio de disponibilidade. Cada domínio de disponibilidade contém três domínios de falha. Domínios de falha permitem distribuir suas instâncias para que não estejam no mesmo hardware físico dentro de um único domínio de disponibilidade. Um domínio de falha não pode estar associado a múltiplos domínios de disponibilidade.

---

## Como escolher uma região?

1. **Localização**: escolha a região mais próxima de seus usuários para garantir a menor latência e o melhor desempenho.

2. **Residência e Conformidade de Dados**: muitos países possuem requisitos rigorosos de residência de dados.

3. **Disponibilidade de Serviços**: novos serviços em nuvem são disponibilizados com base na demanda regional, conformidade regulatória, disponibilidade de recursos, entre outros fatores.

---

## Arquitetura OCI

![Arquitetura OCI](../images/oci_architecture.png)

---

## Design de Alta Disponibilidade

![Alta Disponibilidade](../images/high_availability.png)
