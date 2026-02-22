# ArCar MCP Server
Servidor oficial Model Context Protocol (MCP) para integraciones con **www.arcar.org**.

Este MCP permite que agentes de IA y clientes compatibles puedan buscar y obtener información de vehículos publicados en www.arcar.org en tiempo real.

---

## 🔎 Funcionalidad principal

### Búsqueda

Permite buscar vehículos publicados en arcar.org aplicando filtros como:

- Marca
- Modelo
- Año
- Rango de precio
- Ubicación

Devuelve resultados estructurados optimizados para consumo por asistentes de IA.

---

## 🌐 Endpoint remoto

Transporte SSE:

https://nave.q2bot.com/mcp/arcar-org

---

## 📦 Identificador en el MCP Registry

---

## 🧠 Casos de uso

Este servidor MCP permite:

- Asistentes automotrices con IA
- Agentes de búsqueda de vehículos
- Integraciones con marketplaces
- Herramientas de investigación automotriz
- Experiencias conversacionales de búsqueda

---

## 🏗 Arquitectura

- Base de datos: arcar.org
- Transporte: Server-Sent Events (SSE)
- Protocolo: Model Context Protocol (MCP)
- Versionado mediante MCP Registry

---

## 🔐 Seguridad

Actualmente el acceso es público.

En futuras versiones se podrá incorporar:

- Limitación de tasa (rate limiting)
- Autenticación
- Claves de acceso

---

## 📌 Versionado

Se utiliza versionado semántico:

- 1.0.0 → Publicación inicial
- 1.0.2 → Publicación inicial con mejoras

---

## 🌍 Sitio web

https://www.arcar.org

---

## 📄 Licencia

MIT License
