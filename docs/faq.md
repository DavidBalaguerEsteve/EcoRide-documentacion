# Preguntas frecuentes

Respuestas rápidas sobre la aplicación EcoRide y el alcance descrito en esta documentación.

## ¿Qué necesito para utilizar EcoRide?

La propuesta contempla una aplicación móvil donde la persona usuaria se registra o inicia sesión para consultar estaciones, ver bicicletas disponibles y gestionar sus reservas. Los requisitos de una versión publicada dependerían de la implementación final.

## ¿Cómo puedo saber si hay bicicletas disponibles?

La aplicación consultaría la información de estaciones y bicicletas a través de la API de EcoRide. La disponibilidad mostrada dependería de los datos que el servidor tenga registrados en ese momento.

## ¿La reserva queda confirmada inmediatamente?

En el flujo previsto, el servidor comprueba que la bicicleta siga disponible y registra la reserva antes de devolver una confirmación. Los tiempos de reserva, la cancelación y el desbloqueo quedan pendientes de concretar en una implementación real.

## ¿El ahorro de CO₂ es una medición exacta?

No necesariamente. EcoRide contempla mostrar una estimación basada en comparar el trayecto con un medio de transporte de referencia. Para interpretarla correctamente, la aplicación debería explicar la fórmula y los supuestos utilizados.