# Ejercicios Prácticos de Scrum - Metodologías Ágiles

**Materia:** Metodologías Ágiles  
**Tema:** Scrum Framework  
**Tipo:** Ejercicios Prácticos  
**Archivo:** Apellido-Nombre.pdf  

---

## EJERCICIOS CONCEPTUALES

### Ejercicio 1: Identificación de Roles

* **a) Un stakeholder quiere agregar una nueva funcionalidad urgente durante el Sprint**
  * **Rol:** Product Owner.
  * **Justificación:** Gestiona el Product Backlog en exclusividad. Protege al equipo de interrupciones externas.
* **b) El equipo no entiende claramente un requisito del Product Backlog**
  * **Rol:** Product Owner.
  * **Justificación:** Es responsable de expresar claramente los elementos. Debe clarificar el "qué" al equipo.
* **c) Hay conflictos entre desarrolladores sobre la implementación técnica**
  * **Rol:** Development Team.
  * **Justificación:** Es un equipo autogestionado y autónomo. Define internamente el "cómo" del trabajo.
* **d) Se necesita decidir el orden de prioridad de las User Stories**
  * **Rol:** Product Owner.
  * **Justificación:** Tiene la autoridad final sobre el orden. Maximiza el valor del producto entregado.
* **e) El equipo está teniendo problemas para cumplir con la Definition of Done**
  * **Rol:** Scrum Master.
  * **Justificación:** Actúa como coach del proceso Scrum. Facilita la mejora continua del equipo.

---

### Ejercicio 2: Artefactos de Scrum

| Artefacto | ¿Qué SÍ contiene? | ¿Qué NO debería contener? |
| :--- | :--- | :--- |
| **Product Backlog** | Lista ordenada de funcionalidades futuras. | Tareas técnicas detalladas por horas. |
| **Sprint Backlog** | Sprint Goal e historias seleccionadas. | Requisitos no aprobados por PO. |
| **Increment** | Historias que cumplen el DoD. | Código incompleto sin pruebas hechas. |

---

### Ejercicio 3: Eventos de Scrum - Verdadero o Falso

* **V** | La Sprint Planning puede durar hasta 8 horas para un Sprint de 4 semanas.  
  * *Justificación:* Es el Time-box máximo oficial.
* **F** | En la Daily Scrum cada miembro debe reportar al Scrum Master.  
  * *Justificación:* Es un evento para los desarrolladores.
* **F** | La Sprint Review es solo para demostrar el producto al Product Owner.  
  * *Justificación:* Participan también activamente los stakeholders externos.
* **F** | En la Sprint Retrospective se puede modificar el Sprint Backlog.  
  * *Justificación:* Modifica procesos para el próximo Sprint.
* **F** | El Sprint puede cancelarse solo por decisión del Development Team.  
  * *Justificación:* Solo el Product Owner lo cancela.

---

## EJERCICIOS DE APLICACIÓN

### Ejercicio 4: Creación de Product Backlog (App Delivery)

#### Tabla de User Stories y Estimación

| ID | User Story (Como... quiero... para...) | SP | Prioridad |
| :--- | :--- | :--- | :--- |
| **US-01** | Como usuario, quiero registrarme con mi correo para guardar mi historial. | 3 | 1 |
| **US-02** | Como usuario, quiero ver restaurantes cercanos para elegir dónde comprar. | 5 | 2 |
| **US-03** | Como usuario, quiero agregar platos al carrito para armar mi pedido. | 5 | 3 |
| **US-04** | Como usuario, quiero pagar con tarjeta de crédito para concretar la compra. | 8 | 4 |
| **US-05** | Como repartidor, quiero ver la dirección en mapa para entregar rápido. | 8 | 5 |
| **US-06** | Como usuario, quiero calificar la comida para dejar mi opinión. | 3 | 6 |
| **US-07** | Como administrador, quiero ver un panel de ventas para controlar el negocio. | 13 | 7 |
| **US-08** | Como usuario, quiero aplicar cupones de descuento para ahorrar dinero. | 5 | 8 |

