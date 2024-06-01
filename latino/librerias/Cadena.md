
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

