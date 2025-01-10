# Balanceador de Carga

Um **Balanceador de Carga** permite que você obtenha *alta disponibilidade* e *alta escalabilidade*. Eles também são conhecidos como **Proxy Reverso**.

O **Balanceador de Carga** da Oracle Cloud Infrastructure suporta três tipos de algoritmos de balanceamento de carga:
1. Round Robin
2. Least Connections
3. IP Hash

NOTA: Round Robin ponderado, Least Connections ponderado e Random não são suportados pelo Balanceador de Carga do OCI.

## HTTP/S (Camada 7) Balanceador de Carga

O primeiro tipo de Balanceador de Carga no OCI é o **HTTP/S (Camada 7) Balanceador de Carga**. A Camada 7 basicamente significa que ele entende HTTP e HTTPS, de acordo com o modelo OSI.

O Balanceador de Carga vem em dois formatos diferentes:
- **Formato flexível**: você define o mínimo e o máximo e define o intervalo.
- **Formato dinâmico**: você predefine os formatos (micro, pequeno, médio, grande). Não é necessário aquecer o Balanceador de Carga. Se o tráfego chegar a esse formato específico, o Balanceador de Carga se ajusta automaticamente.

O Balanceador de Carga pode ser:
- **Público**: está disponível na web.
- **Privado**: significa que seus múltiplos níveis, como o nível web, podem se comunicar com o nível do banco de dados e balancear o tráfego entre eles, mas ambos os níveis não precisam ser públicos.

![Balanceador de Carga](../images/http_load_balancer.png)

## Network (Camada 4) Balanceador de Carga

O segundo tipo de Balanceador de Carga no OCI é chamado **Network (Camada 4) Balanceador de Carga**. E, como o nome indica, o Balanceador de Carga de Rede opera nas camadas 3 e 4, ou seja, entende TCP, UDP e também suporta ICMP.

Assim como o Balanceador de Carga HTTP, ele tem as opções pública e privada.

![Network Load Balancer](../images/network_load_balancer.png)

## Balanceador de Carga HTTP/S vs Balanceador de Carga de Rede

Por que você usaria o Balanceador de Carga de Rede ou o Balanceador de Carga HTTP?

A principal razão para usar o Balanceador de Carga de Rede é que ele é muito mais rápido do que o Balanceador de Carga HTTP. Ele tem uma latência muito mais baixa. Então, se o desempenho é um critério importante para você, opte pelo Balanceador de Carga de Rede. Por outro lado, o Balanceador de Carga HTTP tem inteligência de nível mais alto porque ele pode analisar os pacotes, inspecionar os pacotes e obter essas informações. Então, se você está buscando esse tipo de inteligência de roteamento, vá com o Balanceador de Carga HTTP.
