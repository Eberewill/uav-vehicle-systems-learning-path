# UAV Vehicle Systems Learning Path

A practical 16-week transition plan from full-stack/backend engineering into UAV vehicle systems, autonomy, robotics integration, and simulation.

This repository tracks my preparation for software engineering roles involving unmanned vehicles, with emphasis on:

- Modern C++ and systems programming
- Linux, concurrency, networking, and fault handling
- ROS 2 robotics middleware
- PX4, MAVLink, and MAVSDK
- Gazebo simulation and software-in-the-loop testing
- Mission execution, telemetry, failsafes, and field-ready reliability

## Quick Navigation

- [Goal](#goal)
- [16-week timeline](#16-week-timeline)
- [Start here: Phase 1](#start-here-phase-1)
- [Official learning resources](#official-learning-resources)
- [Weekly commitment](#weekly-commitment)
- [Current background](#current-background)
- [Learning principles](#learning-principles)
- [Current status](#current-status)
- [Full roadmap](ROADMAP.md)
- [Weekly checklist](CHECKLIST.md)
- [Portfolio project specification](PROJECT.md)

## Goal

Build a portfolio-grade UAV mission simulation and control system that can:

1. Launch a simulated PX4 vehicle in Gazebo.
2. Receive and display live telemetry.
3. Arm, take off, execute waypoints, and return home.
4. Detect link loss and unhealthy vehicle state.
5. Trigger safe hold, return-to-home, or landing behaviour.
6. Reproduce missions and failures through automated tests.

## 16-Week Timeline

| Phase | Weeks | Focus | Deliverable |
|---|---:|---|---|
| [1](ROADMAP.md#phase-1-modern-c-and-systems-fundamentals--weeks-13) | 1–3 | Modern C++ and systems fundamentals | [C++ telemetry service](CHECKLIST.md#weeks-13-c-and-systems) |
| [2](ROADMAP.md#phase-2-robotics-foundations-and-ros-2--weeks-46) | 4–6 | ROS 2 and robotics foundations | [Vehicle-state and mission nodes](CHECKLIST.md#weeks-46-ros-2) |
| [3](ROADMAP.md#phase-3-uav-stack-px4-and-mavlink--weeks-79) | 7–9 | PX4, MAVLink, and MAVSDK | [Automated simulated mission](CHECKLIST.md#weeks-79-px4-and-mavlink) |
| [4](ROADMAP.md#phase-4-gazebo-and-software-in-the-loop-testing--weeks-1012) | 10–12 | Gazebo and SIL validation | [Fault-injection test environment](CHECKLIST.md#weeks-1012-gazebo-and-sil-tests) |
| [5](ROADMAP.md#phase-5-autonomy-and-reliability--weeks-1314) | 13–14 | Autonomy and reliability | [Mission safety supervisor](CHECKLIST.md#weeks-1314-autonomy-and-reliability) |
| [6](ROADMAP.md#phase-6-hardware-bridge-and-portfolio--weeks-1516) | 15–16 | Hardware bridge and portfolio | [Documented public demonstration](CHECKLIST.md#weeks-1516-hardware-and-portfolio) |

The full curriculum is in [ROADMAP.md](ROADMAP.md). Progress is tracked in [CHECKLIST.md](CHECKLIST.md), and the project definition is in [PROJECT.md](PROJECT.md).

## Start Here: Phase 1

Use this order for the first three weeks:

1. Follow [LearnCpp](https://www.learncpp.com/) through the language fundamentals, functions, classes, object lifetime, references, pointers, and smart pointers.
2. Use [cppreference](https://en.cppreference.com/w/) as the language and standard-library reference.
3. Complete the official [CMake tutorial](https://cmake.org/cmake/help/latest/guide/tutorial/index.html).
4. Learn unit testing through the [GoogleTest primer](https://google.github.io/googletest/primer.html).
5. Practise debugging with the [GDB manual](https://sourceware.org/gdb/current/onlinedocs/gdb.html).
6. Work through the [Phase 1 roadmap](ROADMAP.md#phase-1-modern-c-and-systems-fundamentals--weeks-13).
7. Mark completed tasks in the [Phase 1 checklist](CHECKLIST.md#weeks-13-c-and-systems).

The first engineering deliverable is the telemetry service defined in [PROJECT.md](PROJECT.md#communication).

## Official Learning Resources

### C++ and systems

- [LearnCpp](https://www.learncpp.com/) — structured modern C++ lessons
- [cppreference](https://en.cppreference.com/w/) — C++ language and standard-library reference
- [CMake tutorial](https://cmake.org/cmake/help/latest/guide/tutorial/index.html) — official build-system guide
- [GoogleTest primer](https://google.github.io/googletest/primer.html) — unit-testing fundamentals
- [GDB documentation](https://sourceware.org/gdb/current/onlinedocs/gdb.html) — native debugging
- [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/) — practical socket programming

### ROS 2 and robotics

- [ROS 2 Jazzy tutorials](https://docs.ros.org/en/jazzy/Tutorials.html) — nodes, topics, services, actions, parameters, and launch files
- [ROS 2 C++ client library](https://docs.ros.org/en/jazzy/Concepts/Basic/About-Client-Libraries.html) — `rclcpp` concepts
- [ROS 2 QoS concepts](https://docs.ros.org/en/jazzy/Concepts/Intermediate/About-Quality-of-Service-Settings.html) — reliability and message delivery
- [TF2 tutorials](https://docs.ros.org/en/jazzy/Tutorials/Intermediate/Tf2/Tf2-Main.html) — coordinate frames and transformations
- [rosbag2 tutorial](https://docs.ros.org/en/jazzy/Tutorials/Advanced/Recording-A-Bag-From-Your-Own-Node-CPP.html) — recording and replaying system data

### PX4, MAVLink, and simulation

- [PX4 documentation](https://docs.px4.io/main/en/) — autopilot concepts and development
- [PX4 simulation guide](https://docs.px4.io/main/en/simulation/) — software-in-the-loop and simulators
- [PX4 ROS 2 integration](https://docs.px4.io/main/en/ros2/) — ROS 2 interface and examples
- [MAVLink guide](https://mavlink.io/en/) — protocol, messages, routing, and command handling
- [MAVSDK guide](https://mavsdk.mavlink.io/main/en/) — programmatic vehicle control and telemetry
- [Gazebo Harmonic documentation](https://gazebosim.org/docs/harmonic/getstarted/) — simulator setup, worlds, models, and plugins

### Hardware integration and reliability

- [Linux serial programming](https://www.kernel.org/doc/html/latest/driver-api/serial/index.html) — kernel serial documentation
- [Linux SocketCAN](https://docs.kernel.org/networking/can.html) — CAN networking and interfaces
- [PX4 failsafe configuration](https://docs.px4.io/main/en/config/safety.html) — vehicle safety and recovery behaviour
- [PX4 flight-log analysis](https://docs.px4.io/main/en/log/flight_log_analysis.html) — reviewing and diagnosing simulated flights

## Weekly Commitment

- 5 hours: C++ and robotics concepts
- 6 hours: building and testing
- 2 hours: PX4/ROS documentation and log analysis
- 1–2 hours: documentation and engineering notes

## Current Background

I am building on production experience with Python, Go, Node.js, Linux, Docker, real-time communication, event-driven services, CI/CD, observability, and hardware-connected applications.

## Learning Principles

- Build something testable every week.
- Prefer reproducible simulation over presentation-only demos.
- Treat dropped messages, stale state, timeouts, and recovery as normal conditions.
- Document failures and engineering decisions, not only successful outcomes.
- Never claim a skill without a working example that demonstrates it.

## Current Status

Current phase: **Phase 1 — Modern C++ and systems fundamentals**
