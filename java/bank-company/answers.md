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

### 9. Explain what is TDD? What is triangulation?

TDD (Test Driven Development) es una metodología de desarrollo que se enfoca en desarrollar el código a partir de un test previamente implementado que compruebe su correcto funcionamiento.

La triangulación en TDD sería el método por el cual se escribe una prueba inicial que describe el "happy-path" o comportamiento esperado, se implementa el código mínimo para cumplir con dicho test, después se agregan más pruebas que cubran casos adicionales y límite, se refactoriza el código para que cumpla con dichos tests, y se continua el ciclo hasta que se hayan cubierto todos lo casos y tests pasen.

### 10. What types of software testing do you know? (unit, ...)

Existen muchos tipos diferentes de tests, pero los principales son los tests unitarios, de integración, y end-to-end, aunque también cabe mencionar los tests de carga y balance, los tests de seguridad y el pentesting (que se acerca más a una técnica).

## Clean Code

### 11. At project level, how do you structure your code?

Lo mås correcto es analizar el tipo de problema que se pretende resolver y seleccionar una estructura acorde a las necesidades, pero para aplicaciones de un tamaño medio / grander me gusta aplicar arquitectura hexagonal con DDD, vertical slicing y TDD siempre que este último me aporte valor y no me retrase.

### 12. What is a Software design pattern? Which ones do you often use?

Un patr6n de diseöo de software es una forma común, ya bien estudiada, aplicada y testeada, para dar una soluciön eståndar a un problema concreto.

Generalmente utilizo el patron Singleton, Factory, Port Command, Adapter y Observer.

### 13. What do you notice when you do code review?

A1 implementar Code Review, generalmente noto que se consigue un cédigo mås consistente, con un estilo comün, y donde se suplen las carencias ndividuales que cada miembro del equipo pueda tener, obteniendo un cådigo mucho mås mantenible, escalable y de mayor calidad.

## Git

### 14. What is Git and what is it used for? List all Git commands that you know

Git el principal mecanismo para gestionar IOS diferentes cambios y versiones que tiene el código de una aplicaci6n, aunque no solo se limita necesariamente al código.
Los principales comandos que utilizo en mi dia a dia son:

- git clone [url del repositorio]: Para clonar un repositorio de cödigo al equipo local
- git add . : Para incluir todos los cambios que deseo guardar a Ia hora de realizar un commit
- git commit -m "[texto del mensaje]": Para versionar los cambios mås recientes en el repositorio
- git push: Para subir los cambios y que otros miembros del equipo puedan tener acceso a ellos
- git remote add origin [url del repositorio]: Para incluir la url de un repositorio remoto que albergarå los cambios de la aplicaciån.
- git branch [nombre de la rama]: Para crear una nueva rama en el repositorio
- git checkout [nombre de la rama]: Para checkear el estado de la rama y comprobar si tenemos cambios pendientes por bajar del repositorio, o tenemos código pendiente de subir.

## Network

### 15. What is the difference between hRttp and https? Do you know what is Mutual TLS?

La principal diferencia es la seguridad en la comunicaci6n de los datos, HTTPS es la forma de proveer de encriptaciön por defecto a los datos enviados mientras que HTTP se usa cuando la seguridad y confidencialidad no es un problema.

### 16. What does the different http status code range stands for (IXX, 2XX ...)?

- Informativos (Ixx): Son para informaciön provisional, más centrado en el protocolo.
- Éxito (2xx): Indican que la solicitud del cliente se ha procesado de forma correcta.
- Redirección (3xx): Cuando se requiere de una acciön adicional para completar la request.
- Error en la solicitud del cliente (4xx): Indican que se ha producido un error en la solicitud del cliente por datos inesperados, ausencia de paråmetros, etc.
- Error en el servidor (5xx): Similar a los anteriores pero para indicar que se ha producido un error inesperado en el serv'idor al procesar la request.

## Spring

### 17. How would you explain to someone what Spring is? What can it bring to their projects?

Es un framework open-source para desarrollar aplicaciones backend en lenguajes como Java, Kotlin o Groovy. Estå basado en Java y ofrece una soluci6n standart para crear aplicaciones empresariales completas.

Generalmente se utiliza de la mano con Spring Boot, Spring Security y otras herramientas para proporcionar una correcta configuraciån por defecto a los desarrolladores, y que estos se puedan centrar en implementar soluciones que aporten valor al producto y resuelvan problemas.

### 18. What's the difference between Spring and Spring Boot?

Normalmente suelen confundirse, pero la principal diferencia es que cuando hablamos de Spring, nos referimos al framework completo, y cuando hablamos de Spring Boot, nos referimos a la herramienta que puede integrarse con Spring para simplificar la configuraci6n y gesti6n de dicho framework.

## Databases

### 19. What is an ORM? which ones do you often use?

Un ORM es una técnica de programaci6n que suele utilizarse para mapear objetos de una relaci6n a tablas de una base de datos, permitiendo manejar la información de la capa de persistencia como si fueran objectos.

