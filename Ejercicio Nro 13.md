# Ejercicio Nro: 13

## Enunciado
Responder el cuestionario sobre la metodología ágil Extreme Programming (XP) compuesto por 10 preguntas conceptuales y de aplicación práctica.

## Resolución

### 1. ¿Qué es Extreme Programming (XP) y cuál es su objetivo principal dentro de las metodologías ágiles?
* **Definición:** Es una metodología ágil de desarrollo de software centrada en la excelencia técnica y adaptabilidad.
* **Objetivo principal:** Minimizar el riesgo del proyecto reduciendo el costo del cambio ante requerimientos volátiles mediante software de alta calidad.

### 2. ¿Cuáles son los cinco valores principales de XP? Explicá brevemente cada uno.
* **Comunicación:** Fomentar el diálogo constante y verbal entre desarrolladores y clientes para evitar malentendidos.
* **Simplicidad:** Diseñar y codificar estrictamente lo necesario hoy, evitando complejidades para un futuro incierto.
* **Retroalimentación (Feedback):** Obtener opiniones inmediatas del sistema (pruebas) y del cliente (entregas) para corregir desvíos rápido.
* **Coraje (Valor):** Tomar decisiones difíciles, como refactorizar código obsoleto o descartar trabajo que ya no sirve.
* **Respeto:** Valorar las contribuciones de cada integrante del equipo y preservar la calidad del trabajo colectivo.

### 3. ¿Por qué XP considera que las pruebas son un elemento fundamental del desarrollo de software?
* **Red de seguridad:** Actúan como una garantía automática que valida que los cambios nuevos no rompan el sistema existente.
* **Documentación viva:** Los tests explican el comportamiento esperado del sistema de forma más clara que un manual de texto.
* **Confianza:** Permiten al equipo refactorizar y mejorar la estructura del código continuamente sin temor a introducir fallas.

### 4. ¿Qué es Test Driven Development (TDD) y cómo se relaciona con XP?
* **Definición:** Es una técnica de ingeniería de software donde se escriben las pruebas antes del código de producción.
* **Relación con XP:** Es una de sus prácticas técnicas fundamentales; implementa el ciclo *Rojo* (escribir prueba fallida), *Verde* (escribir código mínimo para que pase) y *Refactorizar* (limpiar el código).

### 5. ¿En qué consiste la práctica de Pair Programming? Mencioná dos ventajas y una posible dificultad.
* **Definición:** Práctica donde dos programadores trabajan juntos en una misma computadora: uno escribe el código (conductor) y el otro lo revisa en tiempo real (navegador).
* **Ventaja 1:** Inspección de código continua que reduce drásticamente la cantidad de errores de diseño y sintaxis.
* **Ventaja 2:** Difusión inmediata del conocimiento técnico y del negocio entre los miembros del equipo.
* **Dificultad:** Puede generar fatiga mental temprana o roces de personalidad si no hay una buena dinámica de comunicación.

### 6. ¿Qué son las historias de usuario en XP y por qué se prefieren frente a una especificación extensa de requisitos?
* **Definición:** Tarjetas breves escritas en lenguaje simple que describen una necesidad específica que aporta valor al usuario.
* **Razón de preferencia:** Promueven la conversación directa en lugar de la interpretación pasiva de un documento estático, adaptándose mejor a los cambios constantes.

### 7. ¿Qué significa Continuous Integration en XP y qué beneficios aporta al equipo de desarrollo?
* **Definición:** Práctica de unificar el código de todos los desarrolladores en una rama principal varias veces al día de forma automatizada.
* **Beneficio 1:** Detección e integración temprana de conflictos de código, evitando sorpresas al final del ciclo.
* **Beneficio 2:** Automatización de pruebas y despliegues, garantizando que el sistema siempre esté en un estado funcional estable.

### 8. ¿Cómo se aplica el concepto de Weekly Cycle en un proyecto desarrollado con XP?
* **Aplicación:** Al inicio de la semana se reúne el equipo con el cliente para revisar el progreso del software funcionando. El cliente selecciona las historias de usuario prioritarias para esa semana y los desarrolladores las descomponen en tareas técnicas que se comprometen a terminar en esos 7 días.

### 9. En XP se plantea que se fija el tiempo, el costo y la calidad, y se negocia el alcance. ¿Qué significa esta idea? Explicalo con un ejemplo.
* **Significado:** El tiempo (fecha de entrega), el presupuesto y la excelencia técnica no se comprometen. Si surgen retrasos o nuevos requerimientos, lo único que puede variar es la cantidad de funcionalidades (alcance) que se entregarán en esa iteración.
* **Ejemplo:** En un sistema de inventario web, si llega la fecha límite y el equipo se retrasa por problemas técnicos, la calidad no se baja (no se omiten pruebas) ni se estira el tiempo; en su lugar, se acuerda con el cliente entregar la funcionalidad "Agregar producto" y postergar "Exportar a PDF" para la siguiente semana.

### 10. Elegí tres prácticas de XP y explicá cómo podrían aplicarse en un proyecto real de desarrollo de software.
* **Práctica 1: Refactoring (Refactorización):** En una app de comercio electrónico, mejorar continuamente la estructura de la base de datos y la legibilidad de las consultas SQL cada vez que se agrega un método de pago, asegurando que el sistema no se vuelva lento con el tiempo.
* **Práctica 2: Pequeñas Entregas (Small Releases):** En un sistema de gestión escolar, desplegar primero la funcionalidad de "Visualización de notas" al finalizar el primer mes, en lugar de esperar a terminar los módulos de asistencia, pagos y horarios.
* **Práctica 3: Cliente en el Sitio (On-site Customer):** Incluir de forma presencial o con disponibilidad virtual absoluta a un analista del negocio o usuario clave en los canales de comunicación del equipo de desarrollo, respondiendo dudas sobre las reglas de negocio de inmediato durante la jornada laboral.
