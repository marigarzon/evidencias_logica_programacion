<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4


<!-- Su documentación aquí -->

# Actividad 4: Ejercicios de control de flujo con expresiones compuestas


```
// Variables de tipo String
String nombre = "Juan Pérez";
String apellido = "González";
String identificación = "1000000001";
String correo = "juan.perez@ejemplo.com";
String carrera = "Desarrollo de Software";
String universidad = "Cesde";
// Variable de tipo int
int edad = 20;
// Variable de tipo boolean
boolean esActivo = true;
boolean becado = false;
// Variable de tipo char
char género = 'M';
// Variable de tipo double
double promedio = 4.5;
// Variable de tipo int
int semestre = 2;
```

Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
- 0.0 - 3.4: El estudiante no recibe beca.
- 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
- 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
- 4.5 - 5.0: El estudiante recibe una beca completa.


## 1
```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
          if (edad >= 18 && esActivo) {
            System.out.println("El estudiante " + nombre + " es mayor de edad y tiene un estado activo.");
        } else {
            System.out.println("El estudiante " + nombre + " no es mayor de edad o no tiene un estado activo.");
        }
          

    }
}
```

## 2
```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
           if (becado || carrera.equals("Desarrollo de Software")) {
            System.out.println("El estudiante tiene una beca o una carrera relacionada con el desarrollo de software.");
        } else {
            System.out.println("El estudiante no tiene una beca ni una carrera relacionada con el desarrollo de software.");
          
           }
    }
}
```

## 3
```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
          if (semestre == 10 && esActivo) {
            System.out.println("El estudiante está en el último semestre de su carrera y tiene un estado activo.");
        } else {
            System.out.println("El estudiante no está en el último semestre de su carrera o no tiene un estado activo.");
        }
    }
}
```

## 4
```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
   if (carrera.equals("Desarrollo de Software") && promedio > 4.0) {
            System.out.println("El estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.");
        } else {
            System.out.println("El estudiante no cumple con los requisitos.");
        }
    }
}
```

## 5

```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
      if (universidad.equals("Cesde")) {
            System.out.println("Toda la información del estudiante:");
            System.out.println("Nombre: " + nombre);
            System.out.println("Edad: " + edad);
            System.out.println("Activo: " + esActivo);
            System.out.println("Becado: " + becado);
            System.out.println("Carrera: " + carrera);
            System.out.println("Promedio: " + promedio);
        } else {
            System.out.println("El estudiante no está matriculado en el Cesde.");
        }
    }
}
```
## 6

```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
     if (universidad.equals("Cesde")) {
            System.out.println("Toda la información del estudiante:");
            System.out.println("Nombre: " + nombre);
            System.out.println("Edad: " + edad);
            System.out.println("Activo: " + esActivo);
            System.out.println("Becado: " + becado);
            System.out.println("Carrera: " + carrera);
            System.out.println("Promedio: " + promedio);
        } else {
            System.out.println("El estudiante no está matriculado en el Cesde.");
        }
    }
}
```

## 7
```
public class Mariana_sesion4 {

    public static void main(String[] args) {
     
       Scanner scanner = new Scanner(System.in);

       String nombre = "Juan Pérez";
        String apellido = "González";
        String identificacion = "1000000001";
        String correo = "juan.perez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";
        int edad = 20;
        boolean esActivo = true;
        boolean becado = false;
        char genero = 'M';
        double promedio = 4.5;
        int semestre = 2;
        
    
        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca.");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            System.out.println("El estudiante recibe una beca parcial del 25%.");
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            System.out.println("El estudiante recibe una beca parcial del 50%.");
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            System.out.println("El estudiante recibe una beca completa.");
        }
    }
}
```
























 <!-- // Solicitar al usuario ingresar el promedio académico del estudiante
        System.out.print("Ingresa el promedio académico del estudiante: ");
        double promedio = scanner.nextDouble();

        double montoBeca = 0.0; // Inicializamos el monto de beca en 0 por defecto

        // Determinar la cantidad de beca según el rango de promedio
        if (promedio >= 0.0 && promedio <= 3.4) {
            System.out.println("El estudiante no recibe beca.");
        } else if (promedio >= 3.5 && promedio <= 3.9) {
            montoBeca = 0.25 * promedio; // Beca del 25%
            System.out.println("El estudiante recibe una beca parcial del 25%.");
            System.out.println("Monto de la beca: " + montoBeca);
        } else if (promedio >= 4.0 && promedio <= 4.4) {
            montoBeca = 0.5 * promedio; // Beca del 50%
            System.out.println("El estudiante recibe una beca parcial del 50%.");
            System.out.println("Monto de la beca: " + montoBeca);
        } else if (promedio >= 4.5 && promedio <= 5.0) {
            montoBeca = promedio; // Beca completa
            System.out.println("El estudiante recibe una beca completa.");
            System.out.println("Monto de la beca: " + montoBeca);
        } else {
            System.out.println("El promedio ingresado no es válido.");
        } -->