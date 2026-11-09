# EcoRide

EcoRide es una propuesta de aplicación móvil de bicicletas compartidas que conecta a las personas con estaciones y bicicletas disponibles en su entorno. Desde la aplicación, un usuario puede consultar estaciones, comprobar la disponibilidad, solicitar una reserva y revisar sus trayectos anteriores. La solución se plantea con una app móvil desarrollada en Flutter, un servidor Java con Spring Boot y una base de datos PostgreSQL. Los componentes se comunican mediante una API REST que intercambia información en formato JSON. El proyecto busca facilitar desplazamientos urbanos de corta distancia y ofrecer una alternativa flexible para combinar con el transporte público. Esta documentación describe el funcionamiento previsto y una arquitectura de referencia; no implica que la aplicación o sus servicios estén desplegados.

## Objetivo

El objetivo de EcoRide es facilitar el acceso a la bicicleta compartida mediante información clara sobre estaciones y disponibilidad, y permitir la gestión de reservas y trayectos desde una aplicación móvil.

La movilidad compartida puede ayudar a:

- Reducir la dependencia del vehículo privado en desplazamientos urbanos cortos.
- Complementar el transporte público en el trayecto de primera o última milla.
- Aprovechar mejor una flota común de bicicletas.
- Favorecer hábitos de movilidad activa.

## Qué ofrece

- Registro e inicio de sesión de usuarios.
- Consulta de estaciones y bicicletas disponibles.
- Creación de reservas.
- Historial de trayectos.
- Estimación informativa del ahorro de CO₂.

Consulta el detalle en [Funcionalidades](funcionalitats.md) y la descripción de los servicios en [Arquitectura](arquitectura.md).
