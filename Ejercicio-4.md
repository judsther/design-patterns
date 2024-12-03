Ejercicio 4:

Patrón Strategy: permite definir un conjunto de algoritmos y seleccionarlos en tiempo de ejecución.

```mermaid
classDiagram
    class MostrarSalida {
        <<interface>>
        + mostrar(mensaje: string)
    }

    class Consola {
        + mostrar(mensaje: string)
    }

    class JSON {
        + mostrar(mensaje: string)
    }

    class TXT {
        + mostrar(mensaje: string)
    }

    class Mensaje {
        - estrategia : MostrarSalida
        + Mensaje(MostrarSalida)
        + enviar(mensaje: string)
    }

    MostrarSalida <|.. Consola
    MostrarSalida <|.. JSON
    MostrarSalida <|.. TXT
    Mensaje o-- MostrarSalida
