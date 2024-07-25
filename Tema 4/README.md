# Tema 4: Herencia y polimorfismo

## :dart: Objetivo:
El alumno aplicará las diferentes propiedades de la programación orientada a objetos para la resolución de
problemas.

## Herencia

La herencia es una de las características más importantes en la POO porque permite que una clase herede los atributos y métodos de otra clase (los constructores no se heredan). Esta característica garantiza la reutilización del código. 

Con la herencia todas las clases están clasificadas en una jerarquía estricta. Cada clase tiene su superclase (la clase superior en la jerarquía, también llamada clase base), y cada clase puede tener una o más subclases (las clases inferiores en la jerarquía; también llamadas clases derivadas).

**Ventajas de la herencia**

La herencia en Programación Orientada a Objetos (POO) ofrece varias ventajas que contribuyen a la organización, reutilización y extensibilidad del código.

- **Reutilización de código:** Permite que las clases hereden atributos y métodos de una clase base. Esto significa que puedes reutilizar funcionalidades comunes y evitar la duplicación de código.
- **Facilita la extensibilidad:** Puedes extender una clase existente para crear una nueva clase que herede todas las características de la clase base y luego agregar o modificar sus propias características. Esta flexibilidad facilita la adaptación y extensión del software a medida que los requisitos cambian o evolucionan.
- **Promueve la coherencia y consistencia:** Al agrupar características comunes en una clase base, garantizas que todas las clases derivadas mantengan una estructura y comportamiento coherentes. Esto facilita la administración del código y mantiene una organización lógica y consistente en la jerarquía de clases.
- **Facilita la implementación de relaciones “es un”:** La herencia permite modelar relaciones “es un” entre las clases. Por ejemplo, si tienes una clase “Animal”, puedes derivar clases más específicas como “Perro”, “Gato”, etc., que son tipos de animales. Esto refleja las relaciones de herencia naturales en el mundo real.
- **Abstracción y generalización:** Al identificar características comunes en clases relacionadas, puedes abstraer estas características en una clase base que capture la esencia común de esas clases. Esto fomenta la generalización y ayuda a comprender y organizar mejor el código.

**Implementación**

- Definición de la superclase

Comienza definiendo una clase base, también llamada superclase, que contiene los atributos y métodos comunes que deseas compartir con las clases derivadas.

      public class Animal {
        String nombre;
          public void comer() {
             System.out.println("El animal está comiendo.");
          }
      }
  
- Creación de la clase derivada

Luego, crea una nueva clase que herede de la clase base usando la palabra clave *extends*.

      public class Perro extends Animal {
          public void ladrar() {
              System.out.println("El perro está ladrando.");
          }
      }

## Polimorfismo

En la programación, esto se traduce en la habilidad de una clase para implementar métodos con el mismo nombre pero con comportamientos distintos, dependiendo de la clase específica con la que se esté interactuando. Esto añade flexibilidad y extensibilidad a tu código, permitiendo adaptarse a diferentes situaciones y requerimientos.

**Ventajas del polimorfismo**

- **Permite que los objetos se comporten de diferentes maneras** según el contexto en el que se utilicen. Esto proporciona flexibilidad en el diseño y la implementación del código, permitiendo adaptarse a diferentes situaciones.
- **Simplicidad y claridad del código**: Al utilizar interfaces o clases base abstractas que definen un conjunto común de métodos, el polimorfismo ayuda a simplificar la lógica del código. Esto mejora la legibilidad y la claridad, ya que se centra en lo que un objeto hace, no en los detalles de cómo lo hace.
- **Permite la expansión de funcionalidades**: Se pueden agregar nuevas clases que implementen una interfaz o hereden de una clase base abstracta existente. Esto significa que puedes expandir la funcionalidad del programa sin modificar el código existente.
- **Fomenta la desacoplación y la modularidad**: Al utilizar interfaces y clases abstractas, el código se vuelve menos dependiente de implementaciones concretas. Esto promueve una menor interconexión entre componentes, lo que conduce a sistemas más modulares y desacoplados.

**Implementación**

El polimorfismo es un concepto importante en la Programación Orientada a Objetos (POO) que permite que los objetos de diferentes clases respondan a un mismo mensaje de manera específica para cada uno. En Java, el polimorfismo se logra mediante el uso de herencia y la implementación de interfaces.