Normalmente para este cometido suelo usar Hibernate como implementaci6n de JPA

### 20. Do yow know flyway/liquibase? what is used for?

Son herramientas ara la migraciån de bases de datos que permiten definir cambios de manera controlada y estructurada, sin embargo nunca he tenido la necesidad de usarlos.

## Event Driven Development

### 21. Do you know what CQRS is? And Event sourcing?

CQRS (Command Query Responsibility Segregation): Es un patron de arquitectura que generalmente se aplica en sistemas dirigidos por eventos donde se separan las operaciones de escritura en base de datos de Ias operaciones de consulta (Qygu).

Event Sourcing: Es un patron de diseño que de forma similar a CQRS se encuentra orientado a sistemas dirigidos por eventos. Este consiste en capturar acciones especificas (casos de uso), para almacenarlos de forma secuencial en eventos que puedan ejecutarse de forma que el estado de la aplicación sea reconstruible.

## Infraestructure

### 22. Differences between IaaS and PaaS Do you know any of each type?

Ambos son conceptos de cloud computing que se diferencian en que IaaS (Infraestructure as a Service) estå basado en ofrecer soluciones hardware a través de servicios, ofreciendo opciones limitadas de configuraciOn para dicho hardware. Por otro lado PaaS as a ofrece una implementación abstracta ya lista para usar, donde los desarrolladores pueden centrarse en desarrollar nuevas features y no tanto en configuraciones sobre escalabilidad, mantenimiento y gesti6n de infraestructura.

- Ejemplos de IaaS: nubes püblicas como Google Cloud, AWS y Microsoft Azure.
- Ejemplos de PaaS: plataformas como Heroku o Vercel, mås especificas y rientadas a ofrecer un servicio concreto.

### 23. Which kind of information does prometheus expose?

Prometheus puede recopilar, almacenar y exponer métricas de diferentes sistemas. Los principales tipos de información que puede exponer a través de estas métricas son:

- Los contadores, que varian en funciön de los eventos que establezcamos (por ejemplo peticiones HTTP).
- Histogramas, donde nos proveen informacién de la distribuci6n de un cierto rango de valores (por ejemplo para medir el tiempo de respuesta).
- Medidores o gauges: Para obtener info. de una métrica en un valor especifico (datos concretos).
- Resumenes o summaries: Proporcicnan un resumen estadistico sobre un rango de valores.

### 24. What is a pipeline? what experience do you have with them?

Un pipeline es una forma automatizada y organizada de realizar una determinada tarea que a menudo estå compuesta de diferentes pasos.

Por lo general se encuentra estrechamente relacionada con los repositorios de software ya que puede servir como principal herramienta para gestionar la integraci6n de cödigo y el despliegue de aplicaciones a través de diferentes stages.

Como DevOps tengo experiencia implementando pipelines para realizar anålisis de vulnerabilidades, compilación, testing, evaluación y despliegue del código utilizando principalmente Microsoft Azure DevOps, AWS CodePipeline, Jenkins, Github Actions y Bitbucket.

## Containers

### 25. What is the difference between an image and a container?

Una imagen es una representaciån eståtica de todo 10 necesario para ejecutar una aplicación, incluyendo el sso base, las bibliotecas, las dependencias y la configuracién del entorno, que se crea a partir de un Dockerfile; mientras que un contenedor es una instancia en ejecuciån de una imagen, que se ejecuta de forma aislada.

A partir de una imagen podemos generar mültiples instancias que pueden llevar a cabo diferentes cometidos pese a que en Origen provienen de Ia misma imagen.

### 26. What is 'kubeclt'?

kubectl es el CLI de Kubernetes encargado de recibir los comandos que nos permiten interactuar y administrar los recursos de Kubernetes.

## Linux

### 27. From a terminal, how would you connect to the remote machine '10.0.0.200' with the user 'logs'

Dependiendo del entorno donde nos encontremos la forma puede variar, sin embargo la forma más tradicional es a través de SSH:

```bash
ssh logs@10.0.0.200
```

Sin embargo, el uso de IaaS como AWS nos permiten conectarnos de forma alternativas, de forma que no sea necesario exponer el puerto 22 por defecto de SSH y asi exponernos a futuras vulnerabilidades.

### 28. Once in the machine '10.0.0.200' how would you find all files where its name ends with '.TRACE.log'

Por lo general depende del sistema operativo, pero una posible solución en Linux sería a través del comando *find*:

```bash
find [ruta origen de la búsqueda] -type f -name "*.TRACE.log"
```

De esta manera buscaremos en la ruta proporcionada los ficheros que se correspondan con la condición de que terminen en ".TRACE.log"
De igual forma pueden utilizarse otros comandos como *grep* para obtener el mismo resultado.

### 29. How would you filter all lines that contains 'USER_CODE'

Suponiendo de nuevo el caso de encontrarnos en un SSOO Linux, podemos utilizar el comando *grep*:

```bash
grep "USER_COOE" [nombre del archivo]
```

De esta manera se buscaré en el archivo especificado la cadena "USER_CODE" siendo esta case sensitive.
