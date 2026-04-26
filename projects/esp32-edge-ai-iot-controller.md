# ESP32 – Edge AI IoT Sensor Controller

## Context
Personal firmware side project built to demonstrate modern embedded IoT development using **ESP32**, **ESP-IDF**, Wi-Fi networking, HTTP APIs, sensor data processing, and lightweight anomaly detection.

The project is designed as a practical embedded system rather than a simple demo. It focuses on modular firmware structure, testability, and clear separation between Wi-Fi connection management, HTTP request handling, sensor data ingestion, feature extraction, and inference/decision logic.

## My Role
Firmware Developer / System Designer.

## What I Built
- Built an ESP32 firmware project using **ESP-IDF** with a component-based architecture.
- Implemented Wi-Fi station connection flow and event-driven status handling.
- Added an HTTP server interface for sensor input, status reporting, and system-level testing.
- Designed a sensor processing pipeline for temperature / pressure style telemetry.
- Implemented lightweight anomaly detection logic suitable for resource-constrained embedded devices.
- Created Python integration tests to send normal and anomaly sensor samples to the ESP32 over HTTP.
- Used Git-based workflow to refactor, review, and evolve the project architecture step by step.

## Key Focus Areas
- ESP-IDF firmware architecture
- Wi-Fi station mode and event handling
- HTTP server endpoints for embedded control / telemetry
- Sensor pipeline design
- TinyML / Edge AI style anomaly detection
- Python-based integration testing
- Embedded software modularity and maintainability

## Architecture Overview
```text
Sensor Test Client / External Input
        |
        v
ESP32 HTTP Server
        |
        v
Sensor Input Parser
        |
        v
Feature Extraction / Window Buffer
        |
        v
Inference / Anomaly Decision
        |
        v
System Status / Alarm State
```

## Design Notes
This project intentionally uses a small embedded-friendly inference pipeline instead of relying on cloud processing. The goal is to explore how an ESP32 can make local decisions from sensor data while keeping the firmware readable, testable, and suitable for future extension.

The anomaly decision is based on a windowed sensor model, which avoids reacting too strongly to a single noisy sample and better reflects real embedded sensor behavior.

## Why This Project Matters
This side project connects my production embedded background with current IoT and edge AI development trends. It demonstrates hands-on experience with:

- Building a complete ESP32 firmware application from scratch
- Structuring firmware into reusable components
- Testing embedded behavior from a host-side Python script
- Thinking about reliability, sensor noise, alarm state design, and future maintainability

## Tech Stack
- **MCU / Platform:** ESP32
- **Framework:** ESP-IDF
- **Language:** Embedded C
- **Networking:** Wi-Fi, HTTP server
- **Testing:** Python integration tests, curl-based endpoint testing
- **Tools:** VS Code, ESP-IDF build system, Git

## Status
Active learning / portfolio project.  
Current focus: improving the sensor pipeline, anomaly detection behavior, documentation, and test coverage.
