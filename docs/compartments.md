# Compartimentos no Oracle Cloud Infrastructure (OCI)

Ao abrir uma conta no OCI, você recebe uma **tenancy** (nome sofisticado para conta) e um **compartimento raiz**.

Um *root compartment* é uma construção lógica onde são mantidos todos os recursos da nuvem. Dentro do compartimento raiz, é possível criar compartimentos específicos para isolamento e controle de acesso. Todos os compartimentos criados são globais e estão disponíveis em todas as regiões acessíveis.

**Nota:** A melhor prática é criar compartimentos dedicados para isolar os recursos.

---

## Principais Características

- Cada recurso pertence a um único compartimento.
- Recursos podem interagir com outros recursos em compartimentos diferentes.
- Recursos podem ser movidos de um compartimento para outro.
- Recursos de várias regiões podem estar no mesmo compartimento.
- Compartimentos podem ser aninhados (até seis níveis de aninhamento).
- É possível definir cotas e orçamentos para compartimentos.

---

![Compartimentos](../images/compartments.png)

![Múltiplas Regiões](../images/multiple_regions.png)
