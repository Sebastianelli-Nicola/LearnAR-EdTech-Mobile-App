# Learn AR — Augmented Reality Mobile Platform for Computer Architecture Education

[![Thesis: UNIVPM Open Archive](https://img.shields.io/badge/UNIVPM%20Open%20Archive-Handle%3A%2017991-003366.svg?style=for-the-badge&logo=internet-archive&logoColor=white)](https://hdl.handle.net/20.500.12075/17991)
[![Framework: Flutter](https://img.shields.io/badge/Framework-Flutter-02569B.svg?style=for-the-badge&logo=flutter&logoColor=white)](#tech-stack)
[![Language: Dart](https://img.shields.io/badge/Language-Dart-0175C2.svg?style=for-the-badge&logo=dart&logoColor=white)](#tech-stack)
[![AR Engine: Vuforia & Unity](https://img.shields.io/badge/AR_Engine-Vuforia%20%7C%20Unity-black.svg?style=for-the-badge&logo=unity&logoColor=white)](#tech-stack)
[![3D Modeling: Blender](https://img.shields.io/badge/3D_Modeling-Blender-E87D0D.svg?style=for-the-badge&logo=blender&logoColor=white)](#tech-stack)
[![Backend: Firebase](https://img.shields.io/badge/Backend-Firebase-FFCA28.svg?style=for-the-badge&logo=firebase&logoColor=black)](#tech-stack)

**Learn AR** is a cross-platform mobile application developed as an **experimental Bachelor's Degree Thesis (*Tesi Sperimentale di Laurea Triennale*)** at **Università Politecnica delle Marche (UNIVPM)**.

The project demonstrates how combining physical study materials with marker-based Augmented Reality (AR) and interactive 3D spatial models overcomes the communicative bottlenecks of traditional static textbooks, transforming abstract computing hardware concepts into an interactive, self-paced learning environment.

---

## Academic Context & Thesis Record

This application was engineered and validated as part of an experimental Bachelor's thesis and academic internship at the Department of Information Engineering (DII), Università Politecnica delle Marche.

* **Thesis Title:** *Learn AR: Augmented Reality Application to Support Education*
* **Author:** **Nicola Sebastianelli** — [GitHub](https://github.com/Sebastianelli-Nicola)
* **Degree:** B.Sc. in Computer and Automation Engineering (*Ingegneria Informatica e dell'Automazione*)
* **Institution:** Università Politecnica delle Marche (UNIVPM), Ancona, Italy
* **Academic Year / Completion:** 2023 / 2024
* **Official Institutional Handle (Permarecord):** [hdl.handle.net/20.500.12075/17991](https://hdl.handle.net/20.500.12075/17991)

---

## Live Demo & Application Package

* **Demonstration Video:** [Download MP4 Walkthrough](https://www.dropbox.com/scl/fi/lre5e3au6ygyoz6lopy4d/learn_ar_video.mp4?rlkey=u4csvye7gumuiur60em5pabve&dl=0)
* **Android Release Package:** [Download learn-ar.apk](https://www.dropbox.com/scl/fi/agwcf24stospe66e0hkno/learn-ar.apk?rlkey=ckxfwvvnbrjec9ybq1hwtj4wq&dl=0)
* **Institutional University Archive:** [UNIVPM Open Research Archive Handle: 17991](https://hdl.handle.net/20.500.12075/17991)

---

## Educational Case Study: Computer Architecture

Traditional computer architecture textbooks rely primarily on 2D planar block diagrams that fail to communicate internal physical hierarchy, real-world pinout structures, and cooling constraints. Learn AR introduces an interactive spatial overlay for physical course literature:

1. **Target Image Calibration:** Standard 2D diagrams printed on the physical textbook pages serve as high-contrast feature targets.
2. **Real-Time AR Projection:** Pointing the device camera at any recognized figure projects a scaled, fully interactive 3D component directly anchored to the page.
3. **Hardware Modules Implemented:**
   * **Central Processing Unit (CPU):** Explores silicon die topology, core clusters, socket array, and execution pipeline units.
   * **Graphics Processing Unit (GPU):** Visualizes parallel compute blocks, memory bus routing, GDDR VRAM placement, and heatsink mounting.
   * **Random Access Memory (RAM):** Highlights DIMM pinouts, SPD EEPROM logic, trace routing, and multi-channel memory banks.

---

## Key Features

* **Sub-Millimeter Optical Tracking:** High-stability 2D target recognition engineered with the Vuforia Engine inside Unity, eliminating spatial jitter.
* **Full Multi-Touch 3D Pipeline:** Touch-driven viewport navigation supporting multi-axis orbit rotation, smooth continuous pinch-to-zoom, and exploded module breakdowns.
* **Hand-Sculpted Low-Poly 3D Assets:** Custom hardware models modeled, UV-unwrapped, and textured in Blender, optimized for mobile rasterization and a consistent 60 FPS frame rate.
* **Integrated Assessment Engine:** Interactive multiple-choice hardware quizzes synchronized with the 3D models to test student retention immediately following module inspection.
* **Flutter-Unity Hybrid Architecture:** High-performance native platform channel linking Flutter's declarative UI layer with the underlying Unity rendering canvas.

---

## System Architecture

```text
       [ Physical Textbook Page (Image Target) ]
                           │
                           ▼  (Camera Video Stream)
       [ Vuforia Engine — Spatial Image Recognition ]
                           │
                           ▼  (Pose & Transform Matrix)
       [ Unity 3D Engine — Hardware Asset Renderer ]
                           │
                           ▼  (Flutter-Unity Widget Bridge)
┌──────────────────────────────────────────────────────────┐
│              Flutter Mobile App (Dart)                   │
│  - User Interface, Lesson Nav & Touch Controls          │
│  - Interactive Knowledge Assessment / Quiz Engine        │
└──────────────────────────┬───────────────────────────────┘
                           │
                           ▼  (Cloud Sync)
              [ Google Firebase Services ]
          (Auth, Cloud Storage, Quiz Scores)
```

---

## Tech Stack

* **Mobile App Framework:** Flutter (Dart)
* **AR Tracking Engine:** Vuforia Engine
* **3D Runtime Environment:** Unity
* **3D Asset Design & Texturing:** Blender
* **Cloud Backend & Database:** Google Firebase
* **Target OS:** Android (SDK 24+)

---

## Getting Started

### Prerequisites
* Flutter SDK (v3.0+)
* Android Studio with Android SDK & NDK installed
* Physical Android smartphone with AR camera capabilities

### Local Build & Installation
```bash
# 1. Clone the repository
git clone https://github.com/Sebastianelli-Nicola/learn_ar.git
cd learn_ar

# 2. Install project dependencies
flutter pub get

# 3. Connect device via USB debugging and launch
flutter run --release
```

---

## Author
* **Nicola Sebastianelli** — [GitHub Profile](https://github.com/Sebastianelli-Nicola)
