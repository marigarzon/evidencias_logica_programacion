<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


<!-- Su documentación aquí -->
# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

```java
import java.util.Scanner;

class Main{
  public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);
    
    System.out.print("Ingresar datos separados por comas: "); 
    String input = scanner.nextLine();
    
    String[] dataStr = input.split(","); 
    double[] data = new double[dataStr.length];
    
    for (int i = 0; i < dataStr.length; i++) {
       data[i] = Double.parseDouble(dataStr[i]);
    }
      
    int n = data.length;  
    double mean = 0, sum = 0, standardDeviation = 0;
      
    // Calcula la media aritmética   
    for (double num : data) {   
       sum += num;
    } 
    mean = sum / n;
      
    // Calcula la varianza      
    for (double num : data) {
         standardDeviation += Math.pow(num - mean, 2);       
     }
     standardDeviation /= n - 1;    
     standardDeviation = Math.sqrt(standardDeviation);  
     
     System.out.println("Mean = " + mean);     
     System.out.println("Standard deviation = " + standardDeviation);
  }  
}
```
La función de este código es calcular la media y la desviación estándar de un conjunto de números ingresados por el usuario. Estos cálculos son estadísticos y proporcionan información sobre la tendencia central y la dispersión de los valores ingresados. La media aritmética representa la tendencia central al calcular el promedio de los valores, mientras que la desviación estándar mide cuán dispersos están los valores en relación con la media.

 el propósito de este código es realizar análisis estadísticos simples de un conjunto de datos ingresados por el usuario para proporcionar información sobre cómo están distribuidos estos datos.


