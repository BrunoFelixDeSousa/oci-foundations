# Configuração de Tenancy no OCI

O administrador da tenancy é responsável por criar a conta no Oracle Cloud Infrastructure (OCI) e gerenciar suas operações. No entanto, **as melhores práticas sugerem limitar o uso do administrador da tenancy apenas para tarefas essenciais e configurar administradores dedicados para operações diárias**.

---

## **Melhores Práticas para Configuração de Tenancy**

1. **Evitar usar a conta do administrador da tenancy em operações diárias.**
   - Reserve o administrador da tenancy para tarefas críticas, como configurações iniciais e mudanças importantes.

2. **Criar compartimentos dedicados para isolar recursos.**
   - Por exemplo, separe ambientes de **produção** e **desenvolvimento**.

3. **Implementar autenticação multifator (MFA).**
   - Garanta segurança adicional exigindo MFA para acessar a tenancy.

---

## **Configuração do Administrador do OCI**

### Políticas do Administrador do OCI

No OCI, recursos do IAM não têm um tipo de recurso agregado. Isso significa que as permissões precisam ser concedidas para cada recurso individualmente.

### Exemplo de Declarações de Políticas

1. Permitir que o grupo **oci-admin-group** gerencie todos os recursos na tenancy:
   ```text
   Allow group oci-admin-group to manage all-resources in tenancy
   ```

2. Políticas específicas para gerenciamento de recursos do IAM:
   ```text
   Allow group oci-admin-group to manage domains in tenancy
   Allow group oci-admin-group to manage users in tenancy
   Allow group oci-admin-group to manage groups in tenancy
   Allow group oci-admin-group to manage dynamic-groups in tenancy
   Allow group oci-admin-group to manage policies in tenancy
   Allow group oci-admin-group to manage compartments in tenancy
   ```

---

## **Benefícios**

- **Maior segurança:** reduz o risco de comprometer contas administrativas críticas.  
- **Gestão eficiente:** isola recursos para facilitar gerenciamento e aplicação de políticas específicas.  
- **Conformidade:** promove práticas seguras para proteger dados e recursos sensíveis.

![Configuração de Tenancy](../images/tenancy_setup.png)
