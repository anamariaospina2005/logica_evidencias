<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 3 

# Actividad 3: Ejercicios de operaciones básicas en Java.

1. Suma y multiplicación: Escribe un programa que solicite al usuario dos números enteros y luego imprima la suma y multiplicación de esos números.

2. Resta y división: Escribe un programa que tome dos números enteros ingresados por el usuario y calcule la resta y división de esos números.

3. Operaciones combinadas: Escribe un programa que solicite al usuario tres números enteros y realice las siguientes operaciones: suma de los tres números, multiplicación del primer número por el segundo y división del resultado entre el tercer número.

4. Operaciones con decimales: Escribe un programa que solicite al usuario dos números decimales y realice las siguientes operaciones: suma, resta, multiplicación y división.

5. Incremento y decremento: Escribe un programa que declare una variable entera y la inicialice con un valor. Luego, incrementa su valor en 1 y muestra el resultado. Después, decrementa su valor en 1 y muestra el resultado nuevamente.

6. Operador de asignación compuesta: Escribe un programa que declare una variable entera y la inicialice con un valor. Utiliza el operador de asignación compuesta para sumar 5 a la variable y luego mostrar su valor.

7. Operadores lógicos: Escribe un programa que tome dos valores booleanos ingresados por el usuario y muestre el resultado de las operaciones lógicas AND, OR y NOT entre esos valores.

8. Operador ternario: Escribe un programa que tome un número entero ingresado por el usuario y utilice el operador ternario para determinar si el número es positivo o negativo. Luego, muestra el resultado en la salida.

# SOLUCIÓN...

1. package com.mycompany.actividadsesion4;

import java.util.Scanner;

public class ActividadSesion4 {

public static void main(String[ ] args) {

 Scanner input = new Scanner (System.in);

System.out.print ("Ingrese et primer numero: ");

 int num1 = input.nextInt( ); 

System.out.print ("Ingrese el segundo numero: ");

int num2 = input.nextInt( );

int suma =num1 + num2;

System.out.println("La suma de los dos numeros ingresado es: + suma);

int multiplicacion = num1 * num2;

System.out.print ("La multiplicación de los dos numeros ingresados es: "+
multiplicacion );
}
 }

2. package com.mycompany.actividadseston4;

import java.util.Scanner;

public class ActividadSesion4 {

public static void main(String[] args) { 

Scanner input = new Scanner (System.in);

System.out.print ("ingrese el primer numero: "); 

int numl = input.nextInt();

System.out.print ("Ingrese el segundo numero: ");

 int num2 input.nextInt();

int resta num1 - num2;

System.out.println("La resta de los dos numeros ingresado es: + resta);

int division = num1 / num2; 

System.out.print ("La division de los dos numeros ingresados es:"+
division);
}
 } 

3. package com.mycompany.actividadseston4;

import java.util.Scanner;

public class ActividadSesions {

public static void main(String[] args) { 

Scanner Input = new Scanner (System. Ln);

System.out.print (ingrese el primer numero entero: "); 

int nl input.nextInt();

System.out.print ("Ingrese el segundo numero entero: ");

int n = input.nextInt();

System.out.print ("Ingrese el tercer numero entero: ");

 int n3 input.nextInt();

int suma ni+n2+ n3;

 int mult ni* n2;

int div mult / n3:

System.out.println ("La suma de los tres numeros enteros ingresados es: "+
suma);

System.out.print ("La multiplicacion de los primeros numeros ingresados es: mult);

System.out.print ("El resultado de la multipicación dividido por el tercer numero ingresado es: +div);
}
  }

4. package com.mycompany.actividadseston4;

import java.util.Scanner;

public class ActividadSeston4 {

public static void main(String[] args) {

Scanner Input = new Scanner (System.in);

System.out.print ("ingrese el primer numero decimal: "); 

float n1 = input.nextFloat();

System.out.print ("Ingrese el segundo numero decimal: "); 

float n2= input.nextFloat();

float suma nt + n2; 

float resta nl - n2;

float mult = ni* n2;

float div nl / m2;

System.out.println("La suma de los dos numeros ingresados es: + suma); 

System.out.println("La resta de los dos numeros ingresados es: + resta); 

System.out.print ("La multiplicacion de los numeros ingresados es:"+
mult);

System.out.print ("La division de los numeros ingresados es: " + div);
}
  }

  5. package com.mycompany.actividadseston4;

public class ActividadSesion4 {

public static void main(String[] args) {

int numero= 15;

numero++;

System.out.println("Incremento" + numero);
numero--;

System.out.println("Decremento" + numero);
} 
 }

 6. package com.mycompany.actividadsesion4;

public class ActividadSesion4 {

public static void main(String[] args) { 

int num = 5;

num+=5;

System.out.println("Valor + num);

}
 }

 7. package com.mycompany.actividadsesion4;

import java.util.Scanner;

public class ActividadSesion4 {

public static void main(String[] args) { 

Scanner melo= new Scanner(System.in);

System.out.print("Ingrsa el primer valor booleano: "); 

boolean v1 = melo.nextBoolean();

System.out.print("Ingresa el segundo valor booleano: ");

boolean v2 = melo.nextBoolean();

boolean rivi && v2;

boolean r2 = v1 || v2;

boolean r3 = 1v1;

boolean r4 1v2;

System.out.println("Respuesta con el resultado AND" + r1);

System.out.println("Respuesta con el resultado OR + r2); 

System.out.println("Respuesta con el resultado del primer valor" + r3); 

System.out.println("Respuesta con el resultado del segundo valor + r4);
} 
 }

 8. package com.mycompany.actividadsesion4;

import java.util.Scanner;

public class ActividadSesion4 {

public static void main(String[] args) { 

Scanner scanner = new Scanner(System.in);

System.out.print("Ingresa un número entero: "); 

int numero= scanner.nextInt();

String Numero = (numero >= ) ? "positivo": "negativo";

System.out.println("El número es " + Numero);
}
 }






