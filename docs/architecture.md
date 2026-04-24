# ProjectTAU Architecture Draft

## Product shape
- Homepage / landing: assistant presence and quick navigation
- Landing page: public root domain entry point
- Dashboard: lives on a separate dashboard route
- Wiki: lives on a separate wiki route
- Project Builder: guided intake that asks questions until the plan is clear
- Web dashboard: stays simple and functional on the dashboard route
- Godot experience: separate advanced interactive/animated layer
- design notes: TAU-Wiki `ProjectTAU Godot Companion Architecture`
- Chat: persistent comms panel, usually docked

## Module boundaries
- layout and routing live in the web shell
- animation can live in a dedicated scene layer
- workspace definitions should be data-driven
- voice state should be shared across dashboard and Office views

## Open decisions
- web shell framework
- animation engine
- desktop wrapper, if any
- split between dashboard UI and scene layer
