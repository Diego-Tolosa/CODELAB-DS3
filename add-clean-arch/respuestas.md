# CODELAB: USANDO ADD + CLEAN ARCHITECTURE

## Preguntas

 **1. ¿Qué es Attribute-Driven Design (ADD) y cuál es su propósito en el diseño de software?**

**R//:  ADD** es una metodología que diseña la arquitectura de un sistema en función de atributos de calidad (como rendimiento, seguridad o escalabilidad). Su propósito es asegurar que la arquitectura resultante satisfaga los requisitos no funcionales, priorizando características clave desde el inicio del desarrollo.

**2. ¿Cómo se relaciona ADD con Clean Architecture en el proceso de diseño de sistemas?**

**R//: ADD** define la arquitectura basándose en atributos de calidad, mientras que **Clean Architecture** organiza el código en capas bien definidas para mantener la separación de responsabilidades. **ADD** guía las decisiones arquitectónicas, y **Clean Architecture** implementa esas decisiones asegurando desacoplamiento y flexibilidad.

 **3. ¿Cuáles son los pasos principales del método ADD para definir una arquitectura de software?**
-   **Definir atributos de calidad y restricciones:** Identificar los requisitos del sistema y los atributos clave (rendimiento, seguridad, etc.).
-   **Diseñar la arquitectura:** Seleccionar tácticas para cumplir los atributos definidos, y organizar los módulos y su interacción.
-   **Implementar con Clean Architecture:** Estructurar el código en capas (dominio, aplicación, infraestructura, presentación).
-   **Validar y refinar:** Evaluar si la arquitectura satisface los atributos de calidad mediante pruebas y optimización.

**4. ¿Cómo se identifican los atributos de calidad en ADD y por qué son importantes?**

**R//:** Se identifican analizando los requisitos del sistema y consultando con los stakeholders. Los atributos (como latencia, disponibilidad o seguridad) son cruciales porque guían las decisiones de diseño, asegurando que la arquitectura soporte las necesidades reales del negocio.

 **5.¿Por qué Clean Architecture complementa ADD en la implementación de una solución?**

**R//:** Porque **Clean Architecture** organiza la implementación de manera modular y desacoplada, facilitando cumplir los atributos definidos en **ADD**. Por ejemplo, si se prioriza la escalabilidad, **Clean Architecture** permite cambiar la base de datos o agregar caching sin tocar la lógica de negocio.

 **6. ¿Qué criterios se deben considerar al definir las capas en Clean Architecture dentro de un proceso ADD?**
-   **Dominio:** Modelar las reglas de negocio esenciales sin depender de tecnologías externas.
-   **Aplicación:** Implementar casos de uso que reflejen las necesidades del negocio.
-   **Infraestructura:** Elegir tecnologías (como SQL o NoSQL) que optimicen atributos clave.
-   **Presentación:** Seleccionar interfaces que ofrezcan la mejor experiencia para los usuarios o sistemas externos.

**7. ¿Cómo ADD ayuda a tomar decisiones arquitectónicas basadas en necesidades del negocio?**

**R//: ADD** alinea la arquitectura con los objetivos del negocio priorizando atributos clave. Por ejemplo, si el negocio requiere alta disponibilidad, ADD puede sugerir replicar servicios y usar balanceadores de carga para garantizar tolerancia a fallos.

**8. ¿Cuáles son los beneficios de combinar ADD con Clean Architecture en un sistema basado en microservicios?**
-   **Optimización por calidad:** ADD asegura que cada microservicio cumpla atributos clave (p. ej., baja latencia).
-   **Desacoplamiento:** Clean Architecture facilita reemplazar componentes sin afectar el sistema completo.
-   **Escalabilidad:** Es fácil escalar microservicios horizontalmente o cambiar tecnologías sin modificar la lógica del negocio.

**9. ¿Cómo se asegura que la arquitectura resultante cumpla con los atributos de calidad definidos en ADD?**

**R//:** A través de pruebas específicas:
-   **Carga:** Para validar tiempos de respuesta.
-   **Penetración:** Para evaluar la seguridad.
-   **Failover:** Para garantizar la disponibilidad.  

Si no se cumplen los atributos, se optimiza la arquitectura (p. ej., agregando caching o ajustando la distribución de cargas).

**10. ¿Qué herramientas o metodologías pueden ayudar a validar una arquitectura diseñada con ADD y Clean Architecture?**
-   **Pruebas de rendimiento:** JMeter, k6.
-   **Monitoreo y logging:** Prometheus, Grafana.
-   **Análisis de arquitectura:** C4 Model, Diagrama de secuencia.
-   **Revisiones técnicas:** Análisis estático con SonarQube o CodeQL.
