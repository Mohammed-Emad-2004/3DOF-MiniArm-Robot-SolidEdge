# 🦾 3-DOF MiniArm Robotic Manipulator — Solid Edge 2026

> **Mohammed Emad Said Soliman** | UHCI4H  
> Mechatronics Engineering BSc. — University of Debrecen  
> Faculty of Engineering | Department of Electrical Engineering and Mechatronics  
> *Modelling and Simulation Prototype Technologies II — 2025/2026/II. Semester*

---

## 📋 Overview

This project presents the complete **mechanical design of a 3-DOF articulated robotic manipulator** called **MiniArm**, built as the second homework assignment for Modelling and Simulation Prototype Technologies II.

The robot features **three revolute joints** — waist (J1), shoulder (J2), and elbow (J3) — giving a planar workspace of approximately **230 mm** with a payload capacity of **100 g**.

All custom parts were designed in **Solid Edge 2026**, technical drawings exported to PDF, and model files saved in `.stl` format for 3D printing.

---

## 🎯 Design Goals

- Use **only three Faulhaber 3242G 012CR** permanent magnet brushed DC motors as the sole actuators
- Achieve a clean, manufacturable assembly using **3D-printed ABS** motor housings and **aluminium link plates**
- Internal cable routing for a clean build
- Suitable for **educational demonstration** and future controller integration

---

## ⚙️ Motor Specifications

**Motor:** Faulhaber 3242G 012CR — Permanent Magnet Brushed DC Motor

| Parameter | Value |
|-----------|-------|
| Actuators | 3× Faulhaber 3242G 012CR |
| Gearhead | Faulhaber 32/3R Planetary |
| Joint 1 (Waist) Gear Ratio | 66:1 |
| Joint 2 (Shoulder) Gear Ratio | 43:1 |
| Joint 3 (Elbow) Gear Ratio | 14:1 |
| Safety Factor (all joints) | > 2.0 |

---

## 🔩 Robot Architecture

### Joints
| Joint | Type | Location |
|-------|------|----------|
| J1 | Revolute | Waist |
| J2 | Revolute | Shoulder |
| J3 | Revolute | Elbow |

### Links
| Part | Material | Manufacturing |
|------|----------|--------------|
| Motor housings (Links 1–5) | ABS | 3D Printed |
| End-effector plate | Aluminium | Machined |
| PCB (CAXX Techniques) | — | Mounted in Base |

### Motor Mounting
- **Front flange**: bolted directly to proximal link housing; provides primary axial retention
- **Rear stabilization screws**: anti-rotation lock to handle high reaction torques from gearheads
- Both faces fastened — joints will not loosen under cyclic pick-and-place, sudden direction changes, or stall conditions

---

## 📁 Project Structure

```
├── 📦 Parts (.par)                   — Solid Edge part files
│   ├── Base.par                      — Robot base
│   ├── Link1.par – Link5.par         — Arm links
│   ├── 32-3R_2stage.par              — Gearhead 2-stage
│   ├── 32-3R_3stage.par              — Gearhead 3-stage
│   ├── 32-3R_flange_a.par            — Gearhead flange
│   ├── 3242G_CR.par                  — Faulhaber motor body
│   └── CAXX_PCB.par                  — Custom PCB part
│
├── 🔧 Assemblies (.asm)
│   ├── Final Assembly.asm            — Complete robot assembly
│   ├── Exploded View.asm             — Exploded view assembly
│   └── F1.asm                        — Sub-assembly
│
├── 📐 drawings/                      — Solid Edge drawing files (.dft)
│   ├── Final Assembly.dft
│   ├── Final Assembly Exploded View.dft
│   ├── Link1.dft – Link5.dft
│   ├── Base.dft
│   ├── PCB_CAXX.dft
│   └── ...
│
├── 📂 UHCI4H_Final_submittion/
│   ├── Parts/                        — STL + log files for all parts
│   ├── PDFs/                         — Technical drawings (PDF)
│   └── UHCI4H FInal Report.pdf       — Full project report (PDF)
│
├── 📂 UHCI4H_Modeling Assignemnt/    — Intermediate submission
│   ├── *.stl                         — STL exports
│   ├── *.pdf                         — Part drawings
│   └── UHCI4H FInal Report.pdf
│
├── UHCI4H FInal Report.docx          — Full project report (Word)
├── UHCI4H_Final_submittion.zip       — Final submission archive
└── UHCI4H_Modeling Assignemnt.zip    — Modeling assignment archive
```

---

## 🏗️ Key Design Features

### ✅ 16 Custom Parts
All 16 custom components modeled from scratch in Solid Edge 2026.

### ✅ Integrated PCB Mount
Custom PCB from CAXX Techniques course is housed directly in the robot base.

### ✅ Cable Management
- Internal cable routing through fixed Link 1 housing to base
- External routing on moving links for easy maintenance

### ✅ Torque Validation
Motor torque validated with safety factors above **2.0** for all joints under full load.

### ✅ 3D Print Ready
All housing parts exported to `.stl` format and ready for 3D printing in ABS.

---

## 📊 Workspace

| Parameter | Value |
|-----------|-------|
| DOF | 3 |
| Joint types | Revolute (R-R-R) |
| Reach | ~230 mm |
| Payload | 100 g |
| Configuration | Planar articulated |

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **Solid Edge 2026** | 3D modeling & technical drawings |
| **PDF export** | Technical drawing documentation |
| **STL export** | 3D printing preparation |

---

## 📄 Report

The full design report includes:
- Motor parameter analysis (from Electrical Machines & Drives assignment)
- Joint torque calculations and safety factor validation
- Assembly sequence and fastener plan
- Technical drawings for all 16 custom parts

📥 See [`UHCI4H_Final_submittion/UHCI4H FInal Report.pdf`](UHCI4H_Final_submittion/UHCI4H%20FInal%20Report.pdf)

---

*Mechatronics Engineering BSc. — University of Debrecen, 2026*
