# Tema 3: Tipos, expresiones y control de flujo

## :dart: Objetivo:
El alumno aplicará las técnicas y herramientas de la programación orientada a objetos para la solución de problemas.

## Generalidades

### Identificadores
**Una variable** representa un espacio de memoria para almacenar un valor de un determinado tipo, valor que puede ser modificado a lo largo de la ejecución del bloque donde la variable es accesible, tantas veces como se necesite. La declaración de una variable consiste en **identificarla** y asociarle un tipo.

Al elegir el identificador para declarar una variable, hay que considerar que el compilador Java trata las letras mayúsculas y minúsculas como caracteres diferentes. 

| Por ejemplo las variables **dato1** y **Dato1** son diferentes. 

Respecto al tipo de una variable, dependera del tipo de valor que vaya a almacenar.

    // Declaración de variables
    
    public class  identificadores
    {
    // Clase para declarar variables
    public static void main( String args[] )
    	{
    	float a = 0;
    	int cadena = 5;
    	double = 1.0;
    	} // fin del método main
    
     } // fin de la clase identificadores

### Palabras reservadas

En el lenguaje de programación Java, una **palabra reservada** es cualquiera de las 50 palabras exlusivas que tienen un significado predefinido en el lenguaje; debido a esto, no se pueden usar palabras reservadas como nombres para variables, métodos, clases o como cualquier otro identificador.

| Palabras  | Reservadas| 	         | 	         |              |
|-----------|-----------|------------|-----------|--------------|
| abstract	| continue	| for	     | new	     | switch       |
| assert	| default	| goto	     | package	 | synchronized |
| boolean	| do	    | if	     | private	 | this         |
| break	    | double	| implements | protected | throw        |
| byte	    | else	    | import	 | public	 | thows        |
| case	    | enum	    | instanceof | return	 | transient    |
| catch	    | extends	| int	     | short	 | try          |
| char	    | final	    | interface	 | static	 | void         |
| class	    | finally	| long	     | strictfp	 | volatile     |
| const	    | float	    | native	 | super	 | while        | 

### Comentarios

Un **comentario** es un mensaje dirigido a cualquiera que lea el código fuente. Tienen como finalidad explicar el código fuente.

Un comentario que comienza con **//** se llama **comentario de fin de línea** (o de una sola línea), ya que termina al final de la línea en la que aparece. 

    // Comentario de fin de línea

**Los comentarios tradicionales**, se distribuyen en varias líneas. Este tipo de comentario comienza con el delimitador **/*** y termina con ** */**. 

    /* Éste es un comentario
    Tradicional. Puede
    dividirse en muchas líneas */

### Descripción de una clases y objetos

Desde la POO un programa es un conjunto de objetos que dialogan entre sí para realizar las distintas tareas programadas.

| Una **clase** es una plantilla para crear objetos.

| Un **objeto** es una instancia de una clase.

La clase puede tener un método llamado **constructor** que se va a llamar cada vez que se cree un objeto de esa clase. El constructor se utiliza generalmente para inicializar los atributos de los objetos. Un constructor se distingue fácilmente porque tiene el mismo nombre que la clase a la que pertenece y no puede retornar un valor (ni siquiera se puede especificar la palabra reservada void).

En la clase se pueden definir métodos (el comportamiento) y atributos (información) que van a tener los objetos. A los atributos se les llama variables de instancia y a los métodos se les llama métodos de instancia.

Un método determina cómo tiene que actuar el objeto cuando recibe el mensaje vinculado con ese método.

Los atributos son información asociada a cada objeto. Los atributos son privados y solo pueden ser leídos y modificados dentro del objeto, a menos de que existan métodos para leerlos y modificarlos.

| Un atributo puede ser una un objeto de otra clase y puede acceder a sus métodos.
 
## Tipos de datos

### Tipos de datos primitivos



## Arreglos

## Tipos y ambitos de las variables

## Tipos de clases

## Estruturas de selección

## Estructuras de repetición
