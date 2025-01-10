# Volume de Bloco

O serviço de **Volume de Bloco** fornece armazenamento persistente e durável para instâncias de computação. Os dados são armazenados de forma independente do ciclo de vida da instância. "Durável" significa que fazemos múltiplas cópias. Assim, mesmo que uma cópia seja perdida, temos outras cópias dos dados disponíveis no data center.

**Tipos de Volume de Bloco:**
1. **Custo mais baixo**: cargas de trabalho de I/O sequenciais grandes (armazenamento de dados em streaming).
2. **Equilibrado**: escolha balanceada para I/O aleatória (discos de inicialização).
3. **Maior performance**: cargas de trabalho mais exigentes de I/O.
4. **Ultra Alta Performance**: cargas de trabalho com maior demanda de I/O (bancos de dados relacionais).

![Níveis de Performance do Volume de Bloco](../images/block_volume_tiers.png)

No caso do volume de bloco, existe um conceito chamado **unidade de performance do volume de bloco**. Isso inclui o conceito de **Unidades de Performance de Volume (VPUs)**. Você pode adquirir mais VPUs para alocar mais recursos para um volume, aumentando seu IOPS por gigabyte e a taxa de transferência por gigabyte.

O serviço de **Volume de Bloco** da OCI utiliza replicação para garantir durabilidade dos dados e proteção contra falhas de hardware. Os dados são automaticamente replicados entre múltiplos dispositivos de armazenamento dentro da mesma **domínio de disponibilidade**, o que ajuda a manter a integridade e disponibilidade dos dados em caso de falhas de hardware.

Os Volumes de Bloco da OCI são automaticamente replicados dentro de um domínio de disponibilidade para garantir alta durabilidade, garantindo redundância de dados e proteção contra falhas de hardware.

## Ajuste Automático de Performance

O **Ajuste Automático de Performance** ajuda a economizar nos custos. Ele altera a performance do volume para uma configuração de menor custo quando o volume é desanexado. Quando o volume é reanexado, a performance do volume é automaticamente ajustada para a configuração anterior.

## Criptografia

A criptografia é ativada por padrão (não é possível desativá-la). A OCI também oferece **criptografia em trânsito**, ou seja, quando sua máquina virtual se comunica com o serviço de armazenamento de blocos, o tráfego é criptografado enquanto está em trânsito entre a máquina virtual e o serviço de bloco.

## Compartilhamento de Leitura/Gravação

O serviço de volume de bloco oferece a funcionalidade de **compartilhamento de leitura/gravação**, onde um único disco pode ser compartilhado com várias VMs e essas VMs podem ler e gravar no mesmo volume de bloco.

## Redimensionamento de Volumes de Bloco

1. **Redimensionamento off-line**
2. **Redimensionamento on-line**: você pode expandir o tamanho do volume sem desvinculá-lo de uma instância, mantendo suas aplicações em funcionamento.

## Replicação (Assíncrona) de Volumes de Bloco

Os Volumes de Bloco estão sendo replicados de uma região para outra.

Cenários:
- Recuperação de desastres
- Migração
- Expansão de negócios

## Grupos de Volumes

O serviço de Volume de Bloco oferece a capacidade de agrupar múltiplos volumes em o que chamamos de **grupo de volumes**. Isso simplifica o processo de criar backups consistentes no tempo de aplicações em execução que abrangem múltiplos volumes em várias instâncias.