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






