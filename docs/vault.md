# Oracle Vault

O OCI Vault é um serviço gerenciado que permite gerenciar centralmente chaves de criptografia e credenciais secretas. O Vault elimina a necessidade de armazenar chaves de criptografia e segredos em arquivos de configuração ou no código. O serviço é regional e possui um endpoint de API pública que pode ser utilizado.

Os segredos são credenciais, como senhas, certificados, chaves SSH ou tokens de autenticação, que podem ser usados com os serviços da Oracle Cloud Infrastructure.

O principal objetivo do serviço OCI Vault é armazenar e gerenciar chaves de criptografia e segredos. O serviço Vault ajuda você a armazenar, gerenciar e controlar o acesso a chaves de criptografia, segredos e certificados de forma segura, garantindo a proteção de dados sensíveis.

O OCI Vault é composto por vários componentes, incluindo chaves de criptografia mestre, segredos e cofres. Um cofre no OCI é uma entidade lógica onde você pode gerenciar e armazenar centralmente suas chaves de criptografia e segredos. Um segredo é um recurso que ajuda a gerenciar credenciais necessárias para acessar os recursos do OCI. Uma chave de criptografia mestre é uma chave que a OCI usa para criptografar as chaves de criptografia que você cria no cofre (essas são gerenciadas pelo cliente). Backup de banco de dados não é um componente do OCI Vault; é uma funcionalidade associada ao serviço de banco de dados OCI.

## Criptografia de Envelope

O funcionamento do Vault é chamado de **criptografia de envelope**. É uma hierarquia de duas camadas para chaves:
- Camada-1: as **chaves de criptografia de dados** criptografam os dados do cliente.
- Camada-2: as **chaves de criptografia mestre** criptografam as chaves de dados.

Como mostrado na imagem, a chave mestre é usada para criptografar a chave de dados. Então, vemos que, fora da caixa central onde os dados são criptografados pela chave mestre, a criptografia real para o armazenamento, seja em armazenamento de bloco, armazenamento de objetos ou armazenamento de arquivos, é feita usando a chave de dados.

Você pode usar políticas de IM (Identity and Management) para autorizar o acesso às chaves mestres e auditorias de log para monitorar todas as atividades relacionadas às chaves.

### Quais são os benefícios?
- É mais fácil de gerenciar.
- Limita o impacto de falhas (blast radius).
- Não gera uma recriptografia completa dos dados.

**IMPORTANTE**: Se a chave mestre for excluída, **não há como recuperar os dados!**

A OCI realiza uma exclusão suave das chaves com um intervalo de sete dias. O cofre não pode ser excluído imediatamente. Você pode agendar a exclusão configurando um período de espera. O cofre e todas as chaves criadas dentro dele são excluídos ao final desse período de espera. Todos os dados protegidos por essas chaves não estarão mais acessíveis após a exclusão do cofre. Por isso, esse período de 7 a 30 dias é projetado dessa forma.

**IMPORTANTE**: uma vez que o cofre seja excluído, **não pode ser recuperado!**

![Vault](../images/vault.png)

![Exemplo de Vault](../images/vault_example.png)