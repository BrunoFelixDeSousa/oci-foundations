# VCN Security

A segurança da **Virtual Cloud Network (VCN)** no Oracle Cloud Infrastructure (OCI) é gerenciada por meio de **Security Lists** e **Network Security Groups (NSGs)**. Esses componentes oferecem controle sobre o tráfego de rede, funcionando como firewalls para proteger os recursos dentro de uma VCN.

## **Security List**

A **Security List** é um conjunto de regras de firewall associadas a uma **sub-rede** (subnet). Essas regras controlam o tráfego de entrada e saída da sub-rede, aplicando-se a todas as instâncias dentro dessa sub-rede. Se uma instância dentro de uma VCN precisa se comunicar com outra instância na mesma rede ou com um host fora da VCN, a **Security List** vai controlar esse tráfego.

### Características da Security List:
- **Firewall para Sub-rede:** Aplica-se a todas as instâncias dentro da sub-rede.
- **Regras de Tráfego:** Define o tráfego de entrada e saída permitido, baseado em protocolos, portas e endereços IP.

![Security List](../images/security_list.png)

---

## **Network Security Group (NSG)**

**Network Security Groups (NSGs)** são conceitos semelhantes às Security Lists, mas com a principal diferença de que as NSGs se aplicam a **interfaces de rede específicas** (NICs) dentro de uma **única VCN**. Isso permite um controle mais granular sobre o tráfego de rede, pois você pode aplicar regras de segurança a recursos individuais, como instâncias de computação ou balanceadores de carga.

### Características do NSG:
- **Controle Granular:** Aplica-se a um conjunto específico de recursos (como uma NIC ou instância).
- **Regras de Tráfego:** Pode ser usado tanto para controle de tráfego de entrada quanto de saída, permitindo maior flexibilidade.
- **Fonte ou Destino:** Um NSG pode ser a fonte ou o destino das regras de tráfego.

Com o **NSG**, é possível especificar quais recursos devem interagir entre si, oferecendo uma camada adicional de segurança em comparação com as **Security Lists**, que aplicam regras de forma mais ampla.

![Network Security Group](../images/network_security_group.png)

---

## **Resumo**

- **Security List:** Aplica regras de firewall a todas as instâncias dentro de uma sub-rede.
- **Network Security Group (NSG):** Aplica regras a interfaces de rede específicas, permitindo controle mais detalhado do tráfego.
- Ambos os mecanismos ajudam a proteger a rede, mas **NSGs** são ideais para um controle mais preciso de acesso entre recursos, enquanto **Security Lists** são adequadas para regras gerais de tráfego em uma sub-rede.

Esses mecanismos ajudam a garantir a segurança da infraestrutura na Oracle Cloud, permitindo controle rigoroso sobre o tráfego de rede entre os recursos, dentro da VCN e fora dela.
