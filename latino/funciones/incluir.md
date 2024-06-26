
[incluirLink](#incluirLink)

# Función incluir( )

La función **incluir( )** nos permite importar **módulos** y **librerías** a nuestro proyecto.

Cuando escribimos el módulo o librería, este debe ser escrito entre **comillas** y no es necesario escribir su extensión.

## Ejemplo de sintaxis

```latino
incluir("librería")              // No requieren una variable
variable = incluir("módulo")     // Requieren ser asignadas a una variable
```

**Nota:** Esta función solo puede incluir archivos con extensión **.lat** o archivos de librerías que hayan sido escritas para Latino y que usen su API.

---

## Subdirectorio

Con el comando **incluir( )**, para especificar archivos en subdirectorios varía dependiendo del sistema operativo.

En MS-Windows, para especificar un archivo en un subdirectorio usamos **\\**.

En Linux y Mac, para especificar un archivo en un subdirectorio usamos **/**.

**Ejemplo**

Para añadir un archivo del siguiente subdirectorio **carpeta/modulo** lo especificamos de la siguiente manera:

```bash
incluir("carpeta\modulo")     // MS-Windows
incluir("carpeta/modulo")     // Unix
```

## Incluir librerías

Una [librería](https://es.wikipedia.org/wiki/Biblioteca_(informática)) es un conjunto de módulos que nos proporciona una serie de funciones/métodos muy concretos que nos ayudan a simplificar tareas complejas y no perjudica la estructura de nuestro código.

A diferencia de los módulos en Latino, las librerías no requieren ser almacenadas en una variable.
