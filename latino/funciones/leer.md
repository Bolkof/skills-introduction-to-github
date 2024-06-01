
[leer( )](#leerlink)
=====================

La función **leer( )** escanea las teclas numéricas y alfanuméricas digitadas por el usuario, hasta que este presione la tecla **enter**.

Es recomendable asignar este comando a una variable, ya que se puede manipular con mayor facilidad cualquier dato digitado por el usuario.

```bash
   leer()
```

**Ejemplo de función**

```latino
escribir("¿Cuál es su nombre?")
x = leer()
escribir("Hola "..x)     //Devolverá "Hola (Más el nombre del usuario)"
```
