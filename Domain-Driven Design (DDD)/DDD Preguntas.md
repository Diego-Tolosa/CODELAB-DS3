# CODELAB: DOMAIN-DRIVEN DESIGN (DDD)

## Preguntas

**1. ¿Qué es Domain-Driven Design (DDD) y cuál es su objetivo principal?**

**R//: DDD** es una metodología de diseño de software que se centra en el dominio del negocio y su lógica compleja. Su objetivo principal es alinear el diseño del software con las necesidades del negocio, facilitando la creación de sistemas que reflejen fielmente los procesos y reglas del dominio. Para ello, DDD propone un conjunto de patrones y prácticas que ayudan a los equipos a modelar el dominio de manera efectiva.

**2. ¿Cuál es la diferencia entre una Entidad y un Objeto de Valor en DDD?**

- **Entidad:**  Es un objeto que tiene una identidad única y un ciclo de vida. Su identidad es lo que la distingue de otras entidades, incluso si sus atributos cambian. Ejemplo: Un usuario con un ID único. <br>

- **Objeto de Valor:**  Es un objeto que no tiene identidad y se define únicamente por sus atributos. Dos objetos de valor son iguales si sus atributos son iguales. Ejemplo: Una dirección (calle, ciudad, código postal).

**3. ¿Qué es un Bounded Context y por qué es importante en DDD?**

**R//:** Un **Bounded Context** es un límite conceptual dentro del cual un modelo de dominio específico es válido y consistente. Es importante porque permite dividir un sistema complejo en partes más manejables, evitando ambigüedades y conflictos en el significado de los términos y reglas del dominio. Cada Bounded Context tiene su propio lenguaje ubicuo y modelo de dominio.

**4. ¿Cuál es el propósito del Lenguaje Ubicuo (Ubiquitous Language) en DDD?**

**R//:** El **Lenguaje Ubicuo** es un lenguaje común y compartido entre los desarrolladores y los expertos del dominio. Su propósito es asegurar que todos los involucrados en el proyecto tengan una comprensión clara y consistente de los conceptos del dominio, evitando malentendidos y facilitando la comunicación efectiva.

**5. ¿Qué es un Agregado (Aggregate) y cómo garantiza la consistencia en el dominio?**

**R//:** Un **Agregado** es un conjunto de objetos de dominio (entidades y objetos de valor) que se tratan como una unidad única para la manipulación de datos. Tiene una raíz de agregado que actúa como punto de entrada para acceder y modificar el agregado. Garantiza la consistencia al encapsular las reglas de negocio y asegurar que todas las operaciones se realicen de manera válida y coherente.

**6. ¿Cómo se relacionan los Repositorios en DDD con la infraestructura de persistencia?**

**R//:** Los **Repositorios** son un patrón de DDD que proporciona una abstracción para acceder y almacenar agregados en la capa de persistencia. Actúan como intermediarios entre el dominio y la infraestructura de persistencia, permitiendo que el dominio permanezca agnóstico de los detalles técnicos de cómo se almacenan los datos (por ejemplo, en una base de datos).

**7. ¿Qué son los Eventos de Dominio y cómo mejoran la comunicación entre Bounded Contexts?**

**R//:** Los **Eventos de Dominio** son notificaciones que se generan cuando ocurre algo significativo en el dominio. Mejoran la comunicación entre Bounded Contexts al permitir que estos se comuniquen de manera desacoplada y asíncrona. Por ejemplo, un Bounded Context puede publicar un evento cuando se actualiza un dato, y otro Bounded Context puede suscribirse a ese evento para reaccionar en consecuencia.

**8. ¿Cómo se diferencian los Servicios de Aplicación y los Servicios de Dominio en DDD?**

- **Servicios de Aplicación:** Coordinan las operaciones de alto nivel y orquestan la interacción entre diferentes componentes del sistema. Suelen estar más relacionados con la lógica de la aplicación que con la lógica del dominio.

- **Servicios de Dominio:** Contienen lógica de negocio que no pertenece naturalmente a una entidad o un objeto de valor. Operan directamente sobre el dominio y encapsulan reglas de negocio específicas.

**9. ¿Cómo DDD facilita el diseño de software en sistemas complejos y escalables?**

- DDD facilita el diseño de sistemas complejos al:<br>
    1. **Dividir el dominio en Bounded Contexts**, lo que reduce la complejidad.
    2. **Promover un lenguaje común** entre desarrolladores y expertos del dominio.
    3. **Enfatizar la separación de preocupaciones** entre la lógica de negocio y la infraestructura.
    4. **Fomentar el uso de patrones como Agregados y Eventos de Dominio**, que ayudan a mantener la consistencia y escalabilidad.

**10. ¿Cómo se puede combinar DDD con Clean Architecture en una aplicación de microservicios?**

- DDD y Clean Architecture son complementarios:<br>
    1. **DDD** se enfoca en el dominio y la lógica de negocio.
    2. **Clean Architecture** organiza el código en capas (dominio, aplicación, infraestructura, etc.) para mantener la independencia del framework y la testabilidad.

- En una aplicación de microservicios:

    - Cada microservicio puede ser un **Bounded Context.**
    - La capa de dominio implementa los **Agregados**, **Entidades** y **Servicios de Dominio.**
    - La capa de aplicación maneja los **Servicios de Aplicación** y los **Casos de Uso.**
    - La capa de infraestructura implementa los **Repositorios** y la comunicación con otros microservicios (por ejemplo, mediante **Eventos de Dominio**).

