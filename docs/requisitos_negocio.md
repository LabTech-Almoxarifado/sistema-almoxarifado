# 📋 Requisitos de Negócio e Funcionais

## Regra de Negócio Central (Lógica Core)
A operação de **Empréstimo** atua como uma entidade associativa que vincula um Aluno a um ou mais Equipamentos. 
* **Bloqueio de Segurança:** É estritamente proibido o registro de um novo empréstimo para equipamentos cujo status atual seja "Em Manutenção" ou "Em Uso".

## Perfis de Acesso
1.  **Técnico (Admin):** Possui privilégios totais (cadastro de equipamentos, alteração manual de status, visão global de empréstimos e atrasos).
2.  **Aluno:** Possui privilégios restritos (consulta de catálogo, visualização de disponibilidade).

## Requisitos Funcionais (RF)
* **RF01:** O sistema deve permitir o cadastro de equipamentos com número de patrimônio e categoria.
* **RF02:** O sistema deve fornecer uma interface de consulta para visualizar a disponibilidade dos itens em tempo real.
* **RF03:** O sistema deve permitir o registro de saída (empréstimo) de um equipamento com data de devolução prevista.
* **RF04:** O sistema deve permitir o registro de retorno (devolução) com atualização automática do status do item.
