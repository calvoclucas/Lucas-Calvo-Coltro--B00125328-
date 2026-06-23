Flujo de Ejecución con Bots (Input/Output)
1) 🤖 BOT 3 (PO) — Prompt 1
BOT: Scrum-Bot-ProductOwner

INPUT (desde Cliente / requerimientos iniciales):

La empresa necesita una aplicación web para gestionar envíos y entregas.
Los clientes deben poder registrar pedidos.
Los operadores deben asignar transportistas.
Los usuarios deben rastrear envíos en tiempo real.
El sistema debe generar reportes de entregas.
Se requiere autenticación de usuarios y control de roles.
OUTPUT (Product Backlog priorizado en tabla):

ID	Historia de Usuario	Prioridad	Criterios de aceptación
HU-01	Como cliente quiero registrar pedidos para solicitar envíos	Alta	- El cliente puede crear un pedido con campos requeridos.<br>- El sistema valida obligatorios/formatos.<br>- El pedido queda persistido y visible.<br>- Confirmación de creación.
HU-02	Como usuario quiero iniciar sesión para acceder al sistema	Alta	- Autenticación con credenciales válidas.<br>- Sesión segura (JWT).<br>- Rutas protegidas requieren autenticación.<br>- Errores claros con credenciales inválidas.
HU-03	Como operador quiero asignar transportistas para gestionar entregas	Alta	- Operador asigna transportista a pedido disponible.<br>- Solo roles correctos pueden asignar.<br>- Estado del pedido pasa a “asignado”.<br>- Registro de cambios.
HU-04	Como cliente quiero rastrear envíos en tiempo real	Alta	- Visualiza estados del pedido.<br>- Actualizaciones reflejadas.<br>- Control de permisos por propietario del pedido.
HU-05	Como administrador quiero gestionar roles de usuarios	Media	- Admin crea/actualiza usuarios con roles.<br>- Autorización respeta roles.<br>- Auditoría básica.
HU-06	Como gerente quiero generar reportes de entregas	Media	- Genera reportes por rango/criterio.<br>- Autorización por rol.<br>- Manejo de “sin datos”.
2) 🤖 BOT 2 (Scrum Master) — Prompt 2
BOT: Scrum-Bot-Master

INPUT (desde PO / Product Backlog generado):

HU-01, HU-02, HU-03, HU-04 (Alta) y HU-05, HU-06 (Media) con criterios.
OUTPUT (Sprint 1 planificado, 2 semanas):

Objetivo del Sprint:
Implementar las funcionalidades básicas de autenticación y registro de pedidos.

Historias seleccionadas (prioridad alta y alcanzables):

HU-01 (Alta)
HU-02 (Alta)
Tabla de tareas:

Historia	Tarea	Responsable	Puntos Scrum
HU-01	Diseño de formulario de pedidos	Ana	3
HU-01	API de registro de pedidos	Carlos	5
HU-02	Pantalla de login	María	3
HU-02	Implementar autenticación JWT	Luis	5
3) 🤖 BOT 4 (Developer) — Prompt 3
BOT: Scrum-Bot-Developer

INPUT (desde Scrum Master / Plan del Sprint):

Tareas HU-01 y HU-02 con responsables y puntos.
OUTPUT (Informe técnico del incremento funcional):

Incremento de Software Funcional

Funcionalidades completadas:

Autenticación mediante JWT.
Pantalla de inicio de sesión.
Formulario de registro de pedidos.
API para almacenamiento de pedidos.
Impedimentos resueltos:

Problema de conexión a BD → ajuste de credenciales y verificación por ambiente.
Error de validación en formularios → alineación de reglas frontend/backend y mensajes.
Resumen del incremento:
Permite autenticar usuarios y registrar pedidos con persistencia, sentando base para rastreo y gestión posterior.

4) 🤖 BOT 1 (Cliente) — Prompt 4
BOT: Scrum-Bot-Cliente

INPUT (desde Dev / Incremento entregado):

JWT + pantalla login + registro pedidos + API persistente.
Impedimentos resueltos.
OUTPUT (Acta de Sprint Review):

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
Mejorar comunicación sobre cambios de requisitos.
Validar interfaces con usuarios antes del desarrollo.
5) 🤖 BOT 2 (Scrum Master) — Retrospectiva (Prompt 5)
BOT: Scrum-Bot-Master

INPUT (desde Cliente / retroalimentación + lecciones):

Positivos, mejoras, requerimientos y lecciones aprendidas.
OUTPUT (Plan de mejora continua para el siguiente Sprint):

Área	Acción de Mejora	Responsable	Métrica
Comunicación	Reuniones de refinamiento semanales	Scrum Master	90% asistencia
Calidad	Pruebas de usabilidad tempranas	Equipo QA	80% satisfacción usuarios
Requisitos	Validación con stakeholders antes del Sprint	Product Owner	Menos de 5 cambios por Sprint
Resultado final: plan para alimentar la planificación del Sprint siguiente.

6) (Opcional) 🤖 BOT 5 (PO-Clientes) — para encuestas (si lo piden)
BOT: Scrum-Bot-PO-Clientes

INPUT (desde Sprint Review / satisfacción 8/10):

Necesidades de mejora: recuperación contraseña, direcciones, notificaciones, historial.
OUTPUT (diseño de encuesta NPS + preguntas):