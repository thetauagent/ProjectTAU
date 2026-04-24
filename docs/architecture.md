# ProjectTAU Architecture Draft

## Product shape
- Homepage / landing: assistant presence and quick navigation
- Dashboard: tasks, agents, live status, and modules
- Project Builder: guided intake that asks questions until the plan is clear
- Office: animated visual home base
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
