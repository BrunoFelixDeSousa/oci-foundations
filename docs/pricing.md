[⬅️ Voltar para o README](../README.md)

# Preços

O modelo de preços da Oracle é simples, transparente e mais barato que os concorrentes.

O OCI tem o mesmo modelo de preços em todo o mundo, o que é diferente do modelo tradicional de nuvem, onde os preços são ajustados localmente.

Fatores que impactam o preço:
- **Tamanho dos recursos** (recursos maiores custam mais)
- **Tipo de recurso** (VMs vs BMs, VMs vs Funções, etc.)
- **Transferência de dados** (sem custo de entrada, cuidado com o custo de saída)

## Modelos de Preços

**Modelo Pay As You Go (PAYG)**:
- Cobrado apenas pelo recurso consumido
- Sem compromisso inicial
- Sem período mínimo de serviço
- Uso medido

**Modelo Anual (ou Mensal) de Créditos Universais**:
- Compromisso com um pool anual de recursos
- Economias significativas
- Os créditos devem ser usados dentro de 12 meses
- Descontos baseados no tamanho e duração do contrato
- Se o uso de recursos exceder o valor comprometido, o pagamento será feito com base no modelo PAYG

**Modelo Bring Your Own License (BYOL)**:
- Aplica suas licenças atuais do Oracle em servidores equivalentes, altamente automatizados de IaaS e PaaS na nuvem
- Mobilidade completa de licenças com instalações locais

**Modelo de Preço com Base no Consumo**:
- Cobrado apenas quando o recurso é consumido
- Ideal para a plataforma serverless gerenciada chamada **Funções**

## Custos de Transferência de Dados

No OCI, você não paga pela transferência de dados entre os Domínios de Disponibilidade.

O tráfego de entrada é **gratuito**, mas o tráfego de saída é **10 vezes mais barato** do que em alguns outros provedores de nuvem.

Na OCI, a transferência de dados de entrada (dados que vêm da internet para a OCI) é normalmente gratuita. No entanto, a transferência de dados de saída (dados que saem da OCI para a internet) é cobrada após os primeiros 10 TB/mês, dependendo da região e do destino.

![Custos de Transferência de Dados](../images/data_transfer_costs.png)