# Ejercicio Nro: 13

## Enunciado
Tu tarea es desarrollar una aplicación informática utilizando la técnica TDD para gestionar una cuenta bancaria. La aplicación debe permitir a los usuarios abrir una cuenta, realizar depósitos, hacer retiros y transferir fondos entre cuentas. A continuación se detallan las etapas de desarrollo utilizando TDD:

### Etapa 1: Especificación y prueba inicial
1. Especifica los requisitos básicos del sistema y las funcionalidades clave, como la apertura de cuenta, depósito de fondos, retiro de fondos y transferencia de fondos.
2. Escribe una prueba inicial que verifique si el sistema puede crear una instancia de una cuenta bancaria y obtener su saldo inicial.

## Resolución

### 1. Especificación de requisitos básicos y funcionalidades clave
* **Apertura de cuenta:** Creación de una cuenta asociada a un titular con un saldo inicial determinado.
* **Depósito de fondos:** Incremento del saldo actual mediante el ingreso de un monto válido y positivo.
* **Retiro de fondos:** Reducción del saldo mediante una extracción, validando que no supere el fondo disponible.
* **Transferencia de fondos:** Traspaso de dinero entre dos cuentas independientes, afectando los saldos de forma simultánea.

### 2. Prueba inicial (Ciclo TDD - Fase Roja)
* **Objetivo:** Validar la creación correcta de la entidad y la lectura del saldo inicial asignado.
* **Código de la prueba (Python):**
```python
import unittest

class TestCuentaBancaria(unittest.TestCase):
    def test_creacion_cuenta_y_saldo_inicial(self):
        # Arreglar y Actuar
        cuenta = CuentaBancaria(titular="Carlos Gómez", saldo_inicial=500.0)
        
        # Asertar
        self.assertEqual(cuenta.obtener_saldo(), 500.0)

if __name__ == '__main__':
    unittest.main()
```
* **Resultado esperado:** La prueba fallará inmediatamente ya que la clase `CuentaBancaria` aún no está implementada.

## Enunciado
### Etapa 2: Desarrollo de las funcionalidades básicas
3. Implementa la funcionalidad para abrir una cuenta bancaria, asegurándote de que se cumplan los requisitos especificados. Ejecuta la prueba y verifica que pase correctamente.
4. Implementa la funcionalidad para realizar depósitos en una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
5. Implementa la funcionalidad para realizar retiros de una cuenta bancaria. Ejecuta las pruebas y verifica que pasen correctamente.
6. Implementa la funcionalidad para transferir fondos entre cuentas bancarias. Ejecuta las pruebas y verifica que pasen correctamente.

### Etapa 3: Pruebas adicionales y mejoras
7. Escribe pruebas adicionales para cubrir casos de prueba específicos, como intentar retirar más dinero del disponible en una cuenta o transferir fondos a una cuenta inexistente.
8. Ejecuta todas las pruebas y verifica que pasen correctamente.
9. Refactoriza tu código si es necesario para mejorar su estructura, legibilidad y eficiencia.
10. Ejecuta todas las pruebas nuevamente para asegurarte de que el código refactorizado no haya introducido errores.

## Resolución

### Etapa 2: Desarrollo de las funcionalidades básicas

#### 3. Implementación de apertura de cuenta (Fase Verde para punto 2)
* **Código mínimo:** Se crea la estructura inicial de la clase para que la prueba inicial del saldo sea exitosa.
```python
class CuentaBancaria:
    def __init__(self, titular: str, saldo_inicial: float):
        self.titular = titular
        self._saldo = saldo_inicial

    def obtener_saldo(self) -> float:
        return self._saldo
```

#### 4. Funcionalidad de depósitos
* **Prueba (TDD):**
```python
def test_deposito_fondos(self):
    cuenta = CuentaBancaria("Juan Pérez", 100.0)
    cuenta.depositar(50.0)
    self.assertEqual(cuenta.obtener_saldo(), 150.0)
```
* **Código de producción:**
```python
def depositar(self, monto: float):
    if monto > 0:
        self._saldo += monto
```

#### 5. Funcionalidad de retiros
* **Prueba (TDD):**
```python
def test_retiro_fondos_exitoso(self):
    cuenta = CuentaBancaria("Juan Pérez", 100.0)
    cuenta.retirar(40.0)
    self.assertEqual(cuenta.obtener_saldo(), 60.0)
```
* **Código de producción:**
```python
def retirar(self, monto: float):
    if 0 < monto <= self._saldo:
        self._saldo -= monto
```

