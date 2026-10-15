# 16-Week Roadmap

## Phase 1: Modern C++ and Systems Fundamentals — Weeks 1–3

### Learn

- C++17/20 syntax, types, references, pointers, and object lifetime
- RAII, smart pointers, classes, templates, STL containers, and algorithms
- CMake, unit testing, GDB, sanitizers, and profiling
- Threads, mutexes, asynchronous work, and safe shared state
- Linux processes, TCP/UDP sockets, serial communication, and structured logs

### Build

A C++ telemetry service that receives simulated vehicle messages, validates them, maintains vehicle state, rejects stale data, and records faults.

### Exit criteria

- Builds reproducibly with CMake
- Includes unit tests and malformed-message tests
- Runs cleanly with address and undefined-behaviour sanitizers
- Documents message format, state transitions, and failure handling

## Phase 2: Robotics Foundations and ROS 2 — Weeks 4–6

### Learn

- Coordinate frames, vectors, quaternions, and transformations
- ROS 2 nodes, topics, services, actions, parameters, and launch files
- C++ and Python publishers/subscribers
- TF2, standard sensor messages, rosbag recording, and playback
- Quality of Service policies and behaviour under dropped or delayed messages

### Build

ROS 2 nodes for vehicle state, telemetry ingestion, mission commands, health monitoring, and emergency-stop behaviour.

### Exit criteria

- Nodes launch together from one command
- Recorded telemetry can be replayed deterministically
- Tests cover stale telemetry and node restart behaviour
- Architecture and topic contracts are documented

## Phase 3: UAV Stack, PX4, and MAVLink — Weeks 7–9

### Learn

- Flight controllers, companion computers, IMUs, GNSS, ESCs, and payloads
- PX4 architecture, flight modes, arming, waypoints, geofencing, and failsafes
- MAVLink heartbeats, telemetry messages, commands, and acknowledgements
- MAVSDK or MAVROS integration

### Build

Command a simulated PX4 aircraft to connect, arm, take off, follow waypoints, return home, and respond to a lost-link event.

### Exit criteria

- Mission completes without manual intervention
- Every command has acknowledgement and timeout handling
- Link-loss behaviour is repeatable
- Flight logs can be inspected and explained

## Phase 4: Gazebo and Software-in-the-Loop Testing — Weeks 10–12

### Learn

- Gazebo worlds, models, sensors, and plugins
- PX4 software-in-the-loop workflows
- Wind, GPS noise, delayed telemetry, link loss, and sensor faults
- Automated mission tests and telemetry/log analysis
- Reproducible containerized development environments

### Build

A PX4 and Gazebo demonstration with automated mission execution and selectable fault-injection scenarios.

### Exit criteria

- Fresh setup is documented and reproducible
- Normal and failure scenarios run from scripts
- Test output identifies the exact failed safety condition
- Results are summarized in an engineering report

## Phase 5: Autonomy and Reliability — Weeks 13–14

### Learn

- Finite-state machines and introductory behaviour trees
- Basic path planning and obstacle avoidance
- State estimation and introductory Kalman filtering
- Watchdogs, retries, timeouts, degraded modes, and safe recovery

### Build

A mission safety supervisor that selects hold, return-to-home, or emergency landing based on vehicle health and communication state.

### Exit criteria

- Safety decisions are deterministic and auditable
- Unit tests cover normal and degraded states
- Recovery behaviour is demonstrated under at least three injected faults

## Phase 6: Hardware Bridge and Portfolio — Weeks 15–16

### Learn

- UART, serial, and CAN fundamentals
- Raspberry Pi or NVIDIA Jetson companion-computer deployment
- Hardware-in-the-loop concepts and resource constraints
- Profiling, operational logs, CI, and field-test procedures

### Deliver

- Public GitHub repository with setup instructions
- Architecture diagram and engineering decision records
- Automated tests and a one-command development setup
- A two-to-three-minute demonstration video
- A technical article explaining one failure scenario and recovery design
- Interview notes covering tradeoffs, failures, and next steps

## Priority Order

1. C++
2. Linux debugging and concurrency
3. ROS 2
4. PX4 and MAVLink
5. Gazebo and SIL testing
6. TCP/UDP, serial, and CAN
7. State estimation and motion planning

Advanced computer vision, CUDA, LiDAR, and SLAM are intentionally deferred. The initial objective is vehicle systems and autonomy, not perception specialization.
