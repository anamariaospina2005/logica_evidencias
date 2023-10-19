<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 8 

# Actividad: Ejecicios de métodos en Java

Implementar los siguientes métodos:

1. Escribe un método que reciba dos números como parámetros y devuelva el mayor de los dos.
2. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de vocales que contiene.
3. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las letras mayúsculas en minúsculas y viceversa.
4. Escribe un método que reciba una cadena de texto como parámetro y devuelva el número de palabras que contiene.
5. Escribe un método que reciba una cadena de texto como parámetro y devuelva una nueva cadena con todas las palabras en orden alfabético.

# SOLUCIÓN...

1. public class Sesion8 {

    public static int obtenerMayor(int numero1, int numero2) {
        if (numero1 > numero2) {
            return numero1;
        } else {
            return numero2;
        }
    }

    public static void main(String[] args) {
        int num1 = 10;
        int num2 = 20;
        int resultado = obtenerMayor(num1, num2);
        System.out.println("El número mayor entre " + num1 + " y " + num2 + " es: " + resultado);
    }
}

2. import java.util.Scanner;

public class Sesion8 {

    public static int contarVocales(String texto) {
        int contador = 0;
        texto = texto.toLowerCase(); 

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (caracter == 'a' || caracter == 'e' || caracter == 'i' || caracter == 'o' || caracter == 'u') {
                contador++;
            }
        }

        return contador;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese una cadena de texto: ");
        String texto = scanner.nextLine();

        int resultado = contarVocales(texto);
        System.out.println("El número de vocales en la cadena es: " + resultado);

        scanner.close();
    }
}

3. import java.util.Scanner;

public class Sesion8 {

    public static String cambiarMayusculasMinisculas(String texto) {
        StringBuilder resultado = new StringBuilder();

        for (int i = 0; i < texto.length(); i++) {
            char caracter = texto.charAt(i);
            if (Character.isUpperCase(caracter)) {
                resultado.append(Character.toLowerCase(caracter));
            } else if (Character.isLowerCase(caracter)) {
                resultado.append(Character.toUpperCase(caracter));
            } else {
                resultado.append(caracter);
            }
        }

        return resultado.toString();
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese una cadena de texto: ");
        String texto = scanner.nextLine();

        String resultado = cambiarMayusculasMinisculas(texto);
        System.out.println("Texto con mayúsculas y minúsculas intercambiadas: " + resultado);

        scanner.close();
    }
}

4. import java.util.Scanner;

public class Sesion8 {

    public static int contarPalabras(String texto) {
        if (texto == null || texto.isEmpty()) {
            return 0;
        }

        String[] palabras = texto.split("\\s+");
        return palabras.length;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Ingrese una cadena de texto: ");
        String texto = scanner.nextLine();

        int resultado = contarPalabras(texto);
        System.out.println("El número de palabras en la cadena es: " + resultado);

        scanner.close();
    }
}





