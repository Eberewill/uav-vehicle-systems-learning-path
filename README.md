# UAV Vehicle Systems Learning Path

A practical 16-week transition plan from full-stack/backend engineering into UAV vehicle systems, autonomy, robotics integration, and simulation.

This repository tracks my preparation for software engineering roles involving unmanned vehicles, with emphasis on:

- Modern C++ and systems programming
- Linux, concurrency, networking, and fault handling
- ROS 2 robotics middleware
- PX4, MAVLink, and MAVSDK
- Gazebo simulation and software-in-the-loop testing
- Mission execution, telemetry, failsafes, and field-ready reliability

## Goal

Build a portfolio-grade UAV mission simulation and control system that can:

1. Launch a simulated PX4 vehicle in Gazebo.
2. Receive and display live telemetry.
3. Arm, take off, execute waypoints, and return home.
4. Detect link loss and unhealthy vehicle state.
5. Trigger safe hold, return-to-home, or landing behaviour.
6. Reproduce missions and failures through automated tests.

## Timeline

| Phase | Weeks | Focus | Deliverable |
|---|---:|---|---|
| 1 | 1–3 | Modern C++ and systems fundamentals | C++ telemetry service |
| 2 | 4–6 | ROS 2 and robotics foundations | Vehicle-state and mission nodes |
| 3 | 7–9 | PX4, MAVLink, and MAVSDK | Automated simulated mission |
| 4 | 10–12 | Gazebo and SIL validation | Fault-injection test environment |
| 5 | 13–14 | Autonomy and reliability | Mission safety supervisor |
| 6 | 15–16 | Hardware bridge and portfolio | Documented public demonstration |

The full curriculum is in [ROADMAP.md](ROADMAP.md). Progress is tracked in [CHECKLIST.md](CHECKLIST.md), and the project definition is in [PROJECT.md](PROJECT.md).

## Weekly Commitment

- 5 hours: C++ and robotics concepts
- 6 hours: building and testing
- 2 hours: PX4/ROS documentation and log analysis
- 1–2 hours: documentation and engineering notes

## Current Background

I am building on production experience with Python, Go, Node.js, Linux, Docker, real-time communication, event-driven services, CI/CD, observability, and hardware-connected applications.

## Principles

- Build something testable every week.
- Prefer reproducible simulation over presentation-only demos.
- Treat dropped messages, stale state, timeouts, and recovery as normal conditions.
- Document failures and engineering decisions, not only successful outcomes.
- Never claim a skill without a working example that demonstrates it.

## Status

Current phase: **Phase 1 — Modern C++ and systems fundamentals**
