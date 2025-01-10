[⬅️ Voltar para o README](../README.md)

# Noções Básicas de Criptografia

A criptografia é usada para transformar dados em texto simples em texto cifrado (também referido como texto criptografado).

## Em Repouso vs Em Trânsito

**Criptografia em repouso** garante que os dados (armazenados em um dispositivo físico, como um servidor, etc.) sejam ilegíveis sem as chaves necessárias para descriptografá-los. Assim, se um invasor obtiver um disco rígido com dados criptografados e não tiver acesso às chaves de criptografia, ele não conseguirá ler esses dados.

**Criptografia em trânsito** refere-se basicamente aos dados que estão se movendo de um local para outro, como pela internet ou através de uma rede privada. Você pode realizar criptografia em trânsito para garantir que os dados estejam seguros. O HTTPS é um exemplo de criptografia em trânsito. A criptografia de dados em trânsito basicamente os protege de atacantes externos e fornece um mecanismo para transmitir dados enquanto limita o risco de exposição.

![Criptografia](../images/encryption.png)

## Simétrica vs Assimétrica

A criptografia de chave simétrica é quando uma **única chave** é usada para criptografar e descriptografar os dados.

A criptografia assimétrica é quando chaves diferentes são usadas para criptografar e descriptografar os dados. Um par de chaves (privada/pública) é gerado com um algoritmo específico para ser usado na criptografia (ou seja, assinatura digital).

## Algoritmos de Criptografia

**Algoritmo AES (Advanced Encryption Standard)**: a mesma chave criptografa e descriptografa os dados. Não **pode** ser usado para assinatura digital.

**Algoritmo RSA (Rivest–Shamir–Adleman)**: a chave pública criptografa os dados e a chave privada descriptografa os dados. Pode ser usado para assinatura digital. RSA é mais intensivo computacionalmente e é um pouco mais lento.

**Algoritmo ECDSA (Elliptic Curve Digital Signature Algorithm)**: as chaves são geradas por criptografia de curva elíptica, que é menor do que as chaves médias geradas pelos algoritmos de assinatura digital. É um dos algoritmos de criptografia de chave pública mais complexos. Pode ser usado **apenas** para assinatura digital, não para criptografia e descriptografia de dados.

## Módulo de Segurança de Hardware (HSM)

O Módulo de Segurança de Hardware é um dispositivo de computação físico que protege e gerencia chaves.

O HSM possui características únicas:
- é à prova de violação
- é usado para gerenciar chaves digitais
- executa funções criptográficas

Os HSMs geralmente são certificados por padrões internacionalmente reconhecidos, como Common Criteria ou FIPS 140, para fornecer aos usuários uma garantia independente de que o design e a implementação do produto e dos algoritmos criptográficos são sólidos.

A Oracle Cloud Infrastructure fornece um serviço chamado **Vault** que utiliza HSM nos bastidores. Os HSMs que ela utiliza atendem à certificação FIPS 140-2 Nível de Segurança 3 (o máximo é 4).