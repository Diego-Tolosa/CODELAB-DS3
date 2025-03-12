# CODELAB: CLEAN ARCHITECTURE

## Preguntas

 **1. ¿Qué problema busca resolver Clean Architecture en el desarrollo de software?**

**R//:  Clean Architecture** busca resolver el problema del acoplamiento excesivo entre la lógica de negocio y los detalles técnicos (frameworks, bases de datos, UI). Esto hace que el software sea más difícil de mantener, probar y escalar. Al separar las responsabilidades en capas bien definidas, permite cambiar tecnologías o componentes sin afectar el núcleo del negocio.

**2. ¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?**
-   **Dominio (Reglas de Negocio)**: Contiene las entidades y reglas de negocio puras. Es independiente de cualquier tecnología externa.
-   **Aplicación (Casos de Uso)**: Define los casos de uso que orquestan las operaciones del dominio. Se comunica con el dominio a través de interfaces.
-   **Infraestructura (Adapters & Frameworks)**: Implementa los detalles técnicos (persistencia, APIs, seguridad). Traduce las peticiones externas para que la aplicación no dependa de tecnologías específicas.
-   **Presentación (UI, Frameworks & Drivers)**: Gestiona la interacción con el usuario o sistemas externos. Es la puerta de entrada a la aplicación.

 **3. ¿Qué relación tiene Clean Architecture con el principio de Inversión de Dependencias (DIP) en SOLID?**
 
**R//: Clean Architecture** aplica el DIP al hacer que las capas externas dependan de las internas, nunca al revés. Por ejemplo, los casos de uso dependen de interfaces definidas en el dominio, y la infraestructura implementa esas interfaces. Esto reduce el acoplamiento y permite cambiar la implementación sin afectar la lógica de negocio.

**4. ¿Por qué es importante desacoplar la lógica de negocio de la infraestructura en una aplicación?**

**R//:** Porque facilita la mantenibilidad, las pruebas y la flexibilidad del sistema. Si la lógica de negocio no depende de la infraestructura, puedes cambiar de base de datos, framework o tecnología sin modificar las reglas de negocio. Esto reduce el riesgo de introducir errores al hacer cambios técnicos.

 **5. ¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad de un sistema?**

**R//:** Al dividir el sistema en capas desacopladas, puedes escalar o modificar una parte sin afectar el resto. Por ejemplo, podrías cambiar la capa de infraestructura para usar un servicio de mensajería o escalar la base de datos sin tocar la lógica de negocio. Además, las pruebas son más fáciles porque puedes probar las reglas de negocio sin depender de la infraestructura.

 **6. ¿Qué diferencia hay entre la capa de dominio y la capa de aplicación en Clean Architecture?**
-   **Dominio**: Contiene las reglas de negocio puras, entidades y objetos de valor. No tiene conocimiento de los casos de uso ni de la infraestructura.
-   **Aplicación**: Orquesta los casos de uso, aplicando las reglas del dominio. No implementa lógica de negocio, sino que coordina las entidades del dominio para resolver un problema específico.

**7. ¿Por qué los controladores (controllers) y la base de datos deben estar en la capa de infraestructura?**

**R//:** Porque son detalles de implementación que no deberían afectar la lógica del negocio. Los controladores solo gestionan la entrada/salida, y los repositorios interactúan con la base de datos, pero estos detalles deben quedar fuera del núcleo del sistema para mantener la independencia del dominio.

**8. ¿Qué ventajas tiene usar una interfaz en la capa de dominio para definir repositorios en lugar de usar directamente JpaRepository?**

**R//:** Usar interfaces en el dominio desacopla la lógica de negocio de la implementación concreta. Así, puedes cambiar la tecnología de persistencia (por ejemplo, de JPA a MongoDB) sin modificar la lógica de negocio, ya que solo necesitarías crear una nueva implementación de la interfaz.

**9. ¿Cómo interactúan los casos de uso (UseCases) con las entidades de dominio en Clean Architecture?**

**R//:** Los casos de uso actúan como coordinadores. Reciben una solicitud, recuperan o manipulan entidades del dominio a través de repositorios o servicios, aplican las reglas de negocio necesarias y devuelven la respuesta. Todo esto sin depender directamente de la infraestructura, solo a través de interfaces.

**10. ¿Cómo se puede aplicar Clean Architecture en una aplicación de microservicios con Spring Boot?**

**R//:** Podrías organizar el proyecto en paquetes por capas:
    

-   `domain`: entidades, objetos de valor, interfaces.
-   `application`: casos de uso y servicios.
-   `infrastructure`: controladores REST, adaptadores, repositorios JPA.
-   `config`: configuración de Spring.

Cada microservicio podría representar un subdominio, implementando su propia arquitectura limpia. Los servicios se comunican mediante eventos o API REST, pero internamente mantienen la independencia de su lógica de negocio respecto a los detalles técnicos.

