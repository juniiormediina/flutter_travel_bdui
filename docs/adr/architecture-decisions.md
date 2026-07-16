# Architecture Decision Records

## ADR-001 - Use Firebase instead of Spring Boot

### Status
Accepted

### Context
The objective of this project is to validate the Backend Driven UI approach with minimal infrastructure complexity.

### Decision
Firebase will be used as the backend platform for the proof of concept.

### Consequences
- Faster implementation.
- Free tier available.
- Less operational overhead.

---

## ADR-002 - Use Web Components for web rendering

### Status
Accepted

### Context
The project aims to support multiple frontend technologies.

### Decision
Web Components will be the standard web rendering approach.

### Consequences
- Compatible with Angular.
- Compatible with React.
- Compatible with Vanilla JavaScript.

---

## ADR-003 - Use Clean Architecture

### Status
Accepted

### Context
The BDUI engine must be isolated from infrastructure and presentation details.

### Decision
Apply Clean Architecture in Flutter modules.

### Consequences
- Better maintainability.
- Better testability.

---

## ADR-004 - Use a Monorepo

### Status
Accepted

### Context
The project will contain applications, shared contracts and rendering engines.

### Decision
Keep all artifacts in a single repository.

### Consequences
- Easier dependency management.
- Simpler collaboration.
