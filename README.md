# ProjectTAU

ProjectTAU is the fresh scaffold for the next TAU interface: a public landing page, a dashboard route, a separate wiki route, and a separate advanced Godot experience for interactive/animated extra layers.

## Product goals
- focus on UI/UX first
- use dummy content initially
- feel futuristic and alive
- remain functional as a dashboard
- support rearrangeable workspaces and module presets
- keep chat available without making the app chat-first
- provide a guided project-builder flow that asks questions until the plan is clear
- allow future Hermes instances to be added later
- keep the public landing page separate from the dashboard and wiki surfaces

## Planned application structure

### `apps/web-shell`
The main application shell.

Responsible for:
- login and boot
- routing
- public landing page / root domain
- dashboard layout on a separate route
- top bar / navigation
- workspace switching
- docking chat
- project builder entry points and outbound links to dashboard/wiki routes

### `apps/office`
The separate Godot-powered experience / interactive layer.

Responsible for:
- Office visuals
- idle / listen / speak states
- ambient motion
- scene-like interactions
- possible future rendering-engine experiments

Design notes live in TAU-Wiki under `ProjectTAU Godot Companion Architecture`.

### `packages/ui`
Shared UI primitives.

Examples:
- buttons
- cards
- panels
- tabs
- drawers
- status pills

### `packages/scene`
Animation and scene helpers.

Examples:
- motion utilities
- audio-reactive helpers
- visual state transitions
- ambient scene logic

### `packages/voice`
Voice and audio-state helpers.

Examples:
- microphone input helpers
- speak/listen state handling
- audio playback state
- voice channel abstractions

### `packages/workspaces`
Workspace and layout definitions.

Examples:
- workspace presets
- module enable/disable state
- panel order and placement
- saved layout configurations

### `packages/agents`
Agent and conversation abstractions.

Examples:
- TAU instance logic
- ARCHIVAR instance logic later
- session identity
- message routing contracts
- channel adapters

### `packages/shared`
Shared utilities, types, and data models.

Examples:
- common types
- constants
- schema helpers
- shared state primitives

## Architecture principles
- prefer composition over inheritance
- keep the app shell separate from the Godot layer
- keep workspace state data-driven
- keep chat as a persistent panel, not the whole app
- keep classes for runtime/adapters/scene objects only when they truly help

## Repo layout
```text
ProjectTAU/
  apps/
    web-shell/
    office/
  packages/
    ui/
    scene/
    voice/
    workspaces/
    agents/
    shared/
  docs/
    architecture.md
    roadmap.md
  assets/
  tests/
```

## Current status
This repo is intentionally a clean scaffold. The next step is choosing the first implementation slice and wiring the app shell around it.
