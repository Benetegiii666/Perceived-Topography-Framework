# AHA_007: Map, Sensor, Navigator

**Date:** 2026-06-09 (from seed material)

## The Moment

The framework's components map to a navigation analogy:
- **Topography** = the map (the actual terrain)
- **Information Surfaces** = the sensors (what the navigator can detect)
- **Perception** = the navigator's mental model (constructed from sensor data)
- **Optimization** = the navigator's route selection (based on the mental model)

## Why It Matters

This analogy makes the framework concrete and testable. A navigator with bad sensors will build a wrong mental model and choose a poor route — even if the map is favorable. This is exactly the information surface corruption pattern (DISCOVERY_002).

It also highlights that you can intervene at any of the four levels: change the terrain, change the sensors, change the model-building process, or change the route-selection algorithm.

## Cross-References
- EC_004 (Information Surfaces = sensors)
- DISCOVERY_002 (KPI gaming = sensor corruption)
- FL_007 (Interface Layer — sensors as "neither agent nor environment")
