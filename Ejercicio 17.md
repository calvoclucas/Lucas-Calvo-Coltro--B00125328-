# Ejercicios Prácticos de Scrum - Ejercicio 17

**Materia:** Metodologías Ágiles  
**Tema:** Estimación de Software con Método COSMIC 

---

## 📋 ANÁLISIS SINTÉTICO DE REQUISITOS (Mapeo COSMIC)

Para calcular el tamaño funcional del proyecto según las reglas del estándar COSMIC (ISO/IEC 19761), se identifican los movimientos de datos básicos: **Entradas (E)**, **Salidas (X)**, **Lecturas (R)** y **Escrituras (W)**. Cada movimiento equivale a 1 Punto de Función COSMIC (PFC).

### 1. Gestión de Cuentas Bancarias
*   Creación y edición de cuentas (1E, 1W) = 2 PFC
*   Visualización de saldo e historial (1E, 1R, 1X) = 3 PFC
*   Transferencias entre cuentas propias (1E, 2R, 2W, 1X) = 6 PFC
*   Descargar historial en CSV/PDF (1E, 1R, 1X) = 3 PFC

### 2. Gestión de Ingresos y Gastos
*   Creación y edición de movimientos (1E, 1W) = 2 PFC
*   Categorización por tipos (1E, 1R, 1W) = 3 PFC
*   Visualización de gráficos y reportes (1E, 2R, 1X) = 4 PFC
*   Establecer alertas de presupuestos (1E, 1W) = 2 PFC

### 3. Gestión de Deudas
*   Creación y edición de deudas/cuotas (1E, 1W) = 2 PFC
*   Calendario y simulación de escenarios (1E, 2R, 1X) = 4 PFC
*   Generación de informes de progreso (1E, 1R, 1X) = 3 PFC

---

## 🛠️ RESOLUCIÓN

### Estimación del tamaño del proyecto:
Utilizando el método COSMIC, se estima que el tamaño funcional total del proyecto es de **34 Puntos de Función COSMIC (PFC)**.

### Cálculo del costo por punto de función:
El costo por punto de función (CPFC) se estima en **250 USD** *(Valor de referencia estándar de mercado regional para desarrollo de software ágil seguro)*.

### Cantidad de puntos de función que se pueden hacer en un mes:
Se estima que un equipo de desarrollo de software de **4 personas** puede desarrollar **17 Puntos de Función COSMIC (PFC)** por mes *(Basado en una tasa de productividad promedio de 4.25 PFC por desarrollador-mes en aplicaciones web financieras)*.

### Duración del proyecto:
La duración del proyecto se estima en **2 meses** *(Cálculo: 34 PFC / 17 PFC mensuales)*.

### Costo del proyecto:
El costo total del proyecto se estima en **8.500 USD** *(Cálculo: 34 PFC × 250 USD)*.