#### Criterios de Aceptación (Top 3 Prioridades)

* **US-01: Registro de usuario**
  * Validar formato de email del usuario.
  * Contraseña de mínimo 8 caracteres alfanuméricos.
  * Enviar correo de confirmación de cuenta.
* **US-02: Ver restaurantes cercanos**
  * Solicitar permiso de ubicación GPS móvil.
  * Listar comercios dentro de 5 kilómetros.
  * Mostrar etiqueta en tiempo real abierto/cerrado.
* **US-03: Carrito de compras**
  * Permitir modificar cantidades en el carrito.
  * Recalcular montos totales de forma inmediata.
  * Retener productos al cerrar la app.

---

### Ejercicio 5: Planning Poker Simulation

* **Paso 1:** El PO expone la historia de pago con tarjeta.
* **Paso 2:** Votación inicial ciega: un desarrollador Jr vota 3 SP y el Senior vota 13 SP.
* **Paso 3:** Debate técnico sobre normativas de seguridad PCI-DSS y gestión de errores.
* **Paso 4:** Segunda votación con consenso final del equipo fijado en 8 SP.

---

### Ejercicio 6: Sprint Planning Práctico

* **Capacidad disponible:** 40 Story Points.
* **Selección de Historias (Sprint Backlog):**
  * Historia B (13 SP - Prioridad Alta)
  * Historia A (8 SP - Prioridad Alta)
  * Historia D (8 SP - Prioridad Media)
  * Historia C (5 SP - Prioridad Media)
  * Historia E (3 SP - Prioridad Baja)
  * *Total acumulado:* 37 Story Points.
* **Sprint Goal:** "Permitir buscar comercios, gestionar el carrito y pagar de forma segura".
* **Descomposición en tareas específicas (Historia B - 13 SP):**
  * Diseñar interfaces de pasarela de pago.
  * Configurar endpoints e integración de API.
  * Programar lógica backend de transacciones.
  * Desarrollar pruebas unitarias de pago.
* **Impedimentos y riesgos identificados:**
  * Demora en credenciales del proveedor externo.
  * Caídas en servidores de testing externos.

---

### Ejercicio 7: Simulación de Daily Scrum

* **Desarrollador 1 (Tarjeta 1):**
  * *Ayer:* Terminé la tarea de login.
  * *Hoy:* Trabajaré en registro de usuarios.
  * *Impedimentos:* Ninguno.
* **Desarrollador 2 (Tarjeta 2):**
  * *Ayer:* Trabajé en base de datos.
  * *Hoy:* Optimizaré consultas con el DBA.
  * *Impedimentos:* Bloqueado por problemas de performance.
* **Desarrollador 3 (Tarjeta 3):**
  * *Ayer:* Completé las pruebas unitarias.
  * *Hoy:* Empiezo con la integración técnica.
  * *Impedimentos:* Ninguno.
* **Desarrollador 4 (Tarjeta 4):**
  * *Ayer:* Intenté conectar el backend transaccional.
  * *Hoy:* Investigar errores de red alternativos.
  * *Impedimentos:* Bloqueado esperando la API externa.
* **Desarrollador 5 (Tarjeta 5):**
  * *Ayer:* Terminé asignación de UI temprano.
  * *Hoy:* Apoyar tareas de mis compañeros.
  * *Impedimentos:* Ninguno.

---

### Ejercicio 8: Sprint Review y Retrospective

#### Parte A - Sprint Review
* **Agenda de la Reunión (2 horas):**
  * 14:00 - 14:15 | Bienvenida y repaso del Sprint Goal.
  * 14:15 - 15:05 | Demo en vivo del incremento (35 SP).
  * 15:05 - 15:45 | Feedback directo con los stakeholders.
  * 15:45 - 16:00 | Revisión y adaptación del Product Backlog.
