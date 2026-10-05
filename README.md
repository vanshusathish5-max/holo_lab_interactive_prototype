# 🔬 Holo-Lab: Frugal Offline-First AR Framework for Low-Resource STEM Education

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Target Hardware](https://img.shields.io/badge/Target_RAM-2_GB-emerald.svg)](#)
[![Deployment](https://img.shields.io/badge/Architecture-Offline--First-indigo.svg)](#)
[![NCERT Aligned](https://img.shields.io/badge/Curriculum-NCERT_Classes_6--10-amber.svg)](#)

> **Holo-Lab** is a low-cost, offline-first Mobile Augmented Reality (AR) learning architecture engineered specifically for low-resource rural classrooms operating on low-spec Android hardware (2 GB RAM target). It turns standard, physical NCERT textbook diagrams into interactive 3D simulations without requiring cloud bandwidth, proprietary markers, or high-end hardware.

---

## 🌟 Key Features

* **NCERT Target Recognition:** Uses standard physical textbook diagrams (e.g., Class 8 Science, Chapter 16 - Light & Optics) as target visual anchors.
* **On-Device 3D Interactive Viewport:** Real-time 360° rotational and layer-by-layer exploration built on WebGL / Three.js without streaming latency.
* **Text-to-Speech Guidance:** Localized voice explanations of core concepts.
* **"Teach Me" Active-Recall Engine:** Voice-driven active recall module allowing students to explain concepts in their own words via on-device speech transcription.
* **Concept Assessment Module:** Interactive multiple-choice quizzes evaluating immediate learning gains.
* **Frugal System Footprint:** Optimized mesh polygon count and local bundle size ($<80\text{ MB}$) designed for smooth rendering ($\ge 30\text{ FPS}$) on entry-level mobile processors.

---

## 🏗️ System Architecture

```text
[ Physical NCERT Textbook Diagram ]
                 │
                 ▼ (Local Mobile Camera Feed)
       [ On-Device Target Recognition Engine ]
                 │
                 ▼ (Instantiates Local Asset)
    ┌────────────┴────────────┐
    │  3D WebGL AR Viewport   │ ──► Interactive 360° Orbital Control
    └────────────┬────────────┘
                 ├──────────────────────────────┐
                 ▼                              ▼
      [ Local Audio Synthesis ]    [ Active-Recall Speech Engine ]
                 │                              │
                 └──────────────┬───────────────┘
                                ▼
                   [ Concept Assessment Quiz ]
