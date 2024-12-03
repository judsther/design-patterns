Ejercicio 1:

Patrón Factory: El patrón Factory se utiliza para delegar la creación de objetos a una clase específica. Podriamos decir que es una clase principal que 'fabrica' a los demás objetos.

```mermaid
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