- Crear una clase base

Debes tener una clase base o una interfaz que defina los métodos que deseas que las clases derivadas implementen de manera específica. Por ejemplo:

      public interface Animal {
       void hacerSonido();
    }
  
- Crear la interfaz

Luego, crea clases concretas que implementen la interfaz o hereden de la clase base. Cada una de estas clases debe proporcionar su propia implementación del método definido en la interfaz o clase base.

       public class Perro implements Animal {
          public void hacerSonido() {
              System.out.println("El perro ladra.");
          }
      }

    public class Gato implements Animal {
        public void hacerSonido() {
            System.out.println("El gato maulla.");
        }
    }

- Utilizar polimorfismo

Ahora puedes crear objetos de las clases derivadas y tratarlos como objetos de la interfaz o clase base. Esto significa que puedes llamar al método común hacerSonido() sin saber la implementación específica de la clase.

    public class Main {
        public static void main(String[] args) {
            Animal miMascota = new Perro();
            miMascota.hacerSonido(); // Llama al método del perro
    
            miMascota = new Gato();
            miMascota.hacerSonido(); // Llama al método del gato
        }
    }

Esto es el polimorfismo en acción: objetos de diferentes clases responden al mismo mensaje de manera específica para cada uno.

## Constructores

Un **constructor** es un método especial que se llama automáticamente cuando se crea una instancia u objeto de una clase. Su objetivo principal es inicializar los atributos de la clase y realizar cualquier otra inicialización necesaria antes de que el objeto esté listo para su uso. Los constructores tienen el mismo nombre que la clase y no tienen tipo de retorno.

Los constructores son fundamentales para inicializar y configurar un objeto de forma apropiada. Pueden recibir parámetros que permiten pasar valores iniciales al objeto durante su creación.

### Tipos de constructores en Java

En Java, hay varios tipos de constructores que puedes utilizar según tus necesidades.

**Constructor por defecto**

No toma ningún parámetro. Si no defines ningún constructor en tu clase, Java proporciona un constructor por defecto sin argumentos automáticamente.

    public class Persona {
        // Constructor por defecto (sin argumentos)
        public Persona() {
            // Inicialización por defecto
        }
    }
    
**Constructor con parámetros**

Toma uno o más parámetros. Este tipo de constructor te permite inicializar los atributos de la clase con valores específicos durante la creación del objeto.

    public class Persona {
        private String nombre;
        private int edad;
        // Constructor con parámetros
        public Persona(String nombre, int edad) {
            this.nombre = nombre;
            this.edad = edad;
        }
    }
    
**Constructor copia**

Toma un objeto del mismo tipo como parámetro y crea un nuevo objeto con los mismos valores de atributos que el objeto pasado como argumento.

    public class Persona {
        private String nombre;
        private int edad;
        // Constructor copia
        public Persona(Persona otraPersona) {
            this.nombre = otraPersona.nombre;
            this.edad = otraPersona.edad;
        }
    }
    
**Constructor privado**

Se usa generalmente para evitar que se instancie la clase directamente y forzar la creación de objetos a través de métodos de fábrica u otros mecanismos de creación controlada.

    public class Singleton {
        private static Singleton instance;
        // Constructor privado
        private Singleton() {
            // Inicialización
        }
        public static Singleton getInstance() {
            if (instance == null) {
               instance = new Singleton();
            }
            return instance;
        }
    }

    

### Cómo crear construtores en Java

Para crear constructores en Java, sigue estos pasos básicos:

 1. Decide qué atributos inicializará el constructor 
 2. Define la clase y los atributos 
 3. Escribe la firma del constructor 
 4. Inicializa los atributos dentro del constructor

## Encapsulamiento

El encapsulamiento en Java es un principio fundamental de la POO que consiste en agrupar los datos (atributos) y los métodos (comportamientos) relacionados con un objeto dentro de una sola unidad, llamada clase. Además, se controla el acceso a estos datos y métodos, permitiendo únicamente interacciones controladas desde el exterior de la clase.

La encapsulación permite ocultar la complejidad interna de una clase, proporcionando una interfaz controlada para interactuar con los objetos de esa clase. Esto mejora la seguridad y la integridad de los datos, ya que solo se pueden modificar a través de métodos específicos de la clase, permitiendo así una validación adecuada antes de realizar cualquier cambio.

