<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 7 


<!-- Su documentación aquí -->

# Actividad: Ejecicios Array - ArrayList

## 1. En parejas, probar, analizar y explicar el funcionamiento de los siguientes ejemplos de Array y ArrayList.

**Ejemplo Array**

```
import java.util.Arrays;

public class EjercicioArray {

    public static void main(String[] args) {
        // Crear un array de números enteros
        int[] numeros = {5, 2, 10, 7, 1};

        // Imprimir el array original
        System.out.println("Array original: " + Arrays.toString(numeros));

        // Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) {
            suma += numeros[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        // Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
    }
}
```

El codigo java realiza 2 tareas:

```
// Calcular la suma de los elementos del array
        int suma = 0;
        for (int i = 0; i < numeros.length; i++) 
            suma += numeros[i];
```

Imprime el contenido de un array llamado números.
Calcula la suma de los elementos en esa matriz y luego imprime el resultado de la suma.

Esta línea imprime el contenido del array números. Utiliza Arrays.toString(números)para convertir el array en una cadena de caracteres legibles que muestra todos los elementos del array. La salida será algo como:
Luego, el código procede a calcular la suma de los elementos en el array:

```
 // Encontrar el número más grande en el array
        int maximo = numeros[0];
        for (int i = 1; i < numeros.length; i++) {
            if (numeros[i] > maximo) {
                maximo = numeros[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);
```

El código funciona recorriendo un array para comparar cada iteración con una variable llamada máximo para así poder mantener un registro del número más grande que se encuentra hasta el momento.
En resumen, este código es una forma válida de encontrar el número más grande en un array en Java y funcionará correctamente siempre que el array contenga al menos un elemento.

```
// Ordenar el array en orden ascendente
        Arrays.sort(numeros);
        System.out.println("Array ordenado: " + Arrays.toString(numeros));
```

Este código se utiliza para ordenar el array numeros en orden ascendente, para luego imprimir el resultado ordenado  

**Ejemlo Arraylist**

```
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas {

  public static void main(String[] args) {

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }

  }

  public static void agregarNota(ArrayList<String> notas, Scanner scan) {
    
    System.out.println("Ingrese el titulo de la nota:");
    String titulo = scan.nextLine();
    
    System.out.println("Ingrese el contenido de la nota:");
    String contenido = scan.nextLine();
    
    notas.add(titulo + " - " + contenido);

  }

  public static void mostrarNotas(ArrayList<String> notas) {

    for(String n : notas) {
      System.out.println(n);
    }

  }

}
```

**Descripcion**

```
import java.util.ArrayList; 
import java.util.Scanner;

public class AppNotas 

  public static void main(String[] args) 

    ArrayList<String> notas = new ArrayList<>();
    
    Scanner scan = new Scanner(System.in);

    while(true) {

      System.out.println("1. Agregar nota");  
      System.out.println("2. Mostrar notas");
      System.out.println("3. Salir");

      int opcion = scan.nextInt();

      if (opcion == 1) {
        agregarNota(notas, scan);  
      } else if (opcion == 2) {
        mostrarNotas(notas);
      } else {
        break;
      }

    }
```

 El  ArrayList llamado `notas` es para almacenar las notas. Cada elemento del ArrayList es una cadena de caracteres que contiene el título y el contenido de una nota.
Se inicia un bucle `while(true)` que se ejecutará continuamente hasta que el usuario seleccione la opción "Salir" (opción 3).
 En cada iteración del bucle, se muestra un menú con tres opciones: "Agregar nota" (opción 1), "Mostrar notas" (opción 2) y "Salir" (opción 3).
Se utiliza `scan.nextInt()` para leer la opción elegida por el usuario.
Si el usuario elige la opción 1 ("Agregar nota"), se llama a la función `agregarNota()` para ingresar el título y el contenido de la nota y luego se agrega la nota al ArrayList `notas`.
Si el usuario elige la opción 2 ("Mostrar notas"), se llama a la función `mostrarNotas()` para mostrar todas las notas almacenadas en el ArrayList.
 Si el usuario elige la opción 3 ("Salir"), el bucle `while` se interrumpe y el programa finaliza.

Las funciones `agregarNota()` y `mostrarNotas()` son simples. `agregarNota()` permite al usuario ingresar el título y el contenido de la nota y luego agrega una cadena formateada al ArrayList `notas`. `mostrarNotas()` itera a través de todas las notas almacenadas en `notas` e imprime cada una de ellas.


## Ejercicio Array

```
public class Sesion7 {

    public static void main(String[] args) {
        
        int[] datos = {8, 2, 10, 6, 9, 12, 4, 3};

        
        System.out.println("Array original: " + Arrays.toString(datos));

        
        int suma = 0;
        for (int i = 0; i < datos.length; i++) {
            suma += datos[i];
        }
        System.out.println("La suma de los elementos es: " + suma);

        
        int maximo = datos[0];
        for (int i = 1; i < datos.length; i++) {
            if (datos[i] > maximo) {
                maximo = datos[i];
            }
        }
        System.out.println("El número más grande es: " + maximo);

        
        Arrays.sort(datos);
        System.out.println("Array ordenado: " + Arrays.toString(datos));
    }
}

```




