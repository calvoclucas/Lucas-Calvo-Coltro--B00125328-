# Ejercicio Nro: 5

## Enunciado
Proponga cinco elementos que ayuden en el desarrollo de software referido a la propiedad de flexibilidad que se requiere. 

Ejemplo: 
Diseño para el cambio, 
Ocultamiento de la Información, 
Herramientas de especificación
Etc.


## Resolución

Para lograr un software flexible que permita evolucionar ante nuevos requisitos o cambios en el entorno, se proponen los siguientes elementos:

Uso de Patrones de Diseño (Design Patterns):
 Aplicar soluciones probadas como Strategy, Observer o Factory, que permiten cambiar el comportamiento del sistema o añadir nuevas funcionalidades sin modificar el código existente.
 
Arquitectura Basada en Microservicios o Componentes: 
Dividir el sistema en módulos independientes y débilmente acoplados. Esto permite actualizar, reemplazar o escalar una parte del software sin afectar al resto de la aplicación.

Inyección de Dependencias (Dependency Injection): 
Técnica que permite que los objetos no creen sus propias dependencias, sino que les sean proporcionadas. Esto facilita el intercambio de componentes (por ejemplo, cambiar una base de datos por otra) de forma sencilla.

Uso de Interfaces y Abstracciones: 
Programar hacia interfaces en lugar de implementaciones concretas. Esto asegura que el sistema dependa de "contratos" de comportamiento, permitiendo cambiar la lógica interna sin romper las conexiones entre módulos.

Refactorización Continua y Pruebas Automatizadas: 
Mantener el código limpio y contar con una suite de tests robusta da la seguridad necesaria para realizar cambios. Si el código es fácil de leer y está protegido por pruebas, el equipo puede adaptarlo rápidamente ante cualquier imprevisto.
