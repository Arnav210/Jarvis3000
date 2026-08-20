---
layout: page
title: Team
permalink: /team-portfolio/
---

# Research Overview & Systems Integration Plan

## 1. System Architecture & Problem Alignment

### Overarching Team Problem Statement
> "Property owners and security personnel struggle to maintain spatial situational awareness and detect true physical security anomalies because conventional smart security cameras rely on continuous video streaming and basic motion detection. Consequently, current visual surveillance solutions suffer from high rates of false alarms caused by non-threatening environmental changes, generate excessive cloud storage overhead, and create severe privacy vulnerabilities by transmitting and storing raw video footage."

---

### Sub-System Integration Matrix
**Overall System Goal:** Build a smart visual monitoring system that tracks spatial changes in real time while reducing false positives, data footprint, and privacy risks.

| Sub-System Lead | Sub-System Focus | Direct Role in Solution |
| :--- | :--- | :--- |
| **Member 1** | Computer Vision & Object Recognition | Solves the bounding box and detection pipeline so the system identifies what items are present in a frame. |
| **Member 2** | Material & Object Understanding | Filters out false alarms caused by surface reflections, material glares, or ambient lighting changes. |
| **Member 3** | Spatial Awareness & Distance Estimation | Calculates exact 3D distances and spatial coordinates relative to the camera lens. |
| **Member 4** | AI Visual Memory & Scene Comparison | Ingests data from all three sub-systems into lightweight visual embeddings to track added, missing, or moved objects without storing raw video. |

---

### Target System Performance Metrics

* **Storage Overhead Reduction:** Achieve **>90% reduction** in data overhead by storing scene vector embeddings/descriptors (< 100 KB per snapshot) instead of raw continuous video frames.
* **Alert Accuracy:** Reduce false-alarm rates by **>70%** relative to standard PIR/pixel-motion security sensors during ambient lighting shifts.
* **System Latency:** Complete local scene change detection in **< 1.5 seconds** per capture on edge hardware.
* **Data Privacy:** Maintain **zero transmission** or persistent storage of identifiable raw RGB video clips during routine monitoring operations.

---

## 2. Research Protocol & Development Roadmap

### Phase 1: Interface Control Document (ICD) Specification
Prior to module implementation, establish a standardized 1-page ICD detailing:
* **Data Transport Strategy:** Standardize pipeline communication via JSON payloads, ROS messages, or REST API endpoints.
* **Schema & Type Definitions:** Define variable conventions (e.g., `confidence_score` as a float `[0.0, 1.0]`, `bbox` as `[x_min, y_min, x_max, y_max]`).
* **Coordinate Frame Standardization:** Set origin `(0,0,0)` at the camera lens center with distances measured in meters (m).

### Phase 2: Mock Generation (Stub Development)
Implement modular mock scripts outputting synthetic data aligned with the ICD schema:
* **Input Stubs:** Generate mock bounding box JSON payloads to advance the Visual Memory module independently of upstream vision model completion.
* **Output Stubs:** Provide downstream test signals (e.g., pre-defined `Scene Changed: True` flags) for peer system validation.

### Phase 3: Version Control & Repository Architecture
Configure a unified Git repository structure to manage concurrent sub-system development:
* **Branch Strategy:** Maintain a protected `main` branch. Development occurs on feature-isolated branches (e.g., `feature/visual-memory`, `feature/object-detection`).
* **Directory Layout:** Separate domain logic into dedicated paths (e.g., `/src/memory`, `/src/detection`, `/src/spatial`).

### Phase 4: Unit Testing & Dataset Standardization
* **Baseline Dataset:** Acquire and distribute 2–3 static sample video/image sets across all sub-systems to maintain consistent evaluation conditions.
* **Validation Tests:** Construct isolated test suites (e.g., asserting `memory_compare()` yields `True` when an object vector is excised from a mock frame).

### Phase 5: Incremental Integration Schedule
[Phase 1: Detection] ---> [Phase 2: Spatial & Material Analysis] ---> [Phase 3: Visual Memory Pipeline]
1. **Checkpoint A:** Pipe Member 1 (Object Detection) output into Member 2 (Material Understanding).
2. **Checkpoint B:** Map Member 3 (Spatial Distance) calculations onto Member 1 bounding boxes.
3. **Checkpoint C:** Feed consolidated spatial/object descriptors into the AI Visual Memory engine for final scene evaluation.