# Práctica 13. Programación Orientada a Objetos

# Factor de ponderación: 10

### Objetivos

Los objetivos de esta práctica son que el alumnado:
- Desarrolle programas sencillos en C++ utilizando programación orientada a objetos, así como todas las características del lenguaje estudiadas anteriormente
- Aprenda a sobrecargar operadores en C++
- Ponga en práctica diferentes formas de relacionar clases en C++


### Rúbrica de evaluación de esta práctica
Se señalan a continuación los aspectos más relevantes (la lista no es exhaustiva) que se tendrán en cuenta a la hora de evaluar esta práctica. Se comprobará que el alumnado:

* Conoce los conceptos expuestos en el material de referencia de esta práctica.
* Ha realizado todos los ejercicios propuestos en este enunciado
* Es capaz de escribir programas simples en C++ que resuelvan problemas de complejidad similar a los que se proponen en este documento
* Sea capaz de utilizar VSC para editar y compilar programas de forma remota en su Máquina Virtual
* Conoce la plataforma Exercism y es capaz de descargar y realizar problemas sencillos interaccionando con ella.
* Es capaz de escribir un fichero `CMakeLists.txt` para automatizar el proceso de compilación de sus programas con `cmake` y `make`
* Ha automatizado la compilación de sus programas usando un fichero `Makefile` para cada uno de los programas que desarrolle
* Hace que sus programas se estructuren en torno a diferentes funciones (sean modulares)
* Todos sus programas se estructuran en directorios diferentes para cada "proyecto" haciendo que cada uno de
  ellos contenga un fichero `CMakeLists.txt` con la configuración de despliegue del proyecto.
