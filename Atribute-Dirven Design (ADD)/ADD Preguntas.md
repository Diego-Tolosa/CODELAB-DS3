# CODELAB: ATRIBUTE-DRIVEN DESIGN (ADD)

## Preguntas

 **1. ¿Cuál es el propósito principal de la metodología ADD en el diseño de arquitecturas de software?**

**R//: ** El propósito principal de ADD (Attribute-Driven Design) es proporcionar un marco estructurado para la toma de decisiones arquitectónicas basadas en los **atributos de calidad** del sistema. ADD asegura que el diseño no solo cumpla con los requisitos funcionales, sino que también optimice aspectos como el rendimiento, escalabilidad, seguridad, mantenibilidad y disponibilidad. Esto permite anticipar problemas y reducir riesgos desde las primeras fases del desarrollo. 

**2. ¿Qué atributos de calidad se consideran en ADD y por qué son importantes en el proceso de diseño?**

Los atributos de calidad más comunes en ADD incluyen:

-   **Rendimiento**: Capacidad del sistema para responder rápidamente.
-   **Escalabilidad**: Capacidad de manejar crecimiento en carga o usuarios.
-   **Seguridad**: Protección de datos y acceso no autorizado.
-   **Disponibilidad**: Tiempo de operación sin interrupciones.
-   **Mantenibilidad**: Facilidad para realizar cambios o correcciones.

Estos atributos son importantes porque definen la  **calidad del software**  y su capacidad para satisfacer las necesidades del negocio y los usuarios. ADD prioriza estos atributos para garantizar que el sistema sea robusto, eficiente y adaptable.

 **3. Explica la importancia de la selección del módulo a diseñar en ADD. ¿Cuáles son los criterios principales para elegir un módulo?**

La selección del módulo es crucial porque permite enfocar el diseño en áreas críticas del sistema, optimizando recursos y tiempo. Los criterios principales para elegir un módulo son:

-   **Dependencias**: Módulos que interactúan con muchos otros.
-   **Riesgos arquitectónicos**: Módulos críticos en rendimiento, seguridad o escalabilidad.
-   **Prioridades del negocio**: Módulos que impactan directamente en los objetivos del proyecto.
-   **Complejidad y viabilidad técnica**: Módulos que el equipo puede implementar eficientemente.

**4. ¿Cómo influyen las tácticas arquitectónicas en la toma de decisiones dentro de ADD? Menciona dos ejemplos de tácticas y su aplicación.**

Las tácticas arquitectónicas son estrategias técnicas que ayudan a cumplir con los atributos de calidad. Influyen en la toma de decisiones al proporcionar soluciones específicas para problemas comunes. Dos ejemplos son:

-   **Caché**: Mejora el rendimiento al almacenar datos frecuentemente accedidos, reduciendo la carga en servidores.
-   **Balanceo de carga**: Aumenta la escalabilidad y disponibilidad al distribuir el tráfico entre múltiples servidores.

 **5. ¿Cuál es la relación entre los escenarios de calidad y la evaluación de la arquitectura en ADD?**

Los escenarios de calidad son herramientas para evaluar si la arquitectura cumple con los atributos de calidad. Estos escenarios definen:

-   **Estímulo**: Evento que activa una respuesta.
-   **Respuesta esperada**: Comportamiento del sistema ante el estímulo.
-   **Medida de respuesta**: Criterios para evaluar si se cumplen los atributos.

Durante la evaluación, se verifica si la arquitectura satisface estos escenarios, asegurando que las decisiones tomadas sean efectivas.

 **6. Describe los principales pasos del proceso ADD y cómo se interrelacionan.**

Los pasos principales de ADD son:

1.  **Identificar atributos de calidad**: Define qué aspectos son críticos para el sistema.
2.  **Seleccionar módulo a diseñar**: Enfoca el diseño en áreas clave.
3.  **Seleccionar tácticas arquitectónicas**: Elige estrategias para cumplir con los atributos.
4.  **Definir la arquitectura**: Estructura los componentes y sus interacciones.
5.  **Evaluar y documentar**: Valida el diseño y registra las decisiones.

Estos pasos son iterativos y se interrelacionan para garantizar que cada decisión esté alineada con los atributos de calidad.

**7. ¿Por qué es crucial documentar las decisiones arquitectónicas en ADD? Menciona al menos tres elementos que deben incluirse en la documentación.**

Documentar las decisiones es crucial porque:
-   Facilita la comunicación entre equipos.
-   Permite reutilizar estrategias en futuros proyectos.
-   Asegura la coherencia durante el desarrollo y mantenimiento.

Elementos clave de la documentación:
1.  **Diagramas de arquitectura**: Representación visual de componentes y conexiones.
2.  **Decisiones arquitectónicas**: Justificación de las tácticas y estrategias seleccionadas.
3.  **Escenarios de calidad evaluados**: Resultados de las pruebas y validaciones.

**8. En un proyecto real, ¿Cómo se puede evaluar si una arquitectura diseñada con ADD cumple con los atributos de calidad esperados?**

Se puede evaluar mediante:

-   **Pruebas de concepto (PoC)**: Implementación de prototipos para simular condiciones reales.
-   **Análisis de escenarios de calidad**: Verificación de que la arquitectura responde adecuadamente a los estímulos definidos.
-   **Revisión técnica**: Discusión con el equipo para identificar posibles mejoras o problemas.
-   **Modelado y simulación**: Uso de herramientas para predecir el comportamiento del sistema bajo carga.

**9. ¿Cuáles son los beneficios de utilizar ADD en comparación con otros enfoques de diseño arquitectónico?**

Los beneficios de ADD incluyen:

-   **Enfoque en atributos de calidad**: Prioriza aspectos no funcionales desde el inicio.
-   **Estructura iterativa**: Permite refinamientos continuos y adaptación a cambios.
-   **Documentación clara**: Facilita la comprensión y reutilización de decisiones.
-   **Reducción de riesgos**: Anticipa problemas antes de la implementación.

En comparación con otros enfoques, ADD es más sistemático y orientado a la calidad del software.

**10. ¿Qué desafíos pueden surgir al aplicar ADD en un equipo de desarrollo y cómo podrían abordarse?**

Desafíos comunes:

-   **Complejidad del proceso**: ADD puede ser difícil de implementar en equipos sin experiencia.  
    **Solución**: Capacitar al equipo y comenzar con proyectos pequeños.
    
-   **Falta de priorización de atributos**: Puede haber desacuerdos sobre qué atributos son más importantes.  
    **Solución**: Involucrar a todas las partes interesadas (stakeholders) en la definición de prioridades.
    
-   **Documentación insuficiente**: Si no se documenta adecuadamente, se pierde la trazabilidad de las decisiones.  
    **Solución**: Establecer estándares claros de documentación y asignar responsables.

