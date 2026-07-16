# Architecture Overview

## Purpose

Flutter Travel BDUI is a Proof of Concept focused on validating a Backend Driven UI approach for travel platforms.

The platform uses Firebase as backend and provides UI contracts in JSON format that are interpreted by different rendering engines.

## Goals

- Dynamic UI driven by backend configuration.
- Platform agnostic UI contract.
- Reusable rendering strategy.
- Multi-channel support.
- Low operational complexity.

## Main Components

### Firebase

Stores and delivers screen definitions.

### UI Contract

Defines screens, sections, components and actions.

### Flutter Renderer

Converts UI contracts into Flutter widgets.

### Web Components

Converts UI contracts into reusable web components.

## Architectural Principles

- Backend does not know frontend technologies.
- UI contracts are technology-agnostic.
- Rendering is delegated to clients.
- Components are composable.
- Clean Architecture is applied in consumers.
