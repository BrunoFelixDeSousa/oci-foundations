[⬅️ Voltar para o README](../README.md)

# VCN Routing

O **Route Tables** (tabelas de rotas) da VCN são responsáveis por direcionar o tráfego para fora da VCN, seja para a internet, para redes on-premises ou para VCNs emparelhadas.

As tabelas de rotas consistem em um conjunto de **regras de rota**. Cada regra especifica um bloco CIDR de destino e um **target de rota** (o próximo salto para o tráfego que corresponde ao bloco CIDR de destino).

### **Roteamento Interno**

Dentro de uma VCN, o tráfego entre sub-redes é automaticamente gerido pelo **roteamento local da VCN**, ou seja, não é necessário adicionar entradas nas tabelas de rotas para a comunicação entre sub-redes públicas e privadas.

---

### **Tabela de Rotas e Regras**

As **regras de rota** determinam para onde o tráfego deve ser enviado com base no bloco CIDR de destino. As opções comuns de roteamento incluem:

- **Roteamento para a Internet** (Internet Gateway)
- **Roteamento para redes on-premises** (Dynamic Routing Gateway - DRG)
- **Roteamento para VCNs emparelhadas** (Local Peering Gateway)

---

### **Peering de VCN**

**VCN Peering** é uma conexão de rede entre duas VCNs que permite o roteamento de tráfego entre elas usando endereços IP privados. A conexão de peering não é baseada em VPN, mas sim uma conexão direta de rede.

As VCNs emparelhadas não podem ter CIDRs sobrepondo-se, ou seja, os endereços IP das duas redes precisam ser exclusivos.

**Tipos de Peering**:

1. **Local Peering (mesma região)**: Para conectar VCNs dentro da mesma região do OCI.
2. **Remote Peering (diferentes regiões)**: Para conectar VCNs em regiões diferentes através de um **Dynamic Routing Gateway (DRG)**.

![VCN Peering](../images/vcn_peering.png)

---

### **Dynamic Routing Gateway v2**

Quando há centenas de VCNs, a gestão do roteamento pode se tornar complexa. Para isso, o **Dynamic Routing Gateway v2 (DRG v2)** oferece uma solução mais eficiente, permitindo que várias VCNs se conectem a um ponto central de roteamento, simplificando o gerenciamento e a escalabilidade.

![Dynamic Router Gateway v2](../images/drg_v2.png)

---

## **Resumo**

- **Roteamento Local:** Tráfego dentro de uma VCN entre sub-redes é automaticamente gerenciado.
- **Roteamento Externo:** Usa tabelas de rotas para enviar tráfego para a internet, redes on-premises ou VCNs emparelhadas.
- **Peering de VCN:** Conexões privadas entre VCNs para comunicação sem sobrecarga da internet.
- **DRG v2:** Melhora a escalabilidade do roteamento quando se tem múltiplas VCNs.

Este modelo oferece flexibilidade, segurança e controle completo sobre como os recursos dentro do OCI comunicam-se entre si e com redes externas.
