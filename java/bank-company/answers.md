# Answers

## Agile

### 2. Have you ever worked with Scrum? Tell us what it is, what events do you remember and what roles are involved?

Si, los principales eventos que se producen en Scrum son:

- La reunión de planificación (Sprint Planning), donde el equipo de desarrollo selecciona los elementos del Product Backlog, el Product Owner (PO) clarifica los elementos del Backlog y define los objetivos del Sprint, y el Scum Master (SM) comprueba que se sigan las reglas de SCRUM.
- La reunión diaria (Daily Scrum): generalmente de corta duración (15 min), donde los miembros del equipo de desarrollo comentan que han hecho, que van a hacer y si tienen algún problema, mientras el SM se asegura del enfoque y la duración de la reunión.
- La reunión de revisión del Sprint (Sprint Review): Se produce al final de cada Sprint para que el equipo al completo junto con los stakeholders (cualquier persona que esté relacionada con la aplicación), se muestre el avance realizado y se pueda obtener feedback sobre posibles ajustes o mejoras en el producto.
- La reunión de retrospectiva (Sprint Retrospective): Se produce tras el Sprint Review, donde el equipo al completo realiza una evaluación sobre el Sprint recién terminado, indicando los puntos positivos, negativos y de mejora para aplicar en futuros Sprints.

## Java

### 3. What's new in Java 8? Explain some of them

- Uso de la clase Optional para facilitar el manejo de null, y nuevas funciones en las colecciones
  como forEach, replaceAll, etc.
- Expresiones Lambda: permiten implementar programación funcional, facilitando el uso de
  funciones como parámetros.
- Permitir la creación de interfaces que permitan realizar la implementación de métodos por
  defecto.
- Stream: una nueva api que permite realizar diferentes tipos de operaciones para filtrar, mapear,
  reducir y realizar transformaciones a las colecciones.

### 4. Given the following list implement a solution in order to get even numbers using Java 8 Streams

```java
List<lnteger> list = Arrays.asList(1,2,3A);
```

```java
List<lnteger> evenNumberList = list.stream0.filter(listElement listElement % 2
O).collect(Collectors.toList0);
```

### 5. What access modifiers (or visibility) do you know in Java?

public, private, protected y default (en el caso de no definir un modificador).

### 6. Differences between an abstract class and an interface. When would you use one or the other? Could you provide an hierarchy example?

La clase abstracta puede contener atributos y métodos que hereden sus clases fijas, sin embargo las interfaces solo pueden definir métodos abstractos (que pueden incluso proveer una implementación por defecto), para que otras clases la implementen.
Generalmente se suelen utilizar clases abstractas para la herencia, y las interfaces como principal método para eliminar el acoplamiento, proveer un contrato que cierta clase debe cumplir, y servir como herramienta principal para la inyección de dependencias.
Un ejemplo de herencia sería la existencia de una clase User que mantiene los atributes mínimos y comunes para albergar la información de un usuario, para luego mediante herencia crear una clase Admin que extienda de ella, incluyendo más campos que se encuentren relacionados con este tipo de Usuario, y de igual manera poder tener un VipUser que extienda de User y representa a un usuario con privilegios de compra en la aplicación.

### 7. What is Maven and why is it used? What is Maven life cycle? What kind of information include the file pom.xml?

Maven es una herramienta para gestionar y construir proyectos en Java, se utiliza debido a la cantidad de funcionalidades que ofrece como la facilidad de gestión de dependencias, la gestión de la configuración centralizada a través de un "pom.xml", y el ciclo de vida que ofrece.

El ciclo de vida de Maven ofrece tres fases que se ejecutan secuencialmente:

- Compilación: Se compila el código Java para generar los archivos class que se almacenarán en el target.
- Prueba: Se ejecutan los test realizados por los programadores generalmente utilizando JIJnit.
- Empaquetado e instalación: Se crea el archivo (jar/war) y se ubica en el repositorio local de Maven, pudiendo configurarse para que además se realice el despliegue de la aplicación.

El fichero "pom.xml" incluye información sobre el proyecto y su configuración, destacando la identificación del proyecto, las propiedades, las dependencias, los repositorios fuente donde maven debe ubicar las dependencias, y configuración adicional relacionada con directorios, plugins, etc.

## Testing

### 8. What is a mock? What would you use it for?

Un mock es una clase que simula el comportamiento de otra, generalmente se usa en los tests unitarios y dependiendo del enfoque los de integración para aislar la ejecución del tests, de manera que se limite la comunicación con otros componentes y se pueda testear un código concreto de manera aislada.

### 9.  Explain what is TDD? What is triangulation?

TDD (Test Driven Development) es una metodología de desarrollo que se enfoca en desarrollar el código a partir de un test previamente implementado que compruebe su correcto funcionamiento.

La triangulación en TDD sería el método por el cual se escribe una prueba inicial que describe el "happy-path" o comportamiento esperado, se implementa el código mínimo para cumplir con dicho test, después se agregan más pruebas que cubran casos adicionales y límite, se refactoriza el código para que cumpla con dichos tests, y se continua el ciclo hasta que se hayan cubierto todos lo casos y tests pasen.

### 10. What types of software testing do you know? (unit, ...)

Existen muchos tipos diferentes de tests, pero los principales son los tests unitarios, de integración, y end-to-end, aunque también cabe mencionar los tests de carga y balance, los tests de seguridad y el pentesting (que se acerca más a una técnica).

## Clean Code

## Git

## Network

## Spring

## Databases

## Event Driven Development

## Infraestructure

## Containers

## Linux
