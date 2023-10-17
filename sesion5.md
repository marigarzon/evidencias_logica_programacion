<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 


<!-- Su documentación aquí -->

# Actividad 5: Ejercicios de bucles

### Ejercicios - while
1. Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
```
public class Sesion_5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);
          System.out.print("Por favor, ingresa un número: ");
        int numero = scanner.nextInt();
        
        System.out.println("Tabla de multiplicar del " + numero + ":");
        
        int i = 1;
        while (i <= 10) {
            int resultado = numero * i;
            System.out.println(numero + " x " + i + " = " + resultado);
            i++;
        }
    }
}
```
2. Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

```
public class Sesion_5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);
         
           System.out.print("ingrese una cadena de caracteres: ");
        String cadena = scanner.nextLine();

        int contadorNumeros = 0;
        int i = 0;

        while (i < cadena.length()) {
            char caracter = cadena.charAt(i);
            if (Character.isDigit(caracter)) {
                contadorNumeros++;
            }
            i++;
        }

        System.out.println("La cantidad de caracteres que son números en la cadena es: " + contadorNumeros);
    }
}
```

### Ejercicios - do while
1. Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.

```
public class Sesion_5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);
         
         int numero = 0;

        do {
            System.out.println(numero);
            System.out.print("Ingresa un número (o un número negativo para detener): ");
            numero = scanner.nextInt();
        } while (numero >= 0);
    }
}
```

2. Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

```

public class Sesion_5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);
         
       int numero;

        do {
            System.out.print("Ingresa un número (o 0 para detener): ");
            numero = scanner.nextInt();

            if (numero != 0) {
                System.out.println("Tabla de multiplicar del " + numero + ":");
                for (int i = 1; i <= 10; i++) {
                    int resultado = numero * i;
                    System.out.println(numero + " x " + i + " = " + resultado);
                }
            }
        } while (numero != 0);
    }
}
```

### Ejercicios - for
1. Imprimir los números impares del 1 al 50.

```
public class Sesion_5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);
         
        for (int i = 1; i <= 50; i++) {
            if (i % 2 != 0) {
                System.out.println(i);
            }
        }
    }
}
```

2. Imprimir los números primos del 1 al 100.

```
public class Sesion_5 {

    public static void main(String[] args) {
         Scanner scanner = new Scanner(System.in);
         
            for (int numero = 2; numero <= 100; numero++) {
            boolean esPrimo = true;
            
            for (int divisor = 2; divisor < numero; divisor++) {
                if (numero % divisor == 0) {
                    esPrimo = false;
                    break;
                }
            }

            if (esPrimo) {
                System.out.println(numero);
            }
        }
    }
}
```





