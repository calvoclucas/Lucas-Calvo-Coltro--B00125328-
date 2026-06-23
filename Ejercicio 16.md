# Ejercicios Prácticos de Scrum - Ejercicio 16

**Materia:** Metodologías Ágiles  
**Tema:** Método Delphi para Selección de Arquitectura y Tecnología

---

## 📋 APLICACIÓN DEL MÉTODO DELPHI: BILLETERA VIRTUAL

### 1. Definición del Panel de Expertos (Anonimato Garantizado)
Para garantizar una evaluación multidimensional sin sesgos de autoridad, se conforma un panel con 4 perfiles especialistas externos:
*   **Experto A:** Arquitecto de Sistemas Cloud (Especialista en escalabilidad y microservicios).
*   **Experto B:** Ingeniero en Ciberseguridad (Especialista en criptografía y normativas financieras).
*   **Experto C:** Desarrollador Senior Blockchain (Especialista en contratos inteligentes y redes distribuidas).
*   **Experto D:** Líder de Desarrollo de Software (Especialista en integración continua y metodologías ágiles).

---

## ⚙️ FASES DE LA CONSULTA ESTRUCTURADA

### Ronda 1: Consulta Abierta e Identificación de Alternativas
Se envía un cuestionario abierto a los expertos de forma individual y anónima.

*   **Pregunta formulada:** ¿Qué tecnologías, bases de datos y arquitectura garantizan la máxima seguridad, escalabilidad y confiabilidad para una billetera virtual?
*   **Resultados consolidados (Respuestas de la Ronda 1):**
    *   *Arquitectura:* Coincidencia en arquitectura basada en microservicios desacoplados.
    *   *Base de Datos:* Propuestas divididas entre bases de datos relacionales tradicionales (PostgreSQL) para transacciones contables y bases NoSQL (MongoDB) para bitácoras e historial dinámico.
    *   *Seguridad/Blockchain:* Propuestas de uso de redes distribuidas públicas (Ethereum/Polygon) vs. redes privadas empresariales (Hyperledger Fabric) para la inmutabilidad de los registros.

### Ronda 2: Evaluación y Filtrado de Opciones (Búsqueda de Convergencia)
El facilitador tabula las opciones de la Ronda 1 y envía un segundo cuestionario estructurado para que los expertos puntúen del 1 al 5 las alternativas más viables.

*   **Resultados de la votación (Ronda 2):**
    *   *Arquitectura de Microservicios:* 4.8 / 5 (Consenso casi total por su alta tolerancia a fallos).
    *   *Hyperledger Fabric (Blockchain Privada):* 4.5 / 5 (Superó a las redes públicas debido a los menores costos de transacción por gas, mayor velocidad de procesamiento y cumplimiento regulatorio estricto).
    *   *PostgreSQL (Con transacciones ACID nativas):* 4.7 / 5 (Elegida sobre NoSQL para el núcleo financiero por su consistencia e integridad de datos matemáticos).

### Ronda 3: Debate Anónimo de Desviaciones y Consenso Final
Se presentan los gráficos estadísticos a los expertos. Se les solicita reevaluar su postura o justificar detalladamente si mantienen una opinión alejada del promedio del grupo. 

*   *Discusión técnica:* El Experto B (Seguridad) inicialmente prefería bases de datos distribuidas puras, pero tras analizar los argumentos de rendimiento del Experto A (Cloud), acepta que una arquitectura híbrida (PostgreSQL centralizado + Hyperledger para auditoría inmutable) es óptima.

---

## 🚀 RESULTADO DE CONSENSO (Salida Técnica del Ejercicio)

Gracias al Método Delphi, se alcanza un consenso técnico sin confrontaciones directas, definiendo la siguiente pila tecnológica para la billetera virtual:

*   **Patrón de Arquitectura:** Microservicios desplegados en contenedores (Docker/Kubernetes) para asegurar la escalabilidad horizontal e independencia de módulos (Módulo de Pagos, Módulo de Autenticación, Módulo de Notificaciones).
*   **Capa de Datos Transaccional:** **PostgreSQL** con replicación activa, garantizando consistencia absoluta y transacciones ACID obligatorias para evitar saldos duplicados o inconsistentes.
*   **Capa de Auditoría y Seguridad:** **Hyperledger Fabric** para registrar de forma inmutable la trazabilidad de los movimientos de fondos de alto valor, blindando el sistema contra fraudes internos.
*   **Capa de Autenticación:** Mecanismos de doble factor (2FA), cifrado AES-256 en reposo y tránsito de datos, y validación mediante tokens JWT seguros.
