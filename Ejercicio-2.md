Ejercicio 2:

Patrón Adapter: permite que una clase incompatible trabaje con otras al transformar su interfaz en una interfaz compatible.

```mermaid
classDiagram
    class Windows7 {
        + abrirArchivoWindows7(archivo: string) : string
    }

    class CompatibilidadAdapter {
        - windows7 : Windows7
        + CompatibilidadAdapter(Windows7)
        + abrirArchivo(archivo: string) : string
    }

    class Windows10 {
        + abrirArchivo(archivo: string, adapter: CompatibilidadAdapter) : string
    }

    Windows10 ..> CompatibilidadAdapter
    CompatibilidadAdapter ..> Windows7

