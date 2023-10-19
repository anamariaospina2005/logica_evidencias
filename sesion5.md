<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 5 

# Actividad 5: Ejercicios de bucles

## Resolver los siguientes ejercicios:

### Ejercicios - while
Pedir al usuario que ingrese un número y mostrar su tabla de multiplicar hasta el número 10.
Pedir al usuario que ingrese una cadena de caracteres y contar la cantidad de caracteres que son números.

### Ejercicios - do while
Escribe un programa en Java que imprima los números del 1 al 100, pero que se detenga si el usuario introduce un número negativo.
Escribe un programa en Java que pida al usuario un número entero e imprima la tabla de multiplicar de ese número, pero que se detenga si el usuario introduce el número 0.

### Ejercicios - for
Imprimir los números impares del 1 al 50.
Imprimir los números primos del 1 al 100.

# SOLUCIÓN...

## PRIMER EJERCICIO...

### Ejercicios - while

import java.util.Scanner;
/**
 *
 * @author Ana
 */
public class Actvdad5 {

    public static void main(String[] args) {
     Scanner scanner = new Scanner(System.in);
        
    System.out.println("Ingresa un numero");
    int n1 = scanner.nextInt();
    int x = 0;
    
    while (x <=10) {
        int mult = n1 * x;
        System.out.println(n1 + " x " + x + " = " + mult);
        x++;
    }

    }
}

## SEGUNDO EJERCICIO...

import java.util.Scanner;

/**
 *
 * @author Ana 
 */
public class Ejercicio2While {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("");
        String texto = sc.nextLine();
        int x = 0;
        int contador = 0;

        while (x < texto.length()) {
            char caracter = texto.charAt(x);
            {
                if (caracter == '1' || caracter == '2' || caracter == '3' || caracter == '4' || caracter == '5' || caracter == '6' || caracter == '7' || caracter == '8' || caracter == '9' || caracter == '0') {
                    contador++;
                }
            }
            x++;
        }

        System.out.println("Los caracteres ingresados contienen " + contador + " números");

    }
}

## PRIMER EJERCICIO ...

### Ejercicios - do while

import java.util.Scanner;
/**
 *
 * @author Ana 
 */
public class Ejercicio1dowhile {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int numero;

        do {
            System.out.println("Ingrese un numero (o numero negativo para detener): ");
            numero = sc.nextInt(); 
            
            while (numero >=0 && numero <= 99) {
                numero+=1;
                System.out.println("Numero: " + numero);
            }
            
         } while (numero >= 0);
        
        System.out.println("Detener");
      
    }
}

## SEGUNDO EJERCICIO...

import java.util.Scanner;
/**
 *
 * @author Ana 
 */
public class Ejercicio2dowhile {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int numero;

        do {
            System.out.println("Ingrese un número entero (0 para salir): ");
            numero = scanner.nextInt();

            if (numero != 0) {
                System.out.println("Tabla de multiplicar del numero " + numero + ":");
                for (int i = 1; i <= 10; i++) {
                    System.out.println(numero + "x" + i + "=" + (numero * i));
                }
                System.out.println();
            }
        } while (numero != 0);
        System.out.println("Se finalizo el programa");

    }
}

## PRIMER EJERCICIO...

### Ejercicios - for

public class Ejercicio1for {

    public static void main(String[] args) {
       
 
        for (int n = 1; n <= 50; n += 2) {
            System.out.println("Numeros impares " + n);
            
        }
       }
    }

## SEGUNDO EJERCICIO...

public class Ejercicio2for {

    public static void main(String[] args) {
        boolean Primo;
        System.out.println("Números primos del 1 al 100 ");
        
        for (int num = 2; num <= 100; num++) {
            Primo = true;
            for (int i = num - 1; i > 1; i--) {
                if (num % i == 0) {
                    Primo = false;
                    break;
                }
            }
            if (Primo) {
                System.out.println(num);
            }
        }
    }
}