Un ejemplo común de encapsulación en Java es tener atributos privados y proporcionar métodos públicos de acceso, conocidos como *get()* y *set()*, para leer y modificar esos atributos de forma controlada. Este enfoque garantiza que el acceso a los datos sea a través de métodos que puedan aplicar validaciones o lógica adicional antes de realizar cualquier modificación.

Para lograr la encapsulación en Java, se utilizan modificadores de acceso, como *public*, *private* y *protected*, para determinar qué partes del código pueden acceder y modificar los atributos y métodos de una clase.

**Public**: Los miembros (atributos y métodos) marcados como públicos son accesibles desde cualquier parte del programa. No existen restricciónes en su acceso.

**Private**: Los miembros marcados como privados solo son accesibles dentro de la misma clase. Otros objetos o clases no pueden acceder directamente a ellos.

**Protected**: Los miembros marcados como protegidos son accesibles dentro del mismo paquete y también por clases derivadas (herencia) fuera del paquete.

A través del encapsulamiento, se puede lograr la inmutabilidad de ciertos atributos de una clase. Al marcar un atributo como privado y proporcionar solo un método de lectura (get), se evita que dicho atributo sea modificado accidental o intencionalmente desde fuera de la clase.

Ventajas del encapsulamiento en Java
El encapsulamiento en Java ofrece una serie de beneficios que son fundamentales para el desarrollo de software de calidad. Entre ellos podemos destacar los siguientes:

- **Seguridad de datos**: Al marcar los atributos como privados, se protegen de accesos no autorizados desde fuera de la clase. Esto evita que los datos se corrompan o modifiquen de manera inesperada, mejorando la seguridad y la integridad del programa.
- **Control de acceso**: Java permite establecer niveles de acceso a los miembros de una clase, como public, private y protected. Esto controla quién puede acceder a los atributos y métodos de la clase, permitiendo un acceso controlado y seguro.
- **Abstracción**: La encapsulación permite ocultar los detalles de implementación de una clase y proporcionar una interfaz pública clara y coherente. Esto facilita la interacción con la clase y reduce la complejidad para otros desarrolladores que utilizan la clase.
- **Flexibilidad**: A través de los métodos “setters” y “getters”, puedes agregar lógica personalizada para validar y transformar los datos antes de su acceso o modificación. Esto brinda flexibilidad para adaptar y modificar la clase sin afectar a otros componentes del programa.
- **Mantenibilidad**: El encapsulamiento mejora la mantenibilidad del código al permitir cambios internos en la clase sin afectar a las partes que interactúan con ella. Esto facilita las actualizaciones y correcciones de errores sin riesgo de efectos secundarios no deseados.
- **Reutilización de código**: Las clases encapsuladas se pueden utilizar en diferentes partes de una aplicación o incluso en proyectos diferentes. Esto fomenta la reutilización de código, ya que una vez que se ha creado una clase bien encapsulada, es fácil de integrar en otros contextos.


Mecanismos para el encapsulamiento
Para implementar encapsulamiento en Java, sigue estos pasos clave que implican el uso de modificadores de acceso, métodos de acceso (getters y setters) y constructores:

1. Definir la clase que encapsulará los datos y métodos relacionados. En esta clase, declara los atributos que representan los datos y los métodos que operarán sobre esos datos.
2. Utilizar modificadores de acceso para controlar la visibilidad de los atributos y métodos. Es buena práctica mantener los atributos como privados (private) para ocultarlos del exterior de la clase.
3. Crear métodos públicos para obtener los valores de los atributos y métodos públicos para modificar estos valores. Estos métodos deben permitir un acceso controlado a los atributos privados.
4. Implementar un constructor para inicializar los atributos de la clase. Puedes tener varios constructores con diferentes parámetros para proporcionar flexibilidad en la inicialización, como vimos en el artículo de Objetos y Clases.