* Utiliza en todos sus programas comentarios adecuados en el formato requerido por
[Doxygen](https://www.doxygen.nl/index.html)
* Acredita que todas las prácticas realizadas hasta la fecha se encuentran alojadas en repositorios privados de
[GitHub](https://github.com/).
* Acredita que es capaz de subir programas a la plataforma
[Jutge](https://jutge.org/)
para su evaluación
* Ha incluido un comentario prólogo en todos los ficheros (`*.cc`, `*.h`) de sus ejercicios
* Que todos los programas que desarrolla, antes de su ejecución imprimen en pantalla un mensaje indicando la
  finalidad del programa así como la información que precisará del usuario para su correcta ejecución.
* Hace que todos los programas que se presentan para su evaluación cumplan con los estándares definidos en la
[Guía de estilo de Google para C++](https://google.github.io/styleguide/cppguide.html)
* Utiliza siempre identificadores significativos en su programa (para constantes, variables, etc.) y
  no utiliza nunca identificadores de una única letra, tal vez con la excepción de las variables que utilice para iterar en un bucle.
* Acredita que es capaz de editar ficheros remotos en su VM usando vi
* Ha realizado todos sus ejercicios en la máquina virtual Ubuntu de la asignatura.
* Demuestra que es capaz de ejecutar comandos Linux en su VM


# Ejercicios
Al realizar los ejercicios cree dentro de su repositorio de esta práctica un directorio diferente para cada uno de los ejercicios. Asigne a cada uno de esos directorios nombres significativos.

Automatice la compilación del programa correspondiente a cada ejercicio con un fichero Makefile independiente para cada programa e inclúyalo en el correspondiente directorio. Alternativamente podría también usarse cmake con un fichero CMakeLists, si se prefiere.

Haga que todos los programas tomen su entrada por la línea de comandos y en caso de que se ejecuten sin pasarles el número adecuado de parámetros impriman en pantalla un mensaje indicando el modo correcto de ejecutar el programa.

El código de cada uno de los programas deberá organizarse de forma modular, es decir haciendo uso de funciones. Cada función deberá realizar una única tarea y hacerlo correctamente. El identificador de una función debe reflejar claramente la finalidad de la función.

Desarrolle una clase ComputeInt que permita la realización de diferentes cálculos con números enteros. Incluya al menos los siguientes métodos en la clase:

Factorial que permita calcular el factorial de un número (Problema Factorial de Jutge).

SumSerie que calcule la suma de los primeros n términos de la serie: 1 + 2 + 3 + ... + n.

IsPrime que permita determinar si un determinado número es primo (Problema Primality de Jutge).

IsPerfectPrime que permita determinar si un determinado número es un primo perfecto (Problema Perfect primes de Jutge).

AreRelativePrimes que permita determinar si dos números son mutuamente primos, es decir, si su único divisor común es el 1

La función main del programa que usara esta clase podría contener, entre otras, sentencias similares a las siguientes:

main() {

  ComputeInt compute_integer{10, 7}; 

  std::cout << compute_integer.Factorial() << std::endl; 

  std::cout << compute_integer.SumSerie() << std::endl; 

  std::cout << compute_integer.IsPrime() << std::endl; 

  std::cout << compute_integer.AreRelativePrimes() << std::endl; 

}

# La clase Racional.
Un número racional tiene un numerador y un denominador de la forma p/q donde p es el numerador y q el denominador. Por ejemplo, 1/3, 3/4 y 10/4 son números racionales.

Un número racional no puede tener denominador 0, pero sí puede ser cero el numerador. Todo número entero n es equivalente al racional n/1. Los números racionales se utilizan en cálculos precisos que involucran fracciones. Por ejemplo, 1/3 = 0.33333 .... Este número no puede ser representado de forma precisa en formato de punto flotante utilizando los tipos float o double. Para obtener resultados precisos es conveniente usar números racionales.

C++ dispone de tipos de datos para enteros y números en punto flotante, pero no para racionales. En este ejercicio se propone el diseño de una clase para representar números racionales.

Desarrolle un programa cliente racionales.cc que permita operar con números racionales y haga uso de la clase Racional que ha de diseñarse.

Las siguientes deben tomarse como especificaciones del programa a desarrollar:

Separe el diseño de su clase Racional en dos ficheros, racional.h y racional.cc conteniendo respectivamente la declaración y la definición de la clase.
La clase Racional incluirá al menos métodos para:
* Crear objetos de tipo Racional. Se debe implementar un constructor por defecto y uno parametrizado.
* Escribir (a fichero o a pantalla) un objeto de tipo Racional.
* Leer (por teclado o desde fichero) un objeto de tipo Racional.
* Sumar dos objetos de tipo Racional.
* Restar dos objetos de tipo Racional.
* Multiplicar dos objetos de tipo Racional.
* Dividir dos objetos de tipo Racional.
* Comparar objetos de tipo Racional.
* El programa ha de permitir leer un fichero de texto en el que figuran pares de números racionales separados por espacios de la forma:
a/b c/d

e/f g/h

  ...

y para cada par de números racionales, el programa ha de imprimir en otro fichero de salida todas las operaciones posibles con cada uno de los pares de números del fichero de entrada, de la forma:

a/b + c/d = n/m

  ...

### Si el programa se ejecuta sin pasar parámetros en la línea de comandos, debemos obtener el siguiente mensaje:

./racionales -- Números Racionales

Modo de uso: ./racionales fichero_entrada fichero_salida

Pruebe ./racionales --help para más información

Si el programa se ejecuta pasando como parámetro la opción --help se ha de obtener:

./racionales -- Números Racionales

Modo de uso: ./racionales fichero_entrada fichero_salida 


fichero_entrada: Fichero de texto conteniendo líneas con un par de números racionales: `a/b c/d` separados por un espacio

fichero_salida:  Fichero de texto que contendrá líneas con las operaciones realizadas: `a/b + c/d = n/m`

# Robot Simulator.

Descargue y estudie el problema [Robot Simulator de Exercism](https://exercism.org/tracks/cpp/exercises/robot-simulator) Teniendo en mente ese problema de Exercism (Robot Simulator), diseñe una solución orientada a objetos para el problema [Movements on the ground de Jutge](https://jutge.org/problems/P79784_en). Suba el problema a Jutge para su evaluación.

Su programa deberá basarse en una clase Robot a la que dotará de la funcionalidad necesaria para resolver el problema de Jutge. Para que Jutge evalúe su solución tendrá que (contrariamente a lo habitual) escribir todo su código en un único fichero. Incluya en un fichero robot_simulator_jutge.cc tanto el código de la clase Robot como la función main() que instancia un objeto robot.

El código de la función main() podría ser similar a este:

1 /** @brief Robot Client main function */

 2 int main() {

 3   const std::pair<int, int> kPosition{0, 0};

 4   const Bearing kBearing {Bearing::NORTH};

 5   Robot robot{kPosition, kBearing};

 6   std::string sequence;

 7   getline(std::cin, sequence);

 8   for (const auto& movement : sequence) {

 9     ...

10   }

11   std::pair<int, int> final_position = robot.get_position();

12   std::cout << "(" << final_position.first << ", " << final_position.second  << ")" << std::endl;

13   return 0;

14 }

En la función main() se declara (línea 5) un objeto robot que se inicializa con una posición (position) y una orientación (bearing) que han sido definidas anteriormente (líneas 3 y 4).

Para trabajar con las posiciones se utiliza un objeto position que se define en la clase std::pair de la STL y que en este caso se utiliza para almacenar un par de números enteros, que definen la posición del robot.

Los ejemplos de este tutorial de Geeksforgeeks pueden servirle de ejemplo para iniciarse en el estudio de std::pair.

Al revisar ese tutorial y reproducir sus ejemplos, ¡tenga en cuenta las consideraciones de estilo que se usan en Informática Básica!.

Las orientaciones que utiliza el robot (norte, sur, este, oeste) se definen en el programa en una clase Bearing cuya definición es la siguiente:

enum class Bearing {

  NORTH,

  EAST,

  SOUTH,

  WEST

};

Es decir, se trata de una clase que simplemente define una enumeración con los valores correspondientes a los puntos cardinales.

La función main() anterior lee una secuencia de movimientos (línea 7) y en el bucle for de la línea 8 hace que el robot ejecute cada uno de los movimientos de la secuencia. Al final del bucle (línea 12) se imprime la posición final del robot.

Realice un programa orientado a objetos que resuelva el ejercicio Robot Simulator de Exercism. Consiga que su solución pase todos los tests y envíe su solución a la plataforma.
Si estudia el fichero robot_simulator_test.cpp de tests del problema observará que la clase Robot a diseñar ha de contener al menos los métodos:
get_bearing()
get_position()
turn_right()
turn_left()
advance()
execute_sequence()
El directorio robot-simulator-initial/ de esta práctica contiene código que puede servirle de ayuda para la resolución del problema.

Comience por descargar el ejercicio de exercism, que se alojará en un directorio con nombre robot-simulator/. Sustituya en ese directorio los ficheros robot_simulator.cpp y robot_simulator.h por los del directorio robot-simulator-initial/. Habiendo hecho esos cambios, ejecute cmake en el directorio robot-simulator-initial/build y compruebe que el programa pasa los primeros tests.

El el directorio robot-simulator-initial se han añadido los ficheros robot_simulator_main.cc y Makefile que no son necesarios para Exercism, pero pueden resultarle útiles para depurar su programa de forma independiente de Exercism. Copie esos ficheros en robot-simulator/ y ejecute make, que generará un fichero ejecutable que puede depurar con el VSC si lo necesita.

Continúe añadiendo el código necesario en robot_simulator.cpp y robot_simulator.h para pasar los tests de forma incremental.

Recuerde que la estrategia a seguir en la solución del problema consiste en ir "desbloqueando" progresivamente los distintos tests que ha de pasar el programa.


# La realización de este ejercicio es opcional.

Se recomienda realizarlo a aquél alumnado que considere que ha realizado progresos significativos en cuanto a su capacidad de realizar programas cada vez más complejos en C++.

Crearemos una clase llamada Serie con las siguientes características:
Sus atributos son título, número de temporadas, entrega, genero y creador.

Por defecto, el numero de temporadas es de 3 temporadas y entregado false. El resto de atributos serán valores por defecto según el tipo del atributo.

Los constructores que se implementarán serán:

Un constructor por defecto.

Un constructor con el titulo y creador. El resto por defecto.

Un constructor con todos los atributos, excepto de entregado.

Los métodos que se implementara serán:

Métodos get de todos los atributos, excepto de entregado.

Métodos set de todos los atributos, excepto de entregado.

Sobrescribe los métodos toString.

Crearemos una clase Videojuego con las siguientes características:
Sus atributos son titulo, horas estimadas, entregado, genero y compañia.

Por defecto, las horas estimadas serán de 10 horas y entregado false. El resto de atributos serán valores por defecto según el tipo del atributo.

Los constructores que se implementarán serán:

Un constructor por defecto.

Un constructor con el titulo y horas estimadas. El resto por defecto.

Un constructor con todos los atributos, excepto de entregado.

Los métodos que se implementara serán:

Métodos get de todos los atributos, excepto de entregado.

Métodos set de todos los atributos, excepto de entregado.

Sobrescribe los métodos toString.

Como vemos, en principio, las clases anteriores no son padre-hija, pero si tienen en común, por eso vamos a hacer una interfaz llamada Entregable con los siguientes métodos:

entregar(): cambia el atributo prestado a true.

devolver(): cambia el atributo prestado a false.

isEntregado(): devuelve el estado del atributo prestado.

Método compareTo (Object a), compara las horas estimadas en los videojuegos y en las series el numero de temporadas. Como parámetro que tenga un objeto, no es necesario que implementes la interfaz Comparable. Recuerda el uso de los casting de objetos.

Implementa los anteriores métodos en las clases Videojuego y Serie. Ahora crea una aplicación ejecutable y realiza lo siguiente:

Crea dos arrays, uno de Series y otro de Videojuegos, de 5 posiciones cada uno.

Crea un objeto en cada posición del array, con los valores que desees, puedes usar distintos constructores.

Entrega algunos Videojuegos y Series con el método entregar().

Cuenta cuantos Series y Videojuegos hay entregados. Al contarlos, devuélvelos.

Por último, indica el Videojuego tiene más horas estimadas y la serie con mas temporadas. Muestralos en pantalla con toda su información (usa el método toString()).
