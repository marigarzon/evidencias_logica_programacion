<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 


<!-- Su documentación aquí -->
# Actividad: Ejercicios de Lógica de Programación

1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.


**Ejemplo ejercicio**

```java
public class Ejercicio1 {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2};

        // Creamos una variable para almacenar el número que aparece más de una vez
        int numeroRepetido = 0;

        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            for (int j = 0; j < i; j++) {
                if (numeros[i] == numeros[j]) {
                    // El número actual ya ha aparecido
                    numeroRepetido = numeros[i];
                    break;
                }
            }
        }

        // Si el número repetido es distinto de 0, lo imprimimos
        if (numeroRepetido != 0) {
            System.out.println("El número repetido es: " + numeroRepetido);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```
**Solucion**
```java
import java.util.HashSet;
import java.util.Set;

public class sesion_11 {

    public static void main(String[] args) {
        // Declaramos un conjunto de números enteros
        int[] numeros = {1, 2, 3, 4, 5, 2};

        // Creamos un HashSet para almacenar los números que aparecen más de una vez
        Set<Integer> numerosRepetidos = new HashSet<>();

        // Recorremos el conjunto de números
        for (int i = 0; i < numeros.length; i++) {
            // Comprobamos si el número actual ya ha aparecido
            if (numerosRepetidos.contains(numeros[i])) {
                // El número actual ya ha aparecido
                numerosRepetidos.add(numeros[i]);
            }
        }

        // Si el HashSet de números repetidos no está vacío, lo imprimimos
        if (!numerosRepetidos.isEmpty()) {
            System.out.println("Los números repetidos son: " + numerosRepetidos);
        } else {
            // No hay ningún número repetido
            System.out.println("No hay ningún número repetido");
        }
    }
}
```

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.

```java
public class sesion_11 {
public static void main(String[] args) {
        // Declaramos un número binario
        int numeroBinario = 101;
        // Declaramos una variable para almacenar el número decimal
        int numeroDecimal = 0;
        // Declaramos una variable para almacenar el valor de la posición
        int posicion = 0;
        // Recorremos el número binario
        while (numeroBinario != 0) {
            // Obtenemos el último dígito del número binario
            int ultimoDigito = numeroBinario % 10;
            // Sumamos el valor de la posición
            numeroDecimal += ultimoDigito * Math.pow(2, posicion);
            // Dividimos el número binario entre 10 para eliminar el último dígito
            numeroBinario /= 10;
            // Incrementamos la posición
            posicion++;
        }
        // Imprimimos el número decimal
        System.out.println("El número decimal es: " + numeroDecimal);
    }
}
```
