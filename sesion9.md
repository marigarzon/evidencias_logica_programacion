<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 9 


<!-- Su documentación aquí -->

# Actividad: Ejecicios de métodos en Java

Resolver en parejas el ejercicio asignado por el docente

```java
//CALCULADORA DE RESISTENCIAS ELECTRICAS, el resultado no se da en 4700 ohmios sino en 4.7k (200000 Ohms --> 200k), ya si es menor de 1000 se pone en omnios, las dos primeras franjas solo toma valores (entre 0 -9), la tercera franja es un multplicador, la cuarta franja es la presicion de la resistencia.

import java.util.Scanner;

public class Ejercicio1{
    public static void main(String[] args) {
        System.out.println("============== BANDA DE COLOR 1 ==================");
        int color1 = menu1();
        System.out.print("El color seleccionado es: ");
        System.out.println(color1);
        System.out.println("================================================");
    
        System.out.println("============== BANDA DE COLOR 2 ==================");
        int color2 = menu1();
        System.out.print("El color seleccionado es: ");
        System.out.println(color2);
        System.out.println("================================================");

        System.out.println("============== MULTIPLICADOR ==================");
        int color3 = menu1();
        System.out.print("El color seleccionado es: ");
        System.out.println(color3);
        System.out.println("================================================");

        int v1 = color1;
        int v2 = color2;
        int v3 = color3;

        int v4 = (v1 *10) + v2;

        double mult=0;
        // Aqui verifica el multiplicador
        if (v3 == 0) {
            mult = v4 *1;
        }else if (v3 == 1) {
            mult = v4 * 10;
        }else if (v3 == 2) {
            mult = v4 * 100;
        }else if (v3 == 3) {
            mult = v4 * 1000;
        }else if (v3 == 4) {
            mult = v4 * 10000;
        }else if (v3 == 5) {
            mult = v4 * 100000;
        }else if (v3 == 6) {
            mult = v4 * 1000000;
        }else if (v3 == 7) {
            mult = v4 /10;
        }else if (v3 == 8) {
            mult = v4 /100;
        } else {
            System.out.println("");
        }
        // System.out.println(v4);
        String resultadoFormateado = formatearResultado(mult);
        System.out.println("Valor de la Resistencia: " + resultadoFormateado + " "+menu2());
    
    
    }

    public static int menu1(){ // este menu sirve para las tres primeras fases 
        Scanner input = new Scanner (System.in);
        System.out.println("0 - Negro");
        System.out.println("1 - Marrón");
        System.out.println("2 - Rojo");
        System.out.println("3 - Naranja");
        System.out.println("4 - Amarillo");
        System.out.println("5 - Verde");
        System.out.println("6 - Azul");
        System.out.println("7 - Morado");
        System.out.println("8 - Gris");
        System.out.println("9 - Blanco");
        System.out.print("Seleccione un color: ");
        int color = input.nextInt();
        // input.close();
        return color; 
    }

    public static String menu2(){ 
        Scanner input1 = new Scanner (System.in);
        System.out.println("Marrón +/- 1%"); 
        System.out.println("Rojo +/- 2%"); 
        System.out.println("Oro +/- 5%"); 
        System.out.println("Plata +/- 10%"); 
        System.out.print("Seleccione un color: ");
        
       String color2 = input1.nextLine();
        if (color2.equals("Marrón")) {
            return "Marrón +/- 1%";
        } else if (color2.equals("Rojo")) {
            return "Rojo +/- 2%";
        } else if (color2.equals("Oro")) {
            return "Oro +/- 5%";
        } else if (color2.equals("Plata")) {
            return "Plata +/- 10%";
        } else {
            return "Color no reconocido";
        }
       
    }

    public static String formatearResultado(double resultado) {
        if (resultado >= 1000) {
            // Si es mayor o igual a 1000, dividir por 1000 y agregar "K"
            return (resultado / 1000) + " K";
        } else {
            // De lo contrario, dejar el resultado tal como está
            return String.valueOf(resultado +" Ohms");
        }
    }
}
```




