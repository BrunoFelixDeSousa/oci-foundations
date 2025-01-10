# Noções Básicas de Instância

Uma instância é um host de computação e possui várias dependências.

O armazenamento em bloco é o tipo de armazenamento associado às instâncias no serviço OCI Compute. Ele fornece volumes de armazenamento de baixa latência e alto desempenho, que podem ser anexados às instâncias para armazenar dados e aplicativos.

A **Configuração da Instância** é uma configuração predefinida que inclui a forma da instância, a imagem base e os metadados. Ela permite que os usuários criem rapidamente novas instâncias com a mesma configuração, agilizando o processo de implantação.

![Noções Básicas de Instância](../images/instance_basics.png)

## Migração ao Vivo

Há uma funcionalidade adicional que é realmente relevante quando se fala sobre instâncias de computação, que é a migração ao vivo. Sabemos que os computadores falham o tempo todo. Então, como garantir que o host de computação que você está utilizando esteja sempre funcionando? Temos essa funcionalidade chamada **Migração ao Vivo**. A ideia aqui é que, se um dos hosts de computação cair ou apresentar um problema, migraremos sua VM para outro host em nosso data center, e isso será transparente para você. Existem várias opções disponíveis (seja opt-in ou opt-out) que você pode escolher. Mas a ideia é que migramos suas máquinas virtuais, permitindo que você faça migração ao vivo entre hosts sem precisar reiniciar. Isso mantém suas aplicações em funcionamento mesmo durante eventos de manutenção. Conseguir isso em seus próprios data centers não é uma tarefa simples, mas fazemos com que seja tranquilo dentro da OCI.