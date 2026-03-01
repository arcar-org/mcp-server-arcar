# 🚗 ArCar MCP Server

Servidor MCP oficial para integraciones con arcar.org.

Permite realizar búsquedas y consultas de vehículos clásicos y especiales publicados en la plataforma mediante herramientas compatibles con Model Context Protocol (MCP).

---

## 📦 Identificador en el MCP Registry

io.github.arcar-org/arcar-mcp

---

## 🌐 Endpoint remoto

Transporte: Server-Sent Events (SSE)

https://nave.q2bot.com/mcp/arcar-org

---

## 🛠 Herramientas disponibles

### Buscar Vehiculos

Búsqueda general de vehículos por término libre. Busca en marca, modelo, título y características. Devuelve hasta 20 resultados.

| Parámetro | Tipo | Descripción |
|-----------|------|-------------|
| `searchTerm` | string | Término de búsqueda (marca, modelo o características) |

### Obtener Vehiculo por ID

Obtiene los detalles completos de un vehículo específico por su ID numérico.

| Parámetro | Tipo | Descripción |
|-----------|------|-------------|
| `vehicleId` | number | ID numérico del vehículo |

### Vehiculos Destacados

Lista los vehículos destacados/premium actualmente en el catálogo. No requiere parámetros.

### Vehiculos Recientes

Obtiene los vehículos más recientemente publicados, ordenados por fecha de alta.

| Parámetro | Tipo | Descripción |
|-----------|------|-------------|
| `cantidad` | number | Cantidad de resultados a devolver (1-20) |

### Vehiculos por Marca

Filtra vehículos de una marca específica.

| Parámetro | Tipo | Descripción |
|-----------|------|-------------|
| `marca` | string | Nombre de la marca (ej: Ford, Chevrolet, Peugeot, BMW) |

### Vehiculos por Rango de Precio

Filtra vehículos por rango de precio y moneda. Devuelve resultados ordenados por precio ascendente.

| Parámetro | Tipo | Descripción |
|-----------|------|-------------|
| `moneda` | string | Moneda: `USD` o `$` (pesos argentinos) |
| `precioMinimo` | number | Precio mínimo del rango |
| `precioMaximo` | number | Precio máximo del rango |

---

## Esquema de respuesta

Todas las herramientas de búsqueda devuelven vehículos con la siguiente estructura:

| Campo | Tipo | Descripción |
|-------|------|-------------|
| `Id` | number | ID único del vehículo |
| `Marca` | string | Marca del vehículo |
| `Modelo` | string | Modelo |
| `MarcaModelo` | string | Título completo |
| `VehiculoTipo` | string | `A` = Auto, `M` = Moto, `N` = Otro |
| `Moneda` | string | `USD` o `$` |
| `Valor` | string | Precio |
| `Caracteristicas` | string | Descripción del vendedor |
| `Pais` | string | País de ubicación |
| `Provincia` | string | Provincia/estado |
| `Foto` | string | URL de la foto principal |
| `Fotos` | number | Cantidad de fotos disponibles |
| `Url` | string | Link a la publicación en arcar.org |
| `Destacado` | string | `0` = normal, otro = premium |
| `Visitas` | number | Contador de visitas |
| `FechaAlta` | datetime | Fecha de publicación |

---

## 🏗 Arquitectura

- Base de datos: arcar.org
- Protocolo: Model Context Protocol (MCP)
- Transporte: SSE
- Versionado: SemVer
- Acceso: Público (sin autenticación)

---

## 📌 Versionado

Versión actual: 1.0.4

- 1.0.0 → Primera publicación en el MCP Registry
- 1.0.1 → Ajustes de configuración
- 1.0.2 → Mejoras internas
- 1.0.3 → Ajustes menores
- 1.0.4 → Nuevas Tools disponibles

---

## 🌍 Sitio web

https://www.arcar.org

---

## 📄 Licencia

MIT License
