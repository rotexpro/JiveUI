# JiveUI

**JiveUI** is a modern desktop UI framework for the JVM designed to simplify how developers build structured, maintainable Java desktop applications.

Java has long been trusted to power critical systems across finance, government, and enterprise infrastructure. Yet building desktop user interfaces in Java has remained unnecessarily complex and fragmented. Frameworks like JavaFX provide a powerful rendering engine, but the developer experience often feels dated—relying on XML layouts, tightly coupled controllers, and manual scene management.

JiveUI aims to rethink that experience.

The project introduces a **code-first, modular UI architecture** built on JavaFX that provides a clearer, more scalable way to build desktop interfaces.

Instead of manipulating scenes, stages, and nodes directly, developers describe their applications in terms of **views, layouts, components, and events**. JiveUI then orchestrates the rendering and lifecycle management behind the scenes.

---

## Vision

JiveUI is built around a simple goal:

> Make building JVM desktop applications structured, predictable, and enjoyable again.

The framework focuses on:

* Code-first UI development
* Clear application structure
* Reusable layout systems
* Strong separation of concerns
* Enterprise-friendly architecture

It aims to bring the developer ergonomics of modern UI frameworks to the Java ecosystem while preserving the JVM's reliability and strength.

---

## Core Concepts

JiveUI introduces a layered UI architecture designed to organize applications in a modular way.

### Views

Views represent **pages or screens** in an application.

A view is typically associated with a route and defines the primary content of a page. Views can be composed with one or more layouts to create consistent UI structures across the application.

---

### Layouts

Layouts are **reusable UI shells** that wrap views.

Layouts make it easy to share UI structures such as navigation bars, side panels, dashboards, or authentication containers across multiple pages.

Layouts can be layered to form hierarchical UI structures similar to modern web frameworks.

Example structure:

App Layout
→ Dashboard Layout
→ Dashboard Page

This enables powerful composition patterns while keeping pages focused on their content.

---

### Components

Components represent **reusable UI building blocks** such as navigation bars, tables, forms, and panels.

Components can be used within views or layouts to promote modular UI development.

---

### Routing

JiveUI includes a router responsible for:

* Route registration
* View resolution
* Navigation between pages
* Passing route parameters

This removes the need to manually manage JavaFX scenes when navigating between pages.

---

### Rendering Engine

JiveUI maintains an internal UI representation that is translated into JavaFX nodes by the renderer.

This allows the framework to manage layout composition and UI structure while delegating actual rendering to JavaFX's mature scene graph system.

---

### Event System

JiveUI introduces an abstraction layer over JavaFX events, allowing developers to work with consistent UI event handling while isolating framework logic from JavaFX-specific behavior.

---

## Architecture

The framework is currently organized around four core modules:

### `jive-core`

The heart of the framework.

Responsibilities include:

* application lifecycle
* view and layout registration
* annotation processing
* framework configuration
* application context

---

### `jive-renderer`

Responsible for translating the JiveUI UI structure into JavaFX scene graph nodes.

---

### `jive-router`

Handles navigation and routing between views.

Responsibilities include:

* route registration
* view switching
* layout resolution
* route parameters

---

### `jive-events`

Provides the event abstraction layer used for UI interactions.

---

## Project Goals

JiveUI is currently an experimental open-source project exploring a modern architecture for JVM desktop development.

The long-term goals include:

* A clean code-first UI framework for Java
* A composable layout system for desktop applications
* Modular UI architecture suited for enterprise projects
* Reactive state support
* Simplified desktop packaging
* Tooling for large-scale application development

Ultimately, JiveUI aims to provide a framework where developers think in terms of **views, layouts, and components**, rather than scenes, nodes, and controllers.

---

## Status

JiveUI is currently in early development and architectural exploration. The initial focus is on defining the core runtime, routing system, and layout architecture.

Contributions, ideas, and feedback are welcome as the project evolves.

---

## Why JiveUI?

Java remains one of the most reliable platforms for building large systems. JiveUI explores how the same reliability and structure can be brought to desktop UI development with a cleaner, modern developer experience.

The goal is simple:

Build desktop applications on the JVM **without fighting the framework**.

---

## License

This project is open source and licensed under the Apache License 2.0.
