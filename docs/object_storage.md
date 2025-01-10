[⬅️ Voltar para o README](../README.md)

# Armazenamento de Objetos

Características do Armazenamento de Objetos OCI:
- Plataforma de armazenamento de alto desempenho em escala de internet
- Dados gerenciados como objetos
- Ideal para dados não estruturados
- Serviço público regional
- Vários níveis de armazenamento
- Acesso privado de recursos OCI (por exemplo, computação)
- Capacidades avançadas

Cenários de uso do Armazenamento de Objetos OCI:
- Repositório de conteúdo
- Dados não estruturados e semi-estruturados
- Cenário de big data (Spark, Hadoop, Análise de Dados)
- Arquivamento/Backups

## Como funciona?

Qualquer coisa que você armazene no armazenamento de objetos é referenciada como **objeto**. Pense em um objeto como *pares chave-valor* ou *pares nome-valor*, onde o nome é o nome do arquivo que você está armazenando e o valor é o valor real do arquivo. Além disso, os objetos também podem ter **metadados de objetos** e você pode definir seus próprios metadados ali.

Os objetos são armazenados em um **bucket** e os buckets possuem um nome exclusivo dentro da tenência. Algo importante a se lembrar é que há uma *hierarquia plana*. E sempre que você vê uma estrutura de pastas, ela é simulada pelo serviço de armazenamento de objetos usando algo chamado *prefixos*.

Também há algo chamado **namespace**. O namespace é uma entidade lógica. É um contêiner de nível superior para todos os buckets de objetos. Ele precisa ter um nome globalmente exclusivo.

![Armazenamento de Objetos](../images/object_storage.png)

## Níveis de Armazenamento de Objetos

1. **Padrão (Hot Tier)**:
    - Dados críticos
    - Acesso rápido, imediato e frequente
    - Cópia mais recente dos dados
    - Recuperação instantânea
    - Não pode ser rebaixado

2. **Acesso Infrequente (Cool Tier)**:
    - Dados críticos
    - Ideal para dados acessados de forma infrequente (por exemplo, backups)
    - Custo de armazenamento mais baixo que o Nível de Armazenamento Padrão (60% mais barato)
    - Retenção mínima exigida (31 dias)
    - Taxas de recuperação

3. **Arquivo (Cold Tier)**:
    - Dados raramente acessados (por exemplo, armazenamento em fita)
    - Retenção mínima exigida (90 dias)
    - Objetos precisam ser restaurados antes do download
    - Tempo de restauração: 1 hora
    - Tempo de download: 24 horas
    - Bucket de arquivo não pode ser atualizado

## Auto-Tiering

Existe uma funcionalidade chamada **auto-tiering** que observa seu padrão de acesso e pode mover os dados do nível padrão para o nível de acesso infrequente e vice-versa.

## Gerenciamento de Ciclo de Vida

Ajuda a transitar os dados de níveis de custo mais altos para níveis de custo mais baixos. Você pode configurar, por exemplo, que após 30 dias, seus dados sejam movidos do nível padrão para o nível de arquivo, e excluídos após 180 dias. Você escreve uma regra e o serviço cuida disso.

## Versionamento

Você também pode fazer versionamento, pois ao armazenar seus dados, pode ter várias versões desses dados. Esses objetos são automaticamente versionados. Você só precisa especificar isso no bucket e a OCI cuida disso.

## Criptografia de Dados

Isso é muito importante porque você está armazenando dados sensíveis na Nuvem. Por isso, fornecemos criptografia de dados **por padrão**. Você não pode desativá-la. No entanto, você pode sempre usar suas próprias chaves para requisitos mais rigorosos, se necessário.

## URL de Solicitação Pré-Autenticada

Uma URL de solicitação pré-autenticada é um recurso no serviço de Armazenamento de Objetos OCI que fornece acesso temporário e seguro a um objeto específico. Ela permite que os usuários gerem uma URL única com um tempo de expiração predefinido, permitindo que usuários externos acessem o objeto sem necessidade de autenticação ou autorização por meio do OCI Identity and Access Management.

## Acesso aos Dados

O Armazenamento de Objetos é um serviço público, e você acessa os dados usando um **endpoint API** público.

    https://<região>.oraclecloud.com/p/<token>/n/<namespace>/b/<bucket>/o/log.zip

    /p = solicitação pré-autenticada (opcional)
    /n = namespace
    /b = bucket
    /o = objeto  

![Recurso de Armazenamento de Objetos](../images/object_storage_resource.png)