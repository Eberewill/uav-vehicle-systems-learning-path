# Portfolio Project: UAV Mission Control and Safety Simulator

## Problem

Unmanned vehicles must continue operating safely when telemetry becomes delayed, communication is lost, commands fail, or vehicle state becomes uncertain.

## Proposed System

The portfolio project will combine PX4, Gazebo, ROS 2, MAVLink/MAVSDK, and a C++ mission supervisor to demonstrate reliable command, telemetry, mission execution, and fault recovery.

## Components

### Vehicle simulation

- PX4 software-in-the-loop flight controller
- Gazebo vehicle and world
- Simulated GNSS, IMU, and environmental effects

### Communication

- MAVLink vehicle connection
- Heartbeat and connection-health monitoring
- Command acknowledgement, timeout, and retry handling

### ROS 2 integration

- Telemetry publisher
- Vehicle-state manager
- Mission-command interface
- Health-monitoring node
- Mission safety supervisor

### Safety scenarios

- Lost communication link
- Stale telemetry
- Rejected or timed-out command
- GPS degradation
- Mission timeout
- Simulated sensor failure

## Target Demonstration

1. Launch the environment with one command.
2. Connect to the simulated vehicle.
3. Arm and take off.
4. Execute a waypoint mission.
5. Inject a communication or sensor fault.
6. Observe the safety supervisor select a recovery action.
7. Review structured logs and test results.

## Quality Requirements

- Clear separation between transport, state, mission, and safety logic
- Deterministic state transitions
- No silent command failures
- Automated tests for normal and degraded behaviour
- Reproducible setup on Ubuntu
- Honest documentation of limitations

## Portfolio Evidence

- Source code and tests
- Architecture diagram
- Mission and failure logs
- Short demo video
- Engineering decision records
- Retrospective explaining failures, tradeoffs, and improvements