Ejemplos prácticos con encapsulamiento

      public class Persona {
          // Atributos privados
          private String nombre;
          private int edad;
      
          // Constructor
          public Persona(String nombre, int edad) {
              this.nombre = nombre;
              this.edad = edad;
          }
      
          // Método para obtener el nombre
          public String getNombre() {
              return nombre;
          }
      
          // Método para establecer el nombre
          public void setNombre(String nombre) {
              this.nombre = nombre;
          }
      
          // Método para obtener la edad
          public int getEdad() {
              return edad;
          }
      
          // Método para establecer la edad
          public void setEdad(int edad) {
              this.edad = edad;
          }
      
          public static void main(String[] args) {
              // Crear un objeto Persona
              Persona persona = new Persona("John Doe", 30);
      
              // Acceder a los datos a través de los métodos de acceso
              System.out.println("Nombre: " + persona.getNombre());
              System.out.println("Edad: " + persona.getEdad());
      
              // Modificar datos a través de los métodos de acceso
              persona.setEdad(31);
              System.out.println("Nueva edad: " + persona.getEdad());
          }
      }

## Interfaces

Una **interfaz** Java es un dispositivo que permite interactuar a objetos no relacionados entre sí. Las interfaces Java en realidad definen un conjunto de mensajes que se puede aplicar a muchas clases de objetos, a los que cada una de ellas debe responder de forma adecuada. Por eso, una interfaz recibe también el nombre de protocolo.

Una interfaz consta de dos partes: el nombre de la interfaz precedido por la palabra reservada interface y el cuerpo de la interfaz encerrado entre llaves. Esto es:

   [public] interface nombre_interfaz extends superinterfaz
   {
         cuerpo de la interfaz
   }

El cuerpo de la interfaz puede incluir declaraciones de constantes y declaraciones de métodos. La palabra clave extends significa que se está definiendo una interfaz que es una extensión de otras; también se puede decir que es una interfaz derivada de otras; estas otras se especifican a continuación de extends separadas por comas. Como habrá observado, a diferencia de las clases, una interfaz puede derivarse de más de una superinterfaz.

### Ventajas de las interfaces

Una interfaz se utiliza para definir un protocolo de conducta que puede ser implementado por cualquier clase en una jerarquía de clases. La utilidad que esto pueda tener puede resumirse en los puntos siguientes: 

- Captar similitudes entre clases no relacionadas sin forzar entre ellas una relación artificial. Una acción de este tipo permitiría, incluso, definir una matriz de objetos de esas clases y aplicar, si fuera necesario, la definición de polimorfismo.
- Declarar métodos que una o más clases deben implementar en determinadas situaciones.
- Orden: declarar interfaces que más tarde serán heredadas por una o varias clases permiten estructurar ordenadamente el código. 
- Simplificar: declarar un objeto sin especificar lo que debe hacer, esto es, la abstracción, permite simplificar el diseño de una aplicación.
- Flexibilidad: las interfaces permiten el polimorfismo, es decir, que objetos similares pueden implementar una misma interfaz. Esto ofrece una gran flexibilidad.
- Herencia: a diferencia de las clases, las interfaces permiten la herencia múltiple, lo que ofrece una gran flexibilidad a los diseñadores. 
- Relación entre clases: se pueden establecer relaciones entre clases de manera sencilla, algo que facilita la lógica del programa. 
- Reutilización del código: las interfaces pueden ser implementadas por diferentes clases, evitando así la redundancia y habilitando la reutilización de código.

### Implementación


En un videojuego de carreras, cada jugador puede diseñar su propio coche desde cero. Sin embargo, para que todos puedan competir de una forma justa, los coches deben seguir las mismas reglas.

Gracias a las interfaces de Java, es posible diseñar un modelo de coche que sirva de base para diseñar otros coches. Por ejemplo, todos tendrán una matrícula y podrán arrancar y detenerse. Veamos cómo se traduce esto en código Java. 


      public interface Vehiculo {
        public String matricula = "";
        public void arrancar();
        public void detener();
      }


Como ves, tan solo se trata de una clase declarativa que ofrece una plantilla para que cada jugador pueda diseñar su propio coche. Todos los coches tendrán la misma estructura, pero no todos funcionarán de la misma forma, ya que, además de tener una matrícula distinta, puede que un vehículo arranque en 1 segundo, mientras que otro lo haga en 0,5 segundos, dependiendo de la implementación realizada. 

      public class Coche implements Vehiculo {
        public void arrancar() {
          System.out.println("arrancando motor...");
        }
        public void detener() {
          System.out.println("deteniendo motor...");
        }
      }
