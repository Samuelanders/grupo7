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
