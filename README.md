# Flutter Travel BDUI

Backend Driven UI (BDUI) proof of concept for a travel platform using Flutter, Firebase and Clean Architecture.

The goal of this project is to validate a technology-agnostic UI contract capable of rendering dynamic screens across multiple clients such as Flutter, Web Components, Angular and React.

---

## Vision

Traditional applications require frontend deployments whenever the user interface changes.

This project explores a Backend Driven UI approach where screen composition is defined through JSON contracts delivered by the backend.

```text
Firebase
    ↓
UI Contract
    ↓
Renderer Engine
    ↓
User Interface
```

The backend is responsible for describing *what* should be rendered.

The client is responsible for deciding *how* it should be rendered.

---

## Objectives

- Validate Backend Driven UI patterns.
- Build dynamic travel experiences using JSON contracts.
- Keep frontend applications technology agnostic.
- Reuse contracts across Flutter and Web platforms.
- Apply Clean Architecture principles.
- Enable future experimentation through A/B testing and personalization.

---

## Architecture Overview

```text
                       Firebase
                           │
                           ▼
                    UI Contract JSON
                           │
         ┌─────────────────┴─────────────────┐
         │                                   │
         ▼                                   ▼

 Flutter Renderer              Web Components Renderer

         ▼                                   ▼

    Flutter App            Angular / React / Vanilla JS
```

---

## Repository Structure

```text
flutter_travel_bdui
│
├── apps
│   ├── flutter_app
│   └── web_preview
│
├── packages
│   ├── ui_contract
│   ├── flutter_renderer
│   └── web_components
│
├── firebase
│   ├── screens
│   ├── models
│   └── rules
│
├── docs
│   ├── architecture
│   ├── diagrams
│   └── adr
│
├── README.md
├── firebase.json
└── .gitignore
```

---

## Main Components

### UI Contract

Defines the structure of screens through a technology-independent JSON format.

Examples:

- Screen
- Section
- Component
- Layout
- Action

---

### Flutter Renderer

Responsible for transforming UI contracts into Flutter widgets.

```text
JSON
 ↓
Parser
 ↓
Registry
 ↓
Flutter Widgets
```

---

### Web Components

Reusable rendering layer for web applications.

Supported consumers:

- Angular
- React
- Vanilla JavaScript

---

### Firebase

Acts as the backend for the proof of concept.

Responsibilities:

- Store screen definitions
- Deliver UI contracts
- Support future experimentation

---

## Example Contract

```json
{
  "screenId": "home",
  "version": "1.0",
  "sections": [
    {
      "id": "hero",
      "components": [
        {
          "type": "banner",
          "props": {
            "title": "Discover Europe",
            "subtitle": "Summer Deals"
          }
        }
      ]
    }
  ]
}
```

---

## Initial Scope

The first iteration focuses on the following travel components:

- Banner
- Title
- Button
- Offer Card
- Flight Search
- Destination Carousel

---

## Architectural Principles

- Backend must remain frontend agnostic.
- UI contracts are the source of truth.
- Rendering happens on the client side.
- Components are reusable and composable.
- Shared contracts must work across platforms.
- Clean Architecture is applied to consumers.

---

## Documentation

Architecture documentation is available under:

```text
docs/architecture
```

System diagrams:

```text
docs/diagrams
```

Architecture decisions:

```text
docs/adr
```

---

## Project Status

🚧 Proof of Concept (PoC)

Current focus:

- Define UI Contract
- Build Flutter Renderer
- Deliver screens through Firebase
- Validate contract portability across platforms

---

## License

MIT
