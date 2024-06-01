
[Lib "archivo"](archivo)
=========================

La librería **archivo** contiene las funciones principales para el manejo de archivos en Latino.

Cada uno de estos comandos puede recibir el **nombre** como también la **ruta** del archivo.

El nombre de archivo o ruta del archivo deben ser escritas entre **comillas**.

**Lista de comando**

| Comando        | Parámetros | Descripción                                             |
|----------------|------------|---------------------------------------------------------|
| anexar\( \ )   | 2          | Agrega un texto o dato al final del archivo             |
| borrar\( \)    | 1          | Elimina el archivo especificado                         |
| eliminar\( \)  |            |                                                         |
| crear\( \)     | 1          | Crea un archivo con el nombre especificado              |
| duplicar\( \)  | 2          | Hace un duplicado del archivo especificado              |
| ejecutar\( \)  | 1          | Ejecuta el archivo especificado                         |
| escribir\( \)  | 2          | Escribe y/o Sobrescribe en el archivo                   |
| leer\( \)      | 1          | Lee el contenido de un archivo y lo convierte en cadena |
| lineas\( \)    | 1          | Almacena en una lista cada línea del archivo            |
| renombrar\( \) | 2          | Renombra un archivo por un nuevo nombre asignado        |

----

**archivo.anexar( )**
----------------------
Este comando nos permite **agregar** texto al final del documento especificado.

A diferencia del comando `archivo.escribir( )` que sobrescribe los datos existentes en el documento, el comando **archivo.anexar( )** añade el texto al final del documento.

```latino
archivo.anexar("c:\\user\\prueba.lat", ", Latino\n\nHoy será un hermoso día.")
```

----

**archivo.duplicar( )**
------------------------
Este comando crea un **duplicado** de un archivo especificado.

**Ejemplo de sintaxis**

```bash
archivo.duplicar("archivo_Original", "archivo_Copia")
```

```latino
archivo.duplicar("c:\\user\\prueba.lat", "c:\\user\\desktop\\hola.lat")
```

----

**archivo.crear( )**
-------------------
Este comando nos permite **crear un archivo** con un nombre especificado en cualquier ruta de nuestro sistema.

```latino
archivo.crear("C:\\Users\\prueba.lat")
```

Nota: Si al especificar la ruta del archivo a crear escribimos un nombre de alguna carpeta que no existe, este no hará nada, ya que este comando solo puede crear archivos y no carpetas.

----

**archivo.ejecutar( )**
----------------------
Este comando nos permite la **ejecución** de un archivo que contenga código de Latino.

```latino
archivo.ejecutar("c:\\user\\prueba.lat")
```

----

**archivo.eliminar( )**
----------------------
Este comando nos ayuda a **eliminar** un archivo especificado.

```latino
archivo.eliminar("c:\\user\\prueba.lat")
```

----

**archivo.escribir( )**
-----------------------
Este comando nos permite **escribir** y **sobrescribe** un archivo especificado.

Si deseamos añadir más información al archivo usar el comando `archivo.anexar( )`.

Si se usa este comando en un archivo **NO vacío** este será completamente **sobrescrito** con la nueva información.

```latino
archivo.escribir("c:\\user\\prueba.lat", "Hola mundo")
```

----

**archivo.leer( )**
------------------
Para este comando se requiere **almacenar en una variable** el contenido del archivo que deseamos leer.

```latino
x = archivo.leer("C:\\Users\\prueba.lat")
escribir(x)
```

----

**archivo.lineas( )**
---------------------
Este comando almacena en una **lista** cada línea de código de un archivo especificado.

Para este comando es requerido asignarlo a una variable para almacenar el contenido del archivo.

```latino
x = archivo.lineas("C:\\Users\\prueba.lat")
escribir(x)
```

----

**archivo.renombrar( )**
------------------------
Este comando nos permite **renombrar** el nombre de un archivo.

Este comando también admite rutas.

**Ejecuta de sintaxis**

```bash
archivo.renombrar(Nombre_viejo, Nombre_nuevo)
```

```latino
archivo.renombrar("hola.lat", "queTal.lat")     // Renombrará el archivo por queTal.lat
```
