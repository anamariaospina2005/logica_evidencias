<!-- No borrar o modificar -->
[Inicio](./index.md)

## Sesión 10 


# Actividad: Prueba, ejecución y explicación de ejercicios de lógica de programación.

Selecciona dos ejercicios de la sesión 10, impleméntalos, ejecútalos y proporciona una explicación detallada de cada uno

# SOLUCIÓN...

### Programa en Java para formar subgrupos con integrantes aleatorios de igual cantidad.

Programa en Java para formar subgrupos con integrantes aleatorios de igual cantidad Este programa en Java permite al usuario ingresar una lista de integrantes separados por comas y luego especificar la cantidad de subgrupos en los que desea dividir a esos integrantes. Los subgrupos se forman de manera aleatoria a partir de la lista de integrantes. Se crea una lista de cadenas llamada integrantes utilizando la clase ArrayList luego se solicita al usuario que ingrese la lista de integrantes separados por comas y eso se almacena en la variable inputIntegrantes, despues se solicita al usuario que ingrese la cantidad de subgrupos que desea formar y se mezclan de manera aleatoria la lista de integrantes utilizando Collections.shuffle(integrantes) para que los subgrupos se formen de manera aleatoria.

import java.util.Scanner;
 import java.util.ArrayList;
import java.util.Collections;

public class Sesion10 {

   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> integrantes = new ArrayList<String>();

      // Solicitar lista de integrantes
      System.out.print("Ingrese la lista de integrantes separados por coma: ");
      String inputIntegrantes = input.nextLine();
      String[] integrantesArray = inputIntegrantes.split(",");
      for (String integrante : integrantesArray) {
         integrantes.add(integrante.trim());
      }

      // Solicitar cantidad de subgrupos
      System.out.print("Ingrese la cantidad de subgrupos que desea formar: ");
      int cantidadSubgrupos = input.nextInt();

      // Formar subgrupos
      int integrantesPorSubgrupo = integrantes.size() / cantidadSubgrupos;
      int integrantesSobrantes = integrantes.size() % cantidadSubgrupos;
      Collections.shuffle(integrantes); // mezclar la lista de integrantes para formar subgrupos aleatorios
      int indiceInicial = 0;
      for (int i = 0; i < cantidadSubgrupos; i++) {
         int integrantesEnSubgrupo = integrantesPorSubgrupo;
         if (integrantesSobrantes > 0) {
            integrantesEnSubgrupo++;
            integrantesSobrantes--;
         }
         int indiceFinal = indiceInicial + integrantesEnSubgrupo;
         ArrayList<String> subgrupo = new ArrayList<String>(integrantes.subList(indiceInicial, indiceFinal));
         indiceInicial = indiceFinal;
         System.out.printf("Subgrupo %d: %s%n", i + 1, subgrupo);
      }
   }
}
### Programa en Java para asignar aleatoriamente ejercicios a un grupo de personas sin repetir

Este programa en Java permite asignar aleatoriamente una serie de ejercicios a una lista de personas ingresadas por el usuario. Los ejercicios se asignan de manera aleatoria y sin repetición.Se importan las clases Scanner, ArrayList y Collections para leer la entrada del usuario, crear listas y realizar operaciones de mezcla (shuffle) en las listas. ArrayList se usara para almacenar los nombres de las personas, la entrada del usuario se almacena en la variable inputPersonas, luego se genera una lista de números de ejercicios del 1 al número total de ejercicios utlizando un bucle for y se mezcla de manera aleatoria la lista utilizando Collections.shuffle(numerosEjercicios). Esto asegura que los ejercicios se asignen aleatoriamente a las personas sin repetir ningún ejercicio.

import java.util.Scanner;
import java.util.ArrayList;
import java.util.Collections;

public class Sesion10 {

   public static void main(String[] args) {
      Scanner input = new Scanner(System.in);
      ArrayList<String> personas = new ArrayList<String>();

      // Solicitar lista de personas
      System.out.print("Ingrese la lista de personas separadas por coma: ");
      String inputPersonas = input.nextLine();
      String[] personasArray = inputPersonas.split(",");
      for (String persona : personasArray) {
         personas.add(persona.trim());
      }

      // Obtener cantidad de ejercicios
      int cantidadEjercicios = personas.size();

      // Generar lista de ejercicios aleatorios sin repetir
      ArrayList<Integer> numerosEjercicios = new ArrayList<Integer>();
      for (int i = 1; i <= cantidadEjercicios; i++) {
         numerosEjercicios.add(i);
      }
      Collections.shuffle(numerosEjercicios); // mezclar la lista de números de ejercicios para asignarlos aleatoriamente
      ArrayList<String> ejercicios = new ArrayList<String>();
      for (int i = 0; i < cantidadEjercicios; i++) {
         ejercicios.add("Ejercicio " + numerosEjercicios.get(i));
      }

      // Asignar ejercicios a personas
      Collections.shuffle(personas); // mezclar la lista de personas para asignarles ejercicios aleatorios
      for (int i = 0; i < cantidadEjercicios; i++) {
         System.out.printf("%s: %s%n", personas.get(i), ejercicios.get(i));
      }
   }
}





