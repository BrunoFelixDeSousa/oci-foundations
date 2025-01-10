[⬅️ Voltar para o README](../README.md)

# Escalabilidade

Existem dois tipos de escalabilidade:
- Escalabilidade vertical
- Escalabilidade horizontal

## Escalabilidade Vertical (escala para cima/para baixo)

A escalabilidade vertical significa que você está alterando o formato das instâncias, ou seja, escalando para cima ou para baixo.

A nova configuração precisa ter a **mesma arquitetura de hardware**.

Quando você escala para cima ou para baixo, há **tempo de inatividade necessário**.

Boa prática: pare sua instância antes de realizar qualquer tipo de escalabilidade vertical.

![Escalabilidade Vertical](../images/vertical_scaling.png)

## Escalabilidade Horizontal (Autoscaling) (escala para fora/para dentro)

A escalabilidade horizontal significa que você adiciona mais VMs do mesmo tipo ou faz ajustes na quantidade de VMs do mesmo tipo. Isso permite implantações de grande escala de VMs.

Por que isso é tão popular e poderoso? O motivo é que ele oferece a capacidade de escalar, mas também proporciona **alta disponibilidade**. Além disso, o que o torna ainda mais poderoso é que você pode ajustar a demanda de tráfego adicionando ou removendo VMs **automaticamente**. Não há custo adicional para usar o Autoscaling.

Para configurar o Autoscaling, existem três etapas que você deve seguir:
1. Criar um **modelo** (configuração): imagem do sistema operacional, metadados, tipos de instância, cNICs, etc.
2. Criar um **pool de instâncias**: um conjunto de instâncias pré-configuradas.
3. Criar as **regras de autoscaling**: tamanho mínimo, tamanho máximo, etc.

O autoscaling em um pool de instâncias dentro do serviço de Computação da OCI provisiona e remove instâncias automaticamente com base em condições ou horários específicos. Não altera o tipo de instância de computação, nem é limitado apenas ao autoscaling baseado em métricas ou horários. Em vez disso, o autoscaling pode ser acionado por políticas **baseadas em métricas** ou **baseadas em horários**, oferecendo uma solução de escalabilidade mais dinâmica e flexível.

![Regras de Autoscaling](../images/autoscaling_rules.png)