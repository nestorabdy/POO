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

### Polimorfismo

En la programación, esto se traduce en la habilidad de una clase para implementar métodos con el mismo nombre pero con comportamientos distintos, dependiendo de la clase específica con la que se esté interactuando. Esto añade flexibilidad y extensibilidad a tu código, permitiendo adaptarse a diferentes situaciones y requerimientos.

**Ventajas del polimorfismo**

- **Permite que los objetos se comporten de diferentes maneras** según el contexto en el que se utilicen. Esto proporciona flexibilidad en el diseño y la implementación del código, permitiendo adaptarse a diferentes situaciones.
- **Simplicidad y claridad del código**: Al utilizar interfaces o clases base abstractas que definen un conjunto común de métodos, el polimorfismo ayuda a simplificar la lógica del código. Esto mejora la legibilidad y la claridad, ya que se centra en lo que un objeto hace, no en los detalles de cómo lo hace.
- **Permite la expansión de funcionalidades**: Se pueden agregar nuevas clases que implementen una interfaz o hereden de una clase base abstracta existente. Esto significa que puedes expandir la funcionalidad del programa sin modificar el código existente.
- **Fomenta la desacoplación y la modularidad**: Al utilizar interfaces y clases abstractas, el código se vuelve menos dependiente de implementaciones concretas. Esto promueve una menor interconexión entre componentes, lo que conduce a sistemas más modulares y desacoplados.

**Implementacion**

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
