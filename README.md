```Ejercicio 1:


classDiagram
    class Personaje {
        +atacar() : string
        +velocidad() : string
    }

    class Esqueleto {
        +atacar() : string
        +velocidad() : string
    }

    class Zombi {
        +atacar() : string
        +velocidad() : string
    }

    class FabricaDePersonajes {
        +crearPersonaje(nivel) : Personaje
    }

    Personaje <|-- Esqueleto
    Personaje <|-- Zombi
    FabricaDePersonajes ..> Personaje
