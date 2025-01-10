# Oracle Cloud Infrastructure IAM

IAM significa **Serviço de Gerenciamento de Identidade e Acesso** (*Identity and Access Management*).

Também é conhecido como:
- **Controle de Acesso Granular**
- **Controle de Acesso Baseado em Funções** (*Role-Based Access Control*).

Este serviço possui dois aspectos principais:
- **Autenticação (AuthN)**: está relacionada à identidade (quem alguém é).
- **Autorização (AuthZ)**: está relacionada às permissões (o que alguém tem permissão para fazer).

O IAM no OCI consiste em Principais, Políticas, Federação e outros componentes.

---

## Domínios de Identidade

Um *Identity Domain* é um contêiner para usuários e grupos.

### Como funciona?

1. Crie um *Identity Domain*.
2. Crie Usuários e Grupos.
3. Escreva Políticas para esses grupos.
4. As Políticas são vinculadas a uma *tenancy* (locação), conta ou compartimento.
5. Os recursos estão disponíveis dentro de um compartimento.

---

Cada recurso no OCI possui um identificador atribuído chamado **Oracle Cloud ID (OCID)**. A Oracle gera esses identificadores únicos.

A sintaxe é:

```plaintext
ocid1.<resource_type>.<realm>.[region][.future_use].<unique_id>
```

Onde:
- **resource_type**: tipo do recurso (por exemplo, instância de computação, armazenamento em bloco, etc.).
- **realm**: conjunto de regiões com as mesmas características (por exemplo, comercial, governo, etc.).
- **region**: código da região.
- **unique_id**: identificador único do recurso.

### Exemplos:
- **Tenancy**:  
  `ocid1.tenancy.oc1..aaaaartg56hjrtyu84556fdfdtqu56`  
  *(Nota: sem região)*  
- **Volume em Bloco**:  
  `ocid1.volume.oc1.eu-frankfurt-1.dsarhsd456hfd98fkajh45as`

![Conceitos de Identidade OCI](../images/oci_identity_concepts.png)

![Gerenciamento de Identidade e Acesso](../images/iam.png)
