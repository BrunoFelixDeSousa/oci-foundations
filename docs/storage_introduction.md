[⬅️ Voltar para o README](../README.md)

# Introdução ao Armazenamento

**Requisitos de Armazenamento:**
- **Persistente vs. Não Persistente:** Armazenamento persistente mantém dados de forma permanente, enquanto o não persistente é temporário.
- **Tipo de Dados:** Pode ser banco de dados, textos, vídeos, fotos, entre outros.
- **Desempenho:** Considera capacidade, IOPS (operações de entrada/saída por segundo), e throughput (taxa de transferência de dados).
- **Durabilidade:** Quantidade de cópias de dados feitas para garantir recuperação em caso de falha.
- **Conectividade:** Pode ser armazenamento local ou em rede, com diferentes formas de acesso aos dados.
- **Protocolo:** Pode envolver armazenamento de blocos, arquivos ou HTTP.

## Serviços de Armazenamento OCI

1. **NVMe Local:** Armazenamento anexado localmente, ideal para aplicações sensíveis ao desempenho. Pode ser usado para armazenar dados com altas exigências de IOPS.

2. **Block Volume:** Armazenamento de volume fixo em um servidor de rede, associado a uma instância de computação. A vantagem é a persistência e durabilidade dos dados, que podem sobreviver à instância. O armazenamento é gerido em **blocos de tamanho fixo**. Você cria uma partição, um sistema de arquivos e então monta esse sistema.

3. **File Storage:** Semelhante ao Block Volume, mas oferece um sistema de **armazenamento de arquivos compartilhado**, no qual você gerencia os dados como arquivos e diretórios. Não é necessário particionar o disco, e ainda assim você monta o sistema de arquivos.

4. **Object Storage:** Usado para armazenar fotos, vídeos, arquivos de log, textos e qualquer tipo de arquivo acessado via **web**. A forma típica de acesso é através de clientes HTTP que utilizam os verbos PUT e GET para interagir com objetos.

Além desses serviços de armazenamento, a OCI oferece alguns serviços de migração de dados:

- **Data Transfer Disk:** Você envia os discos para a Oracle, que migra os dados para o OCI.
- **Data Transfer Appliance:** Uma solução maior onde você envia um dispositivo físico, e a Oracle realiza a migração dos dados.
- **Storage Gateway:** Um appliance Linux no seu data center que possibilita a migração de dados para o OCI.

![Serviços de Armazenamento OCI](../images/oci_storage_service.png)