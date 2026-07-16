# Rendering Strategy

## Principle

The backend only delivers metadata.

The client is responsible for rendering.

## Rendering Flow

Screen

↓

Sections

↓

Components

↓

Renderer Registry

↓

Concrete UI

## Supported Renderers

### Flutter Renderer

Maps components to Flutter widgets.

### Web Components Renderer

Maps components to Web Components.

## Future Renderers

- Angular
- React
- Vue

through Web Components consumption.
