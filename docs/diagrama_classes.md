# 🏗️ Diagrama de Classes

```mermaid
classDiagram
    class Usuario {
        <<Abstract>>
        -String matricula
        -String nome
        -String email
        -String senhA
        +login()
        +consultarDisponibilidade()
    }

    class Tecnico {
        -String turno
        +cadastrarEquipamento()
        +atualizarStatus()
        +registrarEmprestimo()
        +registrarDevolucao()
    }

    class Aluno {
        -String curso
        +solicitarEmprestimo()
    }

    class Equipamento {
        -String numPatrimonio
        -String nome
        -String categoria
        -String status
    }

    class Emprestimo {
        -int idEmprestimo
        -Date dataSaida
        -Date dataDevolucaoPrevista
        +finalizarEmprestimo()
    }

    Usuario <|-- Tecnico
    Usuario <|-- Aluno
    Aluno "1" -- "0..*" Emprestimo
    Equipamento "1" -- "0..*" Emprestimo
    Tecnico "1" -- "0..*" Emprestimo
