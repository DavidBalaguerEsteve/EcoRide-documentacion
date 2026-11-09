# Funcionalidades

Las funciones de esta página describen el alcance previsto para EcoRide. Se indican como **previstas** porque el proyecto de referencia define una aplicación ficticia y no incluye una implementación que permita confirmar su disponibilidad.

## Registro y acceso

La persona usuaria podría crear una cuenta e iniciar sesión para asociar reservas y trayectos a su perfil. El servidor validaría las credenciales y devolvería la información necesaria para continuar la sesión. La autenticación concreta y su mecanismo de seguridad quedan pendientes de definir en una implementación real.

## Consulta de estaciones y bicicletas

La app permitiría consultar estaciones y el número de bicicletas disponibles en cada una. Esta información ayudaría a elegir un punto de recogida antes de iniciar un desplazamiento. La disponibilidad debería proceder de datos actualizados por el servicio.

## Reserva de bicicletas

Una persona con sesión iniciada podría solicitar una bicicleta disponible. El servidor comprobaría la disponibilidad y registraría la reserva para evitar asignar la misma bicicleta a más de una operación simultánea. Las reglas sobre caducidad, cancelación y desbloqueo deben concretarse durante el desarrollo.

## Historial y estimación de CO₂

El usuario podría revisar sus trayectos anteriores y consultar una estimación del CO₂ ahorrado frente a un desplazamiento de referencia en vehículo privado. La fórmula, los factores de emisión y el tratamiento de trayectos incompletos requerirían una definición explícita antes de usar la cifra como indicador real.

## Estado resumido

| Funcionalidad | Estado descrito | Usuario principal |
|---|---|---|
| Registro e inicio de sesión | Prevista | Usuario de EcoRide |
| Consulta de estaciones | Prevista | Usuario de EcoRide |
| Consulta de bicicletas disponibles | Prevista | Usuario de EcoRide |
| Reserva de bicicletas | Prevista | Usuario con sesión iniciada |
| Historial de trayectos | Prevista | Usuario con sesión iniciada |
| Estimación de ahorro de CO₂ | Prevista | Usuario de EcoRide |

El estado “prevista” refleja el alcance narrativo de la práctica, no el resultado de una prueba funcional.
