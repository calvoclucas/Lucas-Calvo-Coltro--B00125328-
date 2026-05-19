# Ejercicio Nro: 9

## Enunciado
Teniendo en cuenta los nuevos conceptos y habilidades aprendidas del proceso unificado, realiza las mejoras que considere necesario del trabajo práctico del Ejercicio 8.

## Resolución
Las mejoras aplicadas incorporan la trazabilidad estricta que exige el Proceso Unificado (UP), vinculando la lógica de negocio modelada en el Ejercicio 8 (Diagramas de Secuencia y Clases de Diseño) con una estrategia de pruebas unitarias automatizadas por capas y manejo de excepciones robusto.

### 1. Pruebas Unitarias para la Capa de Datos (Repositorio / Entidades)
* **Caso de Prueba 1.1: Persistencia exitosa**
  * **Objetivo:** Verificar que la entidad `Producto` se guarda correctamente en la base de datos.
  * **Entrada:** Objeto `Producto` con datos válidos (Nombre: "Teclado", Stock: 50, Precio: 25.00).
  * **Resultado Esperado:** El método retorna el objeto con un identificador (`ID`) único generado.
* **Caso de Prueba 1.2: Restricción de unicidad**
  * **Objetivo:** Validar que el sistema impida duplicados basados en el código de barra o SKU.
  * **Entrada:** Insertar un producto con un código identificador que ya existe en el sistema.
  * **Resultado Esperado:** El sistema lanza una excepción de persistencia (`DataIntegrityViolationException`).

### 2. Pruebas Unitarias para la Capa de Lógica de Negocio (Servicios / Clases de Control)
* **Caso de Prueba 2.1: Validación de reglas de negocio (Campos críticos)**
  * **Objetivo:** Garantizar que el sistema rechace productos con valores monetarios o de inventario ilógicos.
  * **Entrada:** Objeto `Producto` con precio negativo (`-5.00`) o nombre vacío.
  * **Resultado Esperado:** El servicio detiene la ejecución y lanza una excepción personalizada de negocio (`InvalidProductException`).
* **Caso de Prueba 2.2: Asignación de valores por defecto**
  * **Objetivo:** Verificar las post-condiciones del caso de uso cuando se omiten campos opcionales.
  * **Entrada:** Registro de un producto nuevo sin especificar el stock inicial.
  * **Resultado Esperado:** La capa de negocio intercepta el valor nulo y le asigna automáticamente un stock inicial de `0`.

### 3. Pruebas Unitarias para la Capa de Presentación (Controladores de la API / Interfaces)
* **Caso de Prueba 3.1: Enrutamiento y respuesta exitosa (HTTP 201)**
  * **Objetivo:** Asegurar que el endpoint responde con los estándares REST correctos aislando la base de datos (usando Mocks).
  * **Entrada:** Petición HTTP POST a `/api/productos` con formato JSON correcto.
  * **Resultado Esperado:** Retorno de código de estado HTTP 201 (Created) y el cuerpo con el recurso creado.
* **Caso de Prueba 3.2: Control de formato erróneo (HTTP 400)**
  * **Objetivo:** Validar el comportamiento del sistema ante peticiones malformadas desde el cliente web.
  * **Entrada:** Petición HTTP POST con una estructura JSON rota o vacía `{}`.
  * **Resultado Esperado:** Código de estado HTTP 400 (Bad Request) junto con los mensajes de error detallados de los campos faltantes.
