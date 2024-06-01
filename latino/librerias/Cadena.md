
[cadenalibLink]: # (Librería de cadenas en Latino)
[regexLink]: # (RegEx)

# Lib "cadena"

La librería **cadena** nos permite trabajar y manipular las [cadenas (string)](#cadenalibLink) en Latino.

## Lista de comandos

| Comando                 | Parámetros | Descripción                                                              |
|-------------------------|------------|--------------------------------------------------------------------------|
| bytes()                 | 1          | Devuelve el valor ASCII de cada carácter en una lista                    |
| char()                  | 1          | Convierte el valor o lista ASCII a un carácter o una lista de caracteres |
| comparar()              | 2          | Compara dos cadenas de textos y devuelve un valor númerico               |
| concatenar()            | 2          | Combina dos cadenas de textos en una sola cadena                         |
| contiene()              | 2          | Devuelve un valor booleano si encuentra la palabra o cadena especificada  |
| ejecutar()              | 1          | Ejecuta una cadena que tenga código de Latino                            |
| eliminar()              | 2          | Elimina la primera coincidencia en una cadena                             |
| encontrar()             | 2          | Regresa la posición de la primera coincidencia encontrada                 |
| indice()                |            |                                                                          |
| es_alfa()               | 1          | Comprueba si la cadena solo contiene texto y/o números                   |
| es_igual()              | 2          | Regresa verdadero si las dos cadenas son iguales                         |
| es_numerico()           | 1          | Comprueba si la cadena solo contiene números                             |
| esta_vacia()            | 1          | Regresa verdadero si la cadena está vacía                                |
| formato()               | 1          | Asigna un formato a un carácter                                          |
| inicia_con()            | 2          | Comprueba si la cadena inicia con un texto o cadena especificado         |
| insertar()              | 3          | Agrega una cadena en la posición indicada                                |
| invertir()              | 1          | Invierte el contenido de la cadena                                       |
| longitud()              | 1          | Regresa el tamaño de la cadena                                           |
| mayusculas()            | 1          | Convierte toda la cadena en mayúsculas                                   |
| minusculas()            | 1          | Convierte toda la cadena en minúsculas                                   |
| recortar()              | 1          | Elimina los espacios al inicio y al final de la cadena                   |
| reemplazar()            | 4          | Cambia una palabra por otra en una cadena                                |
| regex()                 | 2          | Utiliza RegEx y regresa una lista de las coincidencias                   |
| regexl()                | 2          | Regresa un valor booleano si encuentra la coincidencia                    |
| rellenar_derecha()      | 3          | Agrega n caracteres al final de la cadena especificada                   |
| rellenar_izquierda()    | 3          | Agrega n caracteres al inicio de la cadena especificada                  |
| separar()               | 2          | Separa la cadena en una lista en base a un separador                     |
| subcadena()             | 3          | Devuelve una sub-cadena en base a la posición y su longitud              |
| termina_con()           | 2          | Devuelve un valor booleano si hay una coincidencia                        |
| ultimo_indice()         | 2          | Devuelve la posición final de un carácter o palabra especificada         |

---

### cadena.bytes()

Este comando nos permite **convertir** nuestra **cadena de texto** a `valor ASCII` y la devuelve en una lista.

El comando **cadena.char()** es su contraparte, ya que convierte los valores ASCII a textos.

```latino
x = "Hola mundo"
escribir(cadena.bytes(x))     // Devolverá [72, 111, 108, 97, 32, 109, 117, 110, 100, 111]
```

---

### cadena.char()

Este comando nos permite **convertir** un número o **lista de** `valores ASCII` a una cadena de texto.

El comando **cadena.bytes()** es su contraparte, ya que convierte los textos a valores ASCII.

```latino
x = [72, 111, 108, 97, 32, 109, 117, 110, 100, 111]
escribir(cadena.char(x))     // Devolverá Hola mundo
```

---

### cadena.comparar()

Este comando **compara** dos cadenas de textos **carácter por carácter** hasta encontrar la primera diferencia.

Este comando es similar al comando **strcmp()** en C.

El comando **cadena.comparar()** devuelve los siguientes valores:
  
- -1, si la primera cadena es **menor** que la segunda.
- 0, si ambas cadenas son **iguales**.
- 1, si la primera cadena es **mayor** que la segunda.

**menor**, **igual** o **mayor** hacen referencia al orden o posición de las letras en el alfabeto.

```latino
escribir(cadena.comparar("a", "b"))               // Devolverá -1
escribir(cadena.comparar("a", "a"))               // Devolverá 0
escribir(cadena.comparar("b", "a"))               // Devolverá 1
escribir(cadena.comparar("abeja", "avestruz"))    // Devolverá -1
```

---

### cadena.concatenar()

Este comando nos permite **unir** dos cadenas de textos en una sola.

El comando **cadena.concatenar()** es una alternativa al comando **doble punto (..)**.

```latino
x = "Hola"
y = " mundo"
z = cadena.concatenar(x, y)
escribir(z)     // Devolverá Hola mundo
```

---

### cadena.contiene()

Este comando nos permite **verificar** si existe una **coincidencia** del texto o cadena a buscar en otra y devolverá un valor booleano.

```latino
x = "LenguajeLatino"
y = "Latino"
escribir(cadena.contiene(x, y))     // Devolverá verdadero
```

---

### cadena.ejecutar()

Este comando nos permite **ejecutar** una cadena de texto que tenga código de Latino.

```latino
x = 'escribir("Hola mundo")'     // Almacenamos en una variable el código en Latino como una cadena
cadena.ejecutar(x)               // Devolverá Hola mundo
```

---

## cadena.eliminar( )
---------------------
Este comando solo **elimina la primera coincidencia** encontrada en una cadena de texto.

```latino
x = "Hola mundo, holahola otra vez"
escribir(cadena.eliminar(x, "hola"))     //Devolverá Hola mundo, hola otra vez
```

----

## cadena.encontrar( )
----------------------
Este comando **busca** la posición de la primera coincidencia de caracteres o textos.

Este comando también dispone de un alias **cadena.indice( )**.

El comando **cadena.encontrar( )** cuenta cada carácter de una cadena de texto hasta encontrar la primera coincidencia.

El comando comienza a contar desde el número **cero (0)** como primer número en adelante.

Si el texto o cadena no fue encontrado, entonces devolverá **-1**.

```latino
x = "Hola mundo latino, como estan?"
escribir(cadena.encontrar(x, "como"))     //Devolverá 19
```

----

## cadena.es_alfa( )
--------------------
Este comando **comprueba** si la cadena solo contiene valores **alfanuméricos** y NO símbolos.

El comando **cadena.es_alfa( )** devolverá un valor buleano:

  * **verdadero** si la cadena es letras y/o números.
  * **falso** si la cadena contiene o es un símbolo.

```latino
escribir(cadena.es_alfa("1"))          //Devolverá verdadero
escribir(cadena.es_alfa("a"))          //Devolverá verdadero
escribir(cadena.es_alfa("&"))          //Devolverá falso
escribir(cadena.es_alfa("#"))          //Devolverá falso
escribir(cadena.es_alfa("Hola"))       //Devolverá verdadero
escribir(cadena.es_alfa("Hola++"))     //Devolverá falso
```

----

## cadena.es_igual( )
---------------------
Este comando **comprueba** si ambas cadenas **coinciden entre sí** y regresa un valor buleano.

```latino
escribir(cadena.es_igual("hola", "HOLA"))     //Devolverá falso
escribir(cadena.es_igual("hola", "hola"))     //Devolverá verdadero
```

----

## cadena.es_numero( )
----------------------
Este comando **comprueba** si la cadena **solo contiene números** y devolverá un valor buleano.

Este comando también dispone de un alias **cadena.es_numerico( )**.

```latino
escribir(cadena.es_numerico("123456"))     //Devolverá verdadero
escribir(cadena.es_numerico("1234f"))      //Devolverá falso
escribir(cadena.es_numerico("hola24"))     //Devolverá falso
escribir(cadena.es_numerico("123$%"))      //Devolverá falso
```

----

## cadena.esta_vacia( )
-----------------------
Este comando **verificar** que la cadena está vacía.

El comando **cadena.esta_vacia( )** devolverá un valor buleano:

  * **verdadero** si la cadena esta vacía.
  * **falso** si la cadena NO esta vacía.

```latino
escribir(cadena.esta_vacia(""))      //Devolverá verdadero
escribir(cadena.esta_vacia("a"))     //Devolverá falso
```

----

## cadena.formato( )
--------------------
Este comando permite **dar formato** a un carácter o valor ASCII.

Este comando es similar al comando **imprimirf( )**, aunque este último requiere del carácter **\\n** para poder escribir en pantalla.

El comando **cadena.formato( )** opera con los siguientes formatos:

  * **\%c**, convierte a un carácter el valor ASCII.
  * **\%i**, convierte a un número enteros.
  * **\%f**, convierte a un número decimal.
  * **\%d**, convierte a un número.
  * **\%o**, convierte a un valor octal.
  * **\%x**, convierte a un hexadecimal.
  * **\%e**, convierte a una expresión científica.
  * **\%s**, convierte a carácter o a una cadena de texto.
  * **\%%**, Devuelve el símbolo de **porcentaje (\%)**.

```latino
x = "hola"
escribir(cadena.formato("%c",x))                //Devolverá h
escribir(cadena.formato("%i",x))                //Devolverá 104
escribir(cadena.formato("%f",x))                //Devolverá 104.000000
escribir(cadena.formato("%d",x))                //Devolverá 104
escribir(cadena.formato("%o",x))                //Devolverá 150
escribir(cadena.formato("%x",x))                //Devolverá 68
escribir(cadena.formato("%e",x))                //Devolverá 5.556763e-307
escribir(cadena.formato("%s",x))                //Devolverá hola
escribir(cadena.formato("%%",x))                //Devolverá %
escribir(cadena.formato("%c",75))               //Devolverá K
escribir(cadena.formato("%c%c%c",75,76,77))     //Devolverá KLM
```

----

## cadena.inicia_con( )
-----------------------
A diferencia del comando **cadena.termina_con( )**, este comando **comprueba** si la cadena de texto **inicia con** un carácter especificado, y este devolverá un valor buleano.

Este comando distingue entre **mayúsculas** y **minúsculas**.

```latino
x = "Hola mundo"
escribir(cadena.inicia_con(x, "H"))     //Devolverá verdadero
escribir(cadena.inicia_con(x, "h"))     //Devolverá falso
```

----

## cadena.insertar( )
---------------------
Este comando nos permite **añadir** una cadena a otra cadena de texto en cualquier posición especificada.

La posición se maneja contando cada carácter de la cadena original. Este conteo inicia desde el número **cero (0)** como primer número en adelante.

**Ejemplo de sintaxis**

```bash
cadena.insertar(cadena_original, cadena_a_agregar, la_posición)
```

```latino
x = "Hola mundo, como estan?"
y = " Latino"
escribir(cadena.insertar(x, y, 10))     //Devolverá Hola mundo Latino, como estan?
```

----

## cadena.invertir
---------------------
Este comando nos permite **invertir** el orden de la cadena.

```latino
x = "Hola mundo, como estan?"
escribir(cadena.invertir(x))     //Devolverá ?natse omoc ,odnum aloH
```

cadena.longitud()
---------------------
Este comando retorna la **longitud** de la cadena en dígitos.

El comando comienza a contar desde el número **uno (1)** como primer número en adelante.

```latino
x = "Hola mundo, como estan?"
escribir(cadena.longitud(x))     //Devolverá 23
```

cadena.mayusculas()
-----------------------
Este comando nos permite **transformar** toda nuestra cadena a letras **mayúsculas**.

```latino
x = "hola mundo"
escribir(cadena.mayusculas(x))     //Devolverá HOLA MUNDO
```

cadena.minusculas()
-----------------------
Este comando nos permite **transformar** toda nuestra cadena a letras **minúsculas**.

```latino
x = "HOLA MUNDO"
escribir(cadena.minusculas(x))     //Devolverá hola mundo
```
cadena.recortar()
---------------------
Este comando **elimina** cualquier **carácter de espacio** al inicio y al final de la cadena, ya sea espacio en blanco o tabulación.

```latino
x = "     Hola mundo"
escribir(cadena.recortar(x))     //Devolverá Hola mundo
```
**Error:** Por el momento en Latino 1.2.0 en la librería **cadena**, la función **cadena.recortar()** no funciona correctamente en MS-Windows. Espere a futuros lanzamientos de Latino para ver sus novedades.

----

cadena.reemplazar()
-----------------------
Este comando nos permite **cambiar** una palabra por otra en una cadena.

**Ejemplo de sintaxis**

```bash
(cadena_original, texto_a_reemplazar, texto_nuevo, posición)
```

**Nota:** Este comando cambia el texto seleccionado por el nuevo texto asignado, **mas no lo guarda**. Para guardar el cambio es recomendable asignarlo a una variable.

```latino
x = "Hola mundo HTML"
y = cadena.reemplazar(x, "HTML", "Latino", 12)     //Asignamos en una variable el nuevo texto
escribir(x)                                        //Devolverá Hola mundo HTML
escribir(y)                                        //Devolverá Hola mundo Latino
```

----

cadena.regex()
------------------
Este comando hace uso de las **Expresiones Regulares** o **RegEx** para hacer una **búsqueda avanzada** y retorna una lista con cada una de las coincidencias.

Para aprender más sobre este comando y las expresiones regulares, mire el artículo de RegEx, [aquí](regexLink).

```latino
x = "Hola mundo, Latino"
escribir(cadena.regex(x, "o"))     //Devolverá [["o"], ["o"], ["o"]]
```

----

cadena.regexl()
--------------------
Este comando es conocido como **regex lógico**.

Este comando hace uso de las **Expresiones Regulares** o **RegEx** para hacer una **búsqueda avanzada** y retorna **verdadero** si encuentra la coincidencia y **falso** si no la encontró.

Para aprender más sobre este comando y las expresiones regulares, mire el artículo de RegEx, [aquí](regexLink).

```latino
//Busca si la cadena termina con "Latino"
x = "Hola mundo, Latino"
escribir(cadena.regexl(x, "Latino$"))     //Devolverá verdadero
```

----

cadena.rellenar_derecha()
-----------------------------
Este comando nos permite **añadir al final** de la cadena especificada un texto o cadena.

El comando **cadena.rellenar_derecha()** nos permite indicar la cantidad de veces que deseamos que se repita el nuevo texto a añadir.

**Ejemplo de sintaxis**

```bash
cadena.rellenar_derecha(cadena_original, cadena_a_agregar, long_cadena_original + cantidad_de_repeticiones(Valor numérico))
```

```latino
/*
El no.19 es la longitud de la cadena_original más la cantidad de repeticiones que deseamos,
en este caso indicamos que sean dos veces
*/
x = "Hola mundo, Latino"
y = " que tal?"
escribir(cadena.rellenar_derecha(x,y,19))     //Devolverá Hola mundo, Latino que tal? que tal?
```

----

cadena.rellenar_izquierda()
-------------------------------
Este comando nos permite **añadir al inicio** de la cadena especificada un texto o cadena.

El comando **cadena.rellenar_izquierda()** nos permite indicar la cantidad de veces que deseamos que se repita el nuevo texto a añadir.

**Ejemplo de sintaxis**

```bash
cadena.rellenar_izquierda(cadena_original, cadena_a_agregar, long_cadena_original + cantidad_de_repeticiones(Valor numérico))
```

```latino
/*
El no.14 es la longitud de la cadena_original más la cantidad de repeticiones que deseamos,
en este caso indicamos que sean dos veces
*/
x = "mundo, Latino"
y = "hola "
escribir(cadena.rellenar_izquierda(x,y,14))     //Devolverá hola hola mundo, Latino
```

----

cadena.separar()
--------------------
Este comando nos permite **segmentar** una cadena de texto al especificar un separador y el resultado lo devuelve en una lista.

El separador debe ser especificado **dentro de comillas**.

Si no se le asigna un separador, por defecto buscará los espacios en blanco.

**Ejemplo de sintaxis**

```bash
cadena.separar(cadena_original, separador)
```

```latino
x = "Hola-mundo-Latino-que tal-estan-todos?"
escribir(cadena.separar(x,"-"))     //Devolverá ["Hola","mundo","Latino","que tal","estan","todos?"]
```

----

cadena.subcadena()
----------------------
Este comando **copia** de una cadena el texto deseado el cual se define indicando **en donde inicia** y la **longitud** que deseamos que tenga el texto a copiar.

La **posición_inicial** comienza a contar desde el número **cero (0)** en adelante.

La **longitud** comienza a contar desde el número **uno (1)** en adelante.

**Ejemplo de sintaxis**

```bash
cadena.subcadena(cadena_original, posición_inicial(número), longitud(número))
```

```latino
x = "Hola mundo Latino que tal estan todos?"
escribir(cadena.subcadena(x,5,12))     //Devolverá mundo Latino
```

----

cadena.termina_con()
------------------------
A diferencia del comando **cadena.inicia_con**, este comando nos permite **buscar** en una cadena de texto si esta **termina con** un carácter especificado y devuelve un valor booleano.

Este comando distingue entre **mayúsculas** y **minúsculas**.

```latino
x = "Hola mundo"
escribir(cadena.termina_con(x, "O"))     //Devolverá falso
escribir(cadena.termina_con(x, "o"))     //Devolverá verdadero
```

----

cadena.ultimo_indice()
--------------------------
Este comando devuelve la **última posición encontrada** del carácter especificado.

Este comando comienza a contar desde el número **cero (0)** en adelante.

```latino
x = "Hola mundo"
escribir(cadena.ultimo_indice(x, "u"))     //Devolverá 6
```

Enlaces

- valor ASCII: [ASCII](https://es.wikipedia.org/wiki/ASCII)
- valores ASCII: [ASCII](https://es.wikipedia.org/wiki/ASCII)
```