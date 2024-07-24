# Tema 1: El paradigma orientado a objetos

## :dart: Objetivo:
El alumno interpretará los conceptos de la programación orientada a objetos para aplicarlo a eventos del mundo real.

## Propiedades básicas del paradigma orientado a objetos

En Java, las clases son una parte fundamental de la POO y son la base para la creación de objetos, que son instancias de esas clases. Una clase en Java es un plano o un modelo que define la estructura y el comportamiento de los objetos que se pueden crear a partir de ella.

Los conceptos fundamentales de las clases en Java:

- **Atributos:** Las clases pueden tener atributos, también conocidos como variables de instancia, que representan las características o propiedades del objeto. En el ejemplo del coche los atributos serian el modelo, la velocidad máxima, etc.
- **Métodos:** Las clases contienen métodos que representan el comportamiento del objeto. Los métodos son funciones que pueden realizar acciones y manipular los atributos de la clase. En nuestro caso sería acelerar frenar, girar, etc.
- **Constructores:** Las clases pueden tener constructores, que son métodos especiales utilizados para inicializar objetos cuando se crean. Los constructores tienen el mismo nombre que la clase y pueden tener diferentes parámetros para configurar el estado inicial del objeto.
- **Encapsulación:** La encapsulación es un principio de la POO que se refiere a la ocultación de los detalles de implementación de una clase y la exposición controlada de sus atributos y métodos. En Java, puedes utilizar modificadores de acceso como private, protected, public, etc., para controlar el acceso a los miembros de una clase.
- **Herencia:** Las clases pueden heredar atributos y métodos de otras clases. La herencia permite la creación de jerarquías de clases, donde una clase (subclase o clase derivada) puede extender o heredar características de otra clase (superclase o clase base).
- **Instanciación:** Para utilizar una clase, primero debes crear una instancia u objeto de esa clase. Puedes hacerlo utilizando el operador new, seguido del nombre de la clase y los argumentos necesarios para el constructor si lo tiene.

### Ventajas y desventajas de la POO

**Ventajas:**

- La principal ventaja de la POO radica en la reutilización de código. Esto significa que puedes aprovechar y modificar clases y objetos existentes en lugar de crear todo desde cero. Esto ahorra tiempo y esfuerzo, además de reducir la posibilidad de errores.
- Por otro lado, permite agregar nuevas funcionalidades y mejorar el rendimiento de un programa de manera eficiente. Puedes modificar o extender clases existentes sin afectar negativamente el código ya implementado, lo que facilita las actualizaciones y la adaptación a nuevas necesidades.
- Promueve la división de un programa en módulos más pequeños y manejables. Esto facilita el desarrollo, la depuración y el mantenimiento del código, ya que cada componente se puede abordar de manera independiente.

**Desventajas:**

- La POO puede resultar en un tiempo de ejecución más lento en comparación con otros enfoques de programación, debido a la creación y manipulación de objetos adicionales. Paradigmas como la programación funcional pueden ser más eficientes en este sentido.
- Los objetos requieren más memoria para almacenar datos y métodos, lo que puede afectar el rendimiento en programas de mediana o gran complejidad. Este mayor consumo de memoria es una consideración importante en sistemas con recursos limitados.
- Al principio puede resultar compleja, especialmente para programadores novatos. La necesidad de comprender conceptos como herencia, polimorfismo y encapsulación puede aumentar el tiempo de aprendizaje y desarrollo. 
