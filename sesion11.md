<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 11 

# Actividad: Ejercicios de Lógica de Programación

1. Basándose en el algoritmo 1 de la sesión 11, aplicar la siguiente variante: Dado un conjunto de números enteros, se debe determinar si existe algún número que aparezca más de una vez. Si es así, se deben imprimir todos los números que aparezcan más de una vez.

2. Desarrollar un algoritmo que realice la conversión de binario a decimal.

# SOLUCIÓN...

import java.util.Scanner;


public class Sesion11 {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        System.out.print("Ingresa un número binario: ");
        String binario = input.nextLine();

        int decimal = binarioADecimal(binario);

        System.out.println("El número decimal equivalente es: " + decimal);
    }

    public static int binarioADecimal(String binario) {
        int decimal = 0;
        int longitud = binario.length();

        for (int i = 0; i < longitud; i++) {
            char digito = binario.charAt(i);
            int valor = Character.getNumericValue(digito);
            int potencia = (int) Math.pow(2, longitud - 1 - i);
            decimal += valor * potencia;
        }

        return decimal;
    }
}








