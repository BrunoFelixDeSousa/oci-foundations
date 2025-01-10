# Zonas de Segurança & Security Advisor

**Security Zone** refere-se a um compartimento de nuvem no qual você não pode desativar a segurança.

**Security Advisor** é um serviço de nuvem que unifica o Security Zone, Cloud Guard e outras capacidades em um conjunto coeso.

## Zonas de Segurança

Em termos de uso funcional, **Zonas de Segurança** e uma **Receita de Zona de Segurança** podem ser classificadas como **Medidas Preventivas**.

![Zonas de Segurança](../images/security_zones.png)

Quando você cria uma Zona de Segurança, você seleciona um ou mais compartimentos e uma receita. Uma Receita de Zona de Segurança especifica as políticas que você deseja aplicar. A Oracle fornece um conjunto padrão de políticas, mas você pode criar suas próprias políticas.

Qualquer tentativa de criar ou modificar recursos na zona de segurança que viole uma das políticas da zona é negada. A Zona de Segurança utiliza o Cloud Guard, como mostrado no diagrama, para realizar varreduras periódicas nas suas zonas e relatar qualquer violação das políticas da zona.

**Observação:** você deve ativar o Cloud Guard antes de poder usar as Zonas de Segurança.

A principal vantagem de usar Zonas de Segurança da OCI ao implantar recursos em seu ambiente de nuvem é garantir a conformidade com as melhores práticas e políticas de segurança. As Zonas de Segurança ajudam a manter uma postura de segurança forte, aplicando automaticamente as políticas de segurança predefinidas dentro dos compartimentos designados, impedindo a criação de recursos não conformes.

![Exemplo de Zona de Segurança](../images/security_zone_example.png)

## Security Advisor

O Security Advisor é um serviço combinado que reúne a funcionalidade fornecida pelo Cloud Guard, Security Zone e outros serviços de segurança, trazendo-os juntos em um único serviço coeso.

![Security Advisor](../images/security_advisor.png)