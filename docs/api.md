# API REST

Esta página presenta ejemplos **ficticios y coherentes** de una API de referencia para EcoRide. Las rutas no están conectadas a un servidor real y los datos de respuesta son ilustrativos.

## Rutas de referencia

| Método | Ruta | Finalidad |
|---|---|---|
| `GET` | `/api/stations` | Listar estaciones y disponibilidad |
| `GET` | `/api/bikes` | Consultar bicicletas; admite filtros por estación |
| `POST` | `/api/reservations` | Solicitar una reserva |
| `GET` | `/api/users/{id}` | Consultar el perfil de un usuario |

## Listar estaciones

**Petición:** `GET /api/stations`

**Respuesta de ejemplo:**

```json
[
  {
    "id": 12,
    "name": "Estación Centro",
    "address": "Plaza Mayor, 1",
    "availableBikes": 6,
    "latitude": 40.4168,
    "longitude": -3.7038
  }
]
```

## Consultar bicicletas

**Petición:** `GET /api/bikes?stationId=12`

**Respuesta de ejemplo:**

```json
[
  {
    "id": 204,
    "stationId": 12,
    "type": "standard",
    "available": true
  }
]
```

## Crear una reserva

**Petición:** `POST /api/reservations`

**Cuerpo de la petición:**

```json
{
  "userId": 58,
  "bikeId": 204
}
```

**Respuesta de ejemplo:**

```json
{
  "id": 901,
  "userId": 58,
  "bikeId": 204,
  "status": "confirmed",
  "createdAt": "2026-11-09T10:30:00Z"
}
```

En una implementación real, el servidor tendría que confirmar que el usuario puede reservar y que la bicicleta continúa disponible. Los códigos HTTP y el formato de errores se deberían acordar como parte del contrato de API.

## Consultar un usuario

**Petición:** `GET /api/users/58`

**Respuesta de ejemplo:**

```json
{
  "id": 58,
  "name": "Alex",
  "email": "alex@example.test"
}
```

El dominio `.test` se usa en el ejemplo para no señalar una dirección de correo real.

## Alcance de los ejemplos

Los nombres de campos, identificadores, valores y rutas se proponen únicamente para explicar el contrato. Deben validarse y ajustarse cuando exista una implementación del backend.