* **Métricas a presentar:** Velocidad real lograda (35 SP) y tasa de cumplimiento (87.5%).
* **Preguntas para Stakeholders:** ¿El flujo del carrito resulta amigable? ¿Es intuitivo?
* **Plan para historias no completadas:** Vuelven directo al Product Backlog general.

#### Parte B - Sprint Retrospective (Técnica "Start, Stop, Continue")
* **Start (Empezar a hacer):**
  * Hacer refinamientos de backlog más profundos.
  * Crear matriz de conocimiento cruzado interno.
  * Filtrar cambios mediante el Product Owner.
* **Stop (Dejar de hacer):**
  * Iniciar desarrollos sin criterios de aceptación.
  * Omitir fases críticas de testing técnico.
* **Continue (Continuar haciendo):**
  * Mantener los canales abiertos de comunicación.

---

### Ejercicio 9: Manejo de Impedimentos

#### 1. El PO no está disponible para aclarar dudas
* **Tipo:** Organizacional y de Proceso.
* **Estrategias:** Pactar bloques diarios de atención. Avanzar temporalmente con supuestos lógicos.
* **Quién actúa:** Scrum Master y PO.
* **Seguimiento:** Validar tiempos de respuesta diarios.

#### 2. Un desarrollador senior está sobrecargado
* **Tipo:** Capacidad y Estructura Interna.
* **Estrategias:** Implementar sesiones de Pair Programming. Eliminar la asignación de módulos exclusivos.
* **Quién actúa:** Equipo de Desarrollo.
* **Seguimiento:** Revisar distribución de tareas semanalmente.

#### 3. Las herramientas de desarrollo fallan constantemente
* **Tipo:** Técnico e Infraestructura.
* **Estrategias:** Detener desarrollos para estabilizar entornos. Elevar reclamo formal a DevOps.
* **Quién actúa:** Equipo de Desarrollo.
* **Seguimiento:** Medir recurrencia en las Dailys.

#### 4. Hay conflictos interpersonales en el equipo
* **Tipo:** Humano / Dinámica Interna.
* **Estrategias:** Tener sesiones individuales de escucha. Facilitar dinámicas de acuerdos mutuos.
* **Quién actúa:** Scrum Master.
* **Seguimiento:** Evaluar el clima en Retrospectiva.

#### 5. Un stakeholder presiona para agregar funcionalidades
* **Tipo:** Externo / Alcance del Sprint.
* **Estrategias:** Derivar stakeholder con el PO. Blindar el foco del equipo.
* **Quién actúa:** Scrum Master y PO.
* **Seguimiento:** Monitorear estabilidad del Sprint Backlog.

---

### Ejercicio 10: Definición de Terminado (Definition of Done - DoD)

#### 1. Criterios Técnicos
* Código compilado sin errores críticos.
* Integración correcta en rama principal.

#### 2. Criterios de Calidad
* **Revisión por pares:** Pull Request aprobado por otro desarrollador.
* **Pruebas automatizadas:** Cobertura de tests unitarios al 80%.
* **Performance:** Tiempos de carga menores a 2 segundos.
* **Accesibilidad:** Cumplimiento básico de pautas WCAG.
* **Seguridad:** Datos sensibles de pago encriptados (OWASP).

#### 3. Criterios de Documentación
* Actualizar diagramas técnicos en wiki.
* Documentar endpoints de APIs (Swagger).

#### 4. Criterios de Validación
* Despliegue exitoso en entorno Staging.
* Revisión visual y aprobación del PO.

---

## EVALUACIÓN Y REFLEXIÓN

1. **Principales desafíos:** Unificar estimaciones entre perfiles y mitigar interrupciones de alcance externas.
2. **Beneficios del trabajo colaborativo:** Descentraliza el conocimiento técnico y reduce riesgos arquitectónicos tempranamente.
3. **Adaptación a proyecto real:** Sprints fijos de 2 semanas con refinamientos del backlog semanales.