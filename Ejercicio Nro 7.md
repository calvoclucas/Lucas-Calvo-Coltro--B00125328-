# Ejercicio Nro: 7

## Enunciado
Dar un ejemplo de cada uno de los cuellos de botellas analizados anteriormente en el paper de Brooks

## Resolución

Brooks distingue entre dificultades accidentales (herramientas, lenguajes) y esenciales (la naturaleza del software). Los cuellos de botella reales son las Dificultades Esenciales:

1. Complejidad (Complexity)

Definición: El software es más complejo que cualquier otra construcción humana porque no hay dos partes iguales.
Ejemplo: En un sistema de gestión bancaria, un cambio en el módulo de "Intereses de Préstamos" puede afectar inesperadamente al módulo de "Reportes Fiscales" o al de "Límites de Tarjeta de Crédito". La cantidad de estados posibles es tan alta que es imposible prever todas las interacciones.

2. Conformidad (Conformity)

Definición: El software debe adaptarse (conformarse) a interfaces e instituciones que son arbitrarias y complejas por naturaleza humana, no por lógica.
Ejemplo: Un desarrollador crea una excelente aplicación de facturación, pero debe forzar su código a "conformarse" a las regulaciones impositivas cambiantes de un país o a los protocolos de comunicación anticuados de un servidor gubernamental externo. El software no puede ser simple porque la realidad a la que se conecta no lo es.

3. Variabilidad / Maleabilidad (Changeability)

Definición: A diferencia de un edificio, el software se percibe como algo infinitamente plástico y siempre está bajo presión para cambiar.
Ejemplo: Un sistema de e-commerce exitoso se expande. Ahora el cliente pide que también gestione stock físico, devoluciones internacionales y programas de puntos. El éxito del software inicial obliga a que sea modificado constantemente hasta que su diseño original se degrada.

4. Invisibilidad (Invisibility)

Definición: El software no tiene una existencia física espacial, lo que impide que nuestra mente visualice su estructura de forma geométrica completa.
Ejemplo: Al intentar explicar la arquitectura de una red social, un diagrama de flujo muestra el orden, pero no los datos; un modelo de datos muestra las relaciones, pero no el tiempo. No existe un solo "plano" que permita ver todo el software a la vez, lo que dificulta enormemente la comunicación entre los arquitectos del sistema.

