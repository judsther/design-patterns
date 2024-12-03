Ejercicio 3:

Patrón Decorator: permite añadir funcionalidades a objetos de manera dinámica, sin alterar su estructura original.

```mermaid
classDiagram
    class Personaje {
        <<interface>>
        + equipar() : string
    }

    class Guerrero {
        + equipar() : string
    }

    class Espada {
        - personaje : Personaje
        + Espada(Personaje)
        + equipar() : string
    }

    class Escudo {
        - personaje : Personaje
        + Escudo(Personaje)
        + equipar() : string
    }

    Personaje <|.. Guerrero
    Personaje <|.. Espada
    Personaje <|.. Escudo
    Espada o-- Personaje
    Escudo o-- Personaje

