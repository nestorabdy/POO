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

Definición de la superclase

Comienza definiendo una clase base, también llamada superclase, que contiene los atributos y métodos comunes que deseas compartir con las clases derivadas.

      public class Animal {
        String nombre;
          public void comer() {
             System.out.println("El animal está comiendo.");
          }
      }
  
-Creación de la clase derivada

Luego, crea una nueva clase que herede de la clase base usando la palabra clave *extends*.

      public class Perro extends Animal {
          public void ladrar() {
              System.out.println("El perro está ladrando.");
          }
      }
