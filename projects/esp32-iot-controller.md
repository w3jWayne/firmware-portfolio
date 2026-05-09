# ESP32 – Event-Driven IoT Sensor Controller

## Context

Personal firmware side project built to explore production-style embedded IoT development using **ESP32** and **ESP-IDF**.

The project focuses on modular firmware architecture, event-driven communication, Wi-Fi networking, sensor data processing pipelines, and embedded integration/testing concepts commonly used in connected IoT systems.

---

## Source Code

👉 GitHub:
https://github.com/w3jWayne/esp32-iot-sensor-controller

For more details about the project structure, build steps, architecture notes, and testing workflow, please see the README in the repository.

---

## What I Built

* Built an ESP32 firmware application using **ESP-IDF** with a modular component-based architecture.
* Implemented event-driven firmware flow using **FreeRTOS queues** and centralized event dispatching.
* Designed Wi-Fi connection management and asynchronous system event handling.
* Developed HTTP server endpoints for sensor ingestion, status reporting, and integration testing.
* Built a lightweight sensor processing pipeline with sliding window buffering and data evaluation logic.
* Integrated MQTT-based telemetry publishing for IoT-style communication workflows.
* Created Python-based integration tools for automated sensor simulation and end-to-end testing.
* Structured the project for scalability and maintainability using reusable firmware modules.

---

## Key Focus Areas

* ESP-IDF firmware architecture
* FreeRTOS queue-based task communication
* Event-driven firmware design
* Wi-Fi and HTTP communication
* MQTT telemetry integration
* Sensor data pipeline design
* Embedded integration testing
* Firmware modularity and maintainability

---

## Architecture Overview

```text
External Sensor Input / Test Client
                |
                v
        HTTP / MQTT Interface
                |
                v
        Central Event Queue
                |
                v
        Event Dispatcher Task
                |
     -------------------------
     |           |           |
     v           v           v
 Sensor      Pipeline     System
 Module       Module      Control
     |           |
     v           v
 Data Processing / Evaluation
     |
     v
 System Status / Alarm State
```

---

## Design Notes

The project emphasizes embedded-friendly system design principles including asynchronous event handling, queue-based communication, modular firmware organization, and separation between communication, processing, and control layers.

The sensor evaluation flow uses a sliding-window approach to avoid reacting too strongly to isolated noisy samples and to better simulate real embedded sensing behavior.

The architecture is intentionally designed to support future extension for additional communication interfaces, event sources, and processing modules.

---

## Why This Project Matters

This project demonstrates practical embedded firmware development concepts commonly used in connected IoT systems, including:

* Event-driven firmware architecture
* FreeRTOS-based task communication
* Embedded networking with Wi-Fi, HTTP, and MQTT
* Sensor data processing pipelines
* Integration testing using host-side Python tools
* Modular firmware organization for long-term maintainability

---

## Tech Stack

* **MCU / Platform:** ESP32
* **Framework:** ESP-IDF
* **RTOS:** FreeRTOS
* **Language:** Embedded C
* **Communication:** Wi-Fi, HTTP, MQTT
* **Testing:** Python integration tests, curl-based endpoint testing
* **Tools:** VS Code, ESP-IDF build system, Git

---

## Status

Active learning / portfolio project.

Current focus:

* expanding the event-driven architecture
* improving firmware modularity and scalability
* strengthening MQTT communication flows
* improving integration and reliability testing
