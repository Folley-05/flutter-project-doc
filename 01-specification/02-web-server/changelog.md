# Changelog

All notable changes to this project will be documented in this file.

The format is based on and this project adheres.

---

## [1.0.0] – 2025-04-03

### Added
- Initial implementation of the HTTP server using `shelf`
- `GET /api/v1/hello` test endpoint
- `GET /api/v1/test` returns a welcome message
- `GET /api/v1/temperature` – accepts and echoes JSON body
- `POST /api/v1/houselist` – returns predefined house list
- `POST /api/v1/roomlist/<idHouse>` – stub response (to be implemented)

###  Architecture
- Modular architecture using `AbstractManager` and `GlobalManager`
- Logging system with request ID and structured messages
- Simulated in-memory data for `House` and `Room`
- Route versioning under `/api/v1/`

---

## [Unreleased]

###  Planned
- Full implementation of `/roomlist/<idHouse>` with:
  - 403 if electricity is off
  - 404 if house not found
- `PATCH /house/<id>/power` to toggle electricity state
- WebSocket server with event broadcasting (`/ws`)
- Token-based authentication

---

## [0.1.0] – 2025-03-29

###  Prototype
- Local test server with mock temperature route
- First test of request logging and routing

