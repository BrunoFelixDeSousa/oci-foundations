[⬅️ Voltar para o README](../README.md)

# Banco de Dados Autônomo

O **Banco de Dados Autônomo** é um banco de dados em nuvem que utiliza aprendizado de máquina para automatizar a afinação de banco de dados, segurança, backups, atualizações e outras tarefas rotineiras de gerenciamento, tradicionalmente realizadas por DBAs.

A ideia é que, quanto mais você puder automatizar e deixar os usuários focados em tarefas diferenciadas e de maior nível, melhor. Isso porque eles não precisam se envolver com tarefas manuais e repetitivas, que também são *propensas a erros*. Usando tecnologias como aprendizado de máquina, podemos retirar essas tarefas da equação, permitindo que os usuários foquem nas tarefas de maior valor e mais estratégicas.

A **função de auto-otimização** do Oracle Autonomous Database permite otimizações automáticas do banco de dados sem intervenção manual. Ele utiliza aprendizado de máquina e automação para realizar tarefas como provisionamento, patching, afinação e backup, o que ajuda a reduzir a necessidade de administração e manutenção manual do banco de dados.

A **função de auto-reparo** do Oracle Autonomous Database garante a recuperação automática do banco de dados em caso de falhas. Ele detecta e corrige problemas na infraestrutura do banco de dados, incluindo falhas de hardware, software e erros humanos, ajudando a manter alta disponibilidade e proteger contra perda de dados.

A **função de auto-segurança** do Oracle Cloud Infrastructure Autonomous Database aplica automaticamente patches de segurança e protege contra ameaças. Ela garante que o banco de dados esteja sempre atualizado com as últimas atualizações de segurança, ajudando a proteger seus dados e manter uma postura de segurança robusta.

O Banco de Dados Autônomo suporta dois tipos de banco de dados/carga de trabalho:
1. **Autonomous Transaction Processing (ATP)**: voltado para OLTP, ideal para transações.
2. **Autonomous Data Warehouse (ADW)**: voltado para processamento analítico online (OLAP).

![Banco de Dados Autônomo](../images/autonomous_database.png)

Mas há outros dois tipos de carga de trabalho:
1. **Autonomous JSON Database**: é um ATP projetado para o desenvolvimento de aplicações NoSQL que utilizam documentos JSON.
2. **APEX Service**: voltado para desenvolvedores que constroem aplicações de baixo código (low-code) com APEX.

![Otimizado por Carga de Trabalho](../images/optimized_by_workload.png)