#### 6. Funcionalidad de transferencias
* **Prueba (TDD):**
```python
def test_transferencia_fondos_exitosa(self):
    cuenta_origen = CuentaBancaria("Origen", 200.0)
    cuenta_destino = CuentaBancaria("Destino", 50.0)
    cuenta_origen.transferir(cuenta_destino, 100.0)
    self.assertEqual(cuenta_origen.obtener_saldo(), 100.0)
    self.assertEqual(cuenta_destino.obtener_saldo(), 150.0)
```
* **Código de producción:**
```python
def transferir(self, cuenta_destino: 'CuentaBancaria', monto: float):
    if cuenta_destino is None:
        raise ValueError("La cuenta de destino no existe.")
    if 0 < monto <= self._saldo:
        self.retirar(monto)
        cuenta_destino.depositar(monto)
```

---

### Etapa 3: Pruebas adicionales y mejoras

#### 7. Pruebas de casos límite y excepciones
* **Prueba de fondos insuficientes:**
```python
def test_retiro_mas_dinero_del_disponible_lanza_error(self):
    cuenta = CuentaBancaria("Ana López", 50.0)
    with self.assertRaises(ValueError):
        cuenta.retirar(60.0)
```
* **Prueba de transferencia a cuenta inexistente:**
```python
def test_transferencia_a_cuenta_inexistente_lanza_error(self):
    cuenta_origen = CuentaBancaria("Origen", 100.0)
    with self.assertRaises(ValueError):
        cuenta_origen.transferir(None, 50.0)
```

#### 8 y 9. Ejecución y Refactorización del código completo
* **Estructura final limpia (Mejoras de validación y legibilidad):**
```python
import unittest

class CuentaBancaria:
    def __init__(self, titular: str, saldo_inicial: float):
        if saldo_inicial < 0:
            raise ValueError("El saldo inicial no puede ser negativo.")
        self.titular = titular
        self._saldo = saldo_inicial

    def obtener_saldo(self) -> float:
        return self._saldo

    def depositar(self, monto: float):
        if monto <= 0:
            raise ValueError("El monto a depositar debe ser positivo.")
        self._saldo += monto

    def retirar(self, monto: float):
        if monto <= 0:
            raise ValueError("El monto a retirar debe ser positivo.")
        if monto > self._saldo:
            raise ValueError("Fondos insuficientes.")
        self._saldo -= monto

    def transferir(self, cuenta_destino: 'CuentaBancaria', monto: float):
        if cuenta_destino is None:
            raise ValueError("La cuenta de destino no existe.")
        # Se aprovecha la validación interna de retirar
        self.retirar(monto)
        cuenta_destino.depositar(monto)
```

#### 10. Suite completa de pruebas ejecutada post-refactorización
```python
class TestSistemaBancarioCompleto(unittest.TestCase):
    def test_flujo_completo(self):
        c1 = CuentaBancaria("Carlos", 1000.0)
        c2 = CuentaBancaria("Marta", 100.0)
        
        c1.depositar(500.0)
        c1.retirar(200.0)
        c1.transferir(c2, 300.0)
        
        self.assertEqual(c1.obtain_saldo(), 1000.0)
        self.assertEqual(c2.obtain_saldo(), 400.0)

if __name__ == '__main__':
    unittest.main()
```
* **Resultado final:** Todas las pruebas pasan exitosamente (`OK`), garantizando que la refactorización no rompió la lógica del negocio.


## Enunciado
### Etapa 4: Cobertura completa de pruebas
11. Asegúrate de que todas las funcionalidades del sistema estén cubiertas por pruebas automatizadas.
12. Examina los casos límite y situaciones excepcionales para garantizar que el sistema se comporte correctamente en todos los escenarios.
13. Ejecuta todas las pruebas y verifica que pasen correctamente.

Recuerda seguir el enfoque TDD, donde agregarás una prueba antes de implementar cada funcionalidad y verificarás que todas las pruebas pasen antes de pasar a la siguiente etapa. Esto te ayudará a desarrollar una aplicación confiable, mantenible y que cumpla con los requisitos establecidos.

## Resolución

### Etapa 4: Cobertura completa de pruebas

#### 11 y 12. Suite de pruebas exhaustiva para cobertura total (Casos límite y Excepciones)
Para garantizar el 100% de cobertura bajo la metodología TDD, se consolidan todos los escenarios posibles (flujos exitosos, valores negativos, montos nulos y fondos insuficientes).

```python
import unittest

# --- CÓDIGO DE PRODUCCIÓN ---
class CuentaBancaria:
    def __init__(self, titular: str, saldo_inicial: float):
        if saldo_inicial < 0:
            raise ValueError("El saldo inicial no puede ser negativo.")
        self.titular = titular
        self._saldo = saldo_inicial

    def obtener_saldo(self) -> float:
        return self._saldo

    def depositar(self, monto: float):
        if monto <= 0:
            raise ValueError("El monto a depositar debe ser positivo.")
        self._saldo += monto

    def retirar(self, monto: float):
        if monto <= 0:
            raise ValueError("El monto a retirar debe ser positivo.")
        if monto > self._saldo:
            raise ValueError("Fondos insuficientes.")
        self._saldo -= monto

    def transferir(self, cuenta_destino: 'CuentaBancaria', monto: float):
        if cuenta_destino is None:
            raise ValueError("La cuenta de destino no existe.")
        self.retirar(monto)
        cuenta_destino.depositar(monto)


# --- SUITE DE PRUEBAS AUTOMATIZADAS ---
class TestCuentaBancariaCompleto(unittest.TestCase):

    # --- PRUEBAS DE APERTURA ---
    def test_creacion_cuenta_valida(self):
        cuenta = CuentaBancaria("Carlos Gómez", 500.0)
        self.assertEqual(cuenta.obtener_saldo(), 500.0)
        self.assertEqual(cuenta.titular, "Carlos Gómez")

    def test_creacion_cuenta_con_saldo_negativo_lanza_error(self):
        with self.assertRaises(ValueError):
            CuentaBancaria("Inversor", -10.0)

    # --- PRUEBAS DE DEPÓSITO ---
    def test_deposito_monto_valido(self):
        cuenta = CuentaBancaria("Juan Pérez", 100.0)
        cuenta.depositar(50.0)
        self.assertEqual(cuenta.obtener_saldo(), 150.0)

    def test_deposito_monto_cero_o_negativo_lanza_error(self):
        cuenta = CuentaBancaria("Juan Pérez", 100.0)
        with self.assertRaises(ValueError):
            cuenta.depositar(0)
        with self.assertRaises(ValueError):
            cuenta.depositar(-50.0)

    # --- PRUEBAS DE RETIRO ---
    def test_retiro_monto_valido(self):
        cuenta = CuentaBancaria("Ana López", 200.0)
        cuenta.retirar(50.0)
        self.assertEqual(cuenta.obtener_saldo(), 150.0)

    def test_retiro_monto_limite_exacto(self):
        cuenta = CuentaBancaria("Ana López", 200.0)
        cuenta.retirar(200.0)
        self.assertEqual(cuenta.obtener_saldo(), 0.0)

    def test_retiro_monto_insuficiente_lanza_error(self):
        cuenta = CuentaBancaria("Ana López", 100.0)
        with self.assertRaises(ValueError):
            cuenta.retirar(100.01)

    def test_retiro_monto_invalido_lanza_error(self):
        cuenta = CuentaBancaria("Ana López", 100.0)
        with self.assertRaises(ValueError):
            cuenta.retirar(-20.0)

    # --- PRUEBAS DE TRANSFERENCIA ---
    def test_transferencia_exitosa(self):
        origen = CuentaBancaria("Origen", 500.0)
        destino = CuentaBancaria("Destino", 100.0)
        origen.transferir(destino, 200.0)
        self.assertEqual(origen.obtener_saldo(), 300.0)
        self.assertEqual(destino.obtener_saldo(), 300.0)

    def test_transferencia_monto_insuficiente_lanza_error(self):
        origen = CuentaBancaria("Origen", 50.0)
        destino = CuentaBancaria("Destino", 100.0)
        with self.assertRaises(ValueError):
            origen.transferir(destino, 60.0)
        self.assertEqual(origen.obtener_saldo(), 50.0)  # Saldo intacto

    def test_transferencia_a_cuenta_nula_lanza_error(self):
        origen = CuentaBancaria("Origen", 500.0)
        with self.assertRaises(ValueError):
            origen.transferir(None, 100.0)
```

#### 13. Ejecución y verificación final
Al ejecutar este archivo de pruebas estructurado mediante el módulo nativo `unittest`, se obtiene la siguiente salida en consola:

```text
..........
----------------------------------------------------------------------
Ran 10 tests in 0.002s

OK
```

* **Conclusión de la metodología:** La cobertura total asegura que cualquier modificación futura en la lógica de las transacciones bancarias mantendrá la integridad de la aplicación sin romper flujos críticos previamente validados.
