Prompt 1: Definición del Product Backlog
Entrada

Requerimientos iniciales del cliente:

La empresa necesita una aplicación web para gestionar envíos y entregas.
Los clientes deben poder registrar pedidos.
Los operadores deben asignar transportistas.
Los usuarios deben rastrear envíos en tiempo real.
El sistema debe generar reportes de entregas.
Se requiere autenticación de usuarios y control de roles.
Prompt
Actúa como Product Owner experto en Scrum.

Analiza los requerimientos iniciales proporcionados para una aplicación web de logística y genera un Product Backlog priorizado.

Para cada historia de usuario incluye:
- ID
- Historia de usuario en formato: "Como [usuario], quiero [funcionalidad] para [beneficio]"
- Prioridad (Alta, Media o Baja)
- Criterios de aceptación

Organiza las historias según valor de negocio y entrégalas en una tabla.
Salida Esperada
ID	Historia de Usuario	Prioridad
HU-01	Como cliente quiero registrar pedidos para solicitar envíos	Alta
HU-02	Como usuario quiero iniciar sesión para acceder al sistema	Alta
HU-03	Como operador quiero asignar transportistas para gestionar entregas	Alta
HU-04	Como cliente quiero rastrear envíos en tiempo real	Alta
HU-05	Como administrador quiero gestionar roles de usuarios	Media
HU-06	Como gerente quiero generar reportes de entregas	Media
Prompt 2: Planificación del Sprint
Entrada

Product Backlog generado en el Prompt 1.

Prompt
Actúa como Scrum Master.

Utilizando el Product Backlog recibido, planifica el Sprint 1 con una duración de dos semanas.

Selecciona las historias de usuario de mayor prioridad que puedan completarse durante el Sprint.

Para cada historia:
- Descompón el trabajo en tareas técnicas.
- Asigna un responsable.
- Estima el esfuerzo en puntos Scrum.

Presenta:
1. Objetivo del Sprint.
2. Historias seleccionadas.
3. Tabla de tareas con responsables y estimaciones.
Salida Esperada

Objetivo del Sprint:
Implementar las funcionalidades básicas de autenticación y registro de pedidos.

Historia	Tarea	Responsable	Puntos
HU-01	Diseño de formulario de pedidos	Ana	3
HU-01	API de registro de pedidos	Carlos	5
HU-02	Pantalla de login	María	3
HU-02	Implementar autenticación JWT	Luis	5
Prompt 3: Ejecución del Sprint
Entrada

Plan del Sprint generado en el Prompt 2.

Prompt
Actúa como equipo de desarrollo Scrum.

Con base en el Plan del Sprint proporcionado:

1. Ejecuta las tareas definidas.
2. Describe las funcionalidades desarrolladas.
3. Indica los impedimentos encontrados y cómo fueron resueltos.
4. Genera un resumen del incremento de software funcional entregado.

Presenta el resultado en formato de informe técnico.
Salida Esperada

Incremento de Software Funcional

Funcionalidades completadas:

Módulo de autenticación mediante JWT.
Pantalla de inicio de sesión.
Formulario de registro de pedidos.
API para almacenamiento de pedidos.

Impedimentos resueltos:

Problema de conexión a la base de datos solucionado mediante ajuste de credenciales.
Error de validación en formularios corregido.
Prompt 4: Revisión del Sprint
Entrada

Incremento de software funcional generado en el Prompt 3.

Prompt
Actúa como cliente y stakeholders durante la Sprint Review.

Evalúa el incremento de software entregado.

Genera:
- Comentarios positivos.
- Observaciones de mejora.
- Nuevos requerimientos identificados.
- Nivel de satisfacción (1 a 10).

Presenta la información como acta de revisión del Sprint.
Salida Esperada

Retroalimentación del Cliente

Aspectos positivos:

Inicio de sesión rápido y sencillo.
Registro de pedidos intuitivo.

Mejoras solicitadas:

Recuperación de contraseña.
Validación automática de direcciones.

Nuevos requerimientos:

Notificaciones por correo electrónico.
Historial de pedidos del cliente.

Nivel de satisfacción: 8/10

Lecciones aprendidas:

Mejorar la comunicación sobre cambios de requisitos.
Validar interfaces con usuarios finales antes del desarrollo.
Prompt 5: Retrospectiva del Sprint
Entrada

Retroalimentación del cliente y lecciones aprendidas generadas en el Prompt 4.

Prompt
Actúa como Scrum Master facilitando la Sprint Retrospective.

Analiza la retroalimentación del cliente y las lecciones aprendidas.

Genera:
1. Qué salió bien.
2. Qué puede mejorar.
3. Acciones concretas para el siguiente Sprint.
4. Responsables de cada acción.
5. Métricas para evaluar la mejora.

Presenta el resultado como un plan de mejora continua.
Salida Esperada
Área	Acción de Mejora	Responsable	Métrica
Comunicación	Reuniones de refinamiento semanales	Scrum Master	90% asistencia
Calidad	Pruebas de usabilidad tempranas	Equipo QA	80% satisfacción usuarios
Requisitos	Validación con stakeholders antes del Sprint	Product Owner	Menos de 5 cambios por Sprint

Resultado final: El plan de mejora generado servirá como entrada para la planificación del siguiente Sprint, manteniendo el ciclo iterativo de Scrum.