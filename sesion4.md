<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 4

# Actividad 4: Ejercicios de control de flujo con expresiones compuesta

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

Con la información anterior, implementa los siguientes ejercicios:

1. Determinar si el estudiante es mayor de edad y tiene un estado activo.
2. Determinar si el estudiante tiene una beca o una carrera relacionada con el desarrollo de software.
3. Determinar si el estudiante está en el último semestre de su carrera y tiene un estado activo.
4. Determinar si el estudiante tiene una carrera relacionada con el desarrollo de software y un promedio superior a 4.0.
5. Mostrar toda la información del estudiante si está matriculado en el Cesde.
6. Asignar una beca del 50% si el estudiante está matriculado en el Cesde, tiene un promedio superior a 4.0 y está activo.
7. Determinar la cantidad de beca que recibe el estudiante según su promedio:
° 0.0 - 3.4: El estudiante no recibe beca.
° 3.5 - 3.9: El estudiante recibe una beca parcial del 25%.
° 4.0 - 4.4: El estudiante recibe una beca parcial del 50%.
° 4.5 - 5.0: El estudiante recibe una beca completa.


# SOLUCIÓN... 


 * @author Juan Y Ana
 */
 
public class Ejer4 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String nombre = "Pepito Amador";
        String apellido = "ALvarez";
        String identificación = "1000000001";
        String correo = "pepito.alvarez@ejemplo.com";
        String carrera = "Desarrollo de Software";
        String universidad = "Cesde";

        int edad = 20;

        boolean esActivo = true;
        boolean tieneBeca = false;

        char género = 'M';

        double promedio = 4.5;

        int semestre = 2;

        System.out.println("Ejercicio ------------------------------------");
        System.out.println("Ejercicio 1");

        if (edad >= 18 && esActivo) {
            System.out.println("Es mayor de edad y esta activo");
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 2");

        System.out.println("El estudiante estudia " + carrera);

        if (tieneBeca) {
            System.out.println("El estudiante tiene una beca.");
        } else {
            System.out.println("El estudiante no tiene una beca");
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 3");

        if (semestre == 2 && esActivo) {
            System.out.println("El estudiante  no está en el último semestre de su carrera y esta activo.");
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 4");

        if (carrera == "Desarrollo de Software") {
            System.out.println("Tienes una carrera relacionada con desarrollo de Sotfware");

        }
        if (promedio >= 4.0) {
            System.out.println("Tienes un promedio superior a 4");
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 5");

        if (universidad == "Cesde") {
            System.out.println("Informacion del estudiante");
            System.out.println(nombre);
            System.out.println(apellido);
            System.out.println(identificación);
            System.out.println(correo);
            System.out.println(carrera);
            System.out.println(universidad);
            System.out.println(edad);
            System.out.println(esActivo);
            System.out.println(tieneBeca);
            System.out.println(género);
            System.out.println(promedio);
            System.out.println(semestre);
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 6");

        if (universidad == "Cesde" && promedio >= 4.1 && esActivo) {

            System.out.println("Tienes una beca del 50%");
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 7");

        if (promedio >= 4.5) {
            System.out.println("Tienes una beca completa para estudiar tu carrera en desarrollo");
        }

        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 8");

        System.out.println("Ingresa tu nombre completo");
        String nombrecompleto = scanner.nextLine();
        
        
        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 9");
        
        System.out.println("Ingrese la edad");
        int eda = scanner.nextInt();
    
        System.out.println("Ejercicio ----------------------------------------");
        System.out.println("Ejercicio 10");

        System.out.println("Ingresar las notas de 1 a 5 para sacar el promedio");

        System.out.print("ingrese la primera nota:");
        double n1 = scanner.nextDouble();
        System.out.print("ingrese la segundo nota:");
        double n2 = scanner.nextDouble();
        System.out.print("ingrese la tercera nota:");
        double n3 = scanner.nextDouble();
        System.out.print("ingrese la cuarta nota:");
        double n4 = scanner.nextDouble();

        double Resultado = (n1 + n2 + n3 + n4) / 4;
        System.out.print("el resultado del promedio de 4 notas es:" + Resultado);

        if (Resultado >= 3.0) {
            System.out.print(" El estudiante aprobo");

        } else {
            System.out.print(" El estudiante desaprobo");
        }

    }

}







