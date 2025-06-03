# grupo7
Fork do grupo7
@startuml
left to right direction

actor Estudante

rectangle "Sistema de Matrícula" {
  usecase "Realizar Matrícula" as UC1
  usecase "Cancelar Matrícula" as UC2
  usecase "Visualizar Disciplinas" as UC3
  usecase "Verificar Matrículas" as UC4
}

Estudante --> UC1
Estudante --> UC2
Estudante --> UC3
Estudante --> UC4
@enduml


@startuml
actor Estudante
participant Sistema
participant Banco

Estudante -> Sistema : login(usuário, senha)
Sistema --> Estudante : confirmação de login

Estudante -> Sistema : solicitarDisciplinas()
Sistema -> Banco : buscarDisciplinas(ano)
Banco --> Sistema : lista de disciplinas
Sistema --> Estudante : exibir disciplinas

Estudante -> Sistema : selecionarDisciplina(id)
Sistema -> Banco : verificarVagas(id)
Banco --> Sistema : vagas disponíveis
Sistema -> Banco : registrarMatricula(idEstudante, idDisciplina)
Banco --> Sistema : matrícula confirmada
Sistema --> Estudante : matrícula registrada
@enduml
