[⬅️ Voltar para o README](../README.md)

# Virtual Cloud Network (VCN)

A **Virtual Cloud Network** (VCN) no Oracle Cloud é uma rede privada e definida por software, projetada para comunicação segura. Ela existe dentro de uma região do OCI.

Uma VCN é uma rede privada virtual que você configura nos data centers da Oracle dentro de uma única região do OCI. Ela se assemelha a uma rede tradicional, com regras de firewall e tipos específicos de gateways de comunicação que você pode escolher usar. Uma VCN abrange todos os domínios de disponibilidade na região.

---

## **Espaço de Endereçamento da VCN**

A VCN possui um **espaço de endereçamento** (faixa de endereços IP). Você pega essa faixa e a divide em redes menores, chamadas de *sub-redes*. Essas sub-redes são onde você instanciaria suas instâncias de computação.

![VCN Address Space](../images/vcn_address_space.png)

---

## **Mecanismos de Comunicação dentro de uma VCN**

Existem diversos mecanismos para comunicação dentro de uma VCN:

1. **Internet Gateway**: Comunicação bidirecional entre a VCN e a internet.
2. **NAT Gateway**: Comunicação unidirecional de uma VCN para a internet (usado principalmente para instâncias privadas acessarem a internet).
3. **Service Gateway**: Acesso de uma VCN a serviços públicos da Oracle dentro da mesma região.
4. **Dynamic Router Gateway (DRG)**: Acesso de uma VCN a destinos fora da internet, como redes on-premises ou outras VCNs na mesma ou em diferentes regiões.

### **Service Gateway**

O **Service Gateway** no Oracle Cloud Infrastructure permite acesso a serviços da Oracle dentro da mesma região, sem que o tráfego precise passar pela internet pública. Isso oferece uma conexão mais segura e confiável para acessar serviços da Oracle, como **Object Storage**, **Autonomous Database**, entre outros.

---

## **Exemplos de Comunicação**

- **Comunicação com a Internet**:

   Com o **Internet Gateway**, é possível realizar comunicação bidirecional entre a VCN e a internet, permitindo que as instâncias dentro da VCN acessem recursos externos, como sites e serviços, além de permitir que usuários externos acessem serviços expostos na VCN.

   ![Communication Internet](../images/vcn_internet.png)

- **Comunicação com Redes On-Premises**:

   Com o **Dynamic Router Gateway (DRG)**, a VCN pode se comunicar com redes on-premises ou outras VCNs em regiões diferentes, usando uma conexão privada ou VPN, sem passar pela internet pública.

   ![Communication On-Premises](../images/vcn_on_premises.png)

---

## **Benefícios**

- **Segurança:** A VCN oferece controle completo sobre o tráfego de rede dentro da sua nuvem, permitindo regras de firewall, segmentação por sub-redes e integração com políticas de segurança.
- **Escalabilidade:** Suporta o uso de múltiplas sub-redes para distribuir cargas de trabalho em diferentes zonas de disponibilidade, aumentando a disponibilidade e a resiliência.
- **Conectividade personalizada:** Oferece diferentes gateways para diferentes tipos de comunicação, seja com a internet, com redes externas ou com outros serviços dentro da Oracle Cloud.
