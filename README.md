# 3D Printable Mechanical Polar Planimeter

An open-source, parametric 3D-printable **Polar Planimeter**—an analog mechanical integration device used to measure the surface area of any arbitrary 2D shape by tracing its perimeter.

This project translates **Green's Theorem** from multivariable calculus into a functional physical mechanism using mechanical linkages and a precision measuring wheel.

---

## 🛠️ Features

* **Fully Parametric Design:** Modeled for clean assembly, precise joint alignments, and smooth kinematic motion.
* **Pure Mechanical Integration:** Computes 2D enclosed surface areas mechanically without microprocessors or electronic sensors.
* **Optimized for 3D Printing (DFAM):** Engineered with tuned tolerances for standard FDM desktop printers.
* **Modular Assembly:** Uses print-in-place or pin-joint connectors for easy calibration and part replacement.

---

## 📐 How It Works

A polar planimeter converts a line integral along a closed boundary ($\partial D$) into the enclosed area ($A$) of a shape using a tracer arm, an anchor point, and a perpendicular integrating wheel:

$$\oint_{\partial D} (L\,dx + M\,dy) = \iint_D dA$$

1. **Fix the Anchor:** Place the weighted pole/anchor point at a fixed location outside or inside the shape.
2. **Trace the Contour:** Trace the perimeter of the 2D shape clockwise using the tracer stylus.
3. **Read the Wheel:** The integrating wheel rolls during lateral motion and slides during longitudinal motion. The net rotation read off the graduated scale corresponds directly to the shape's enclosed area.

---

## 📂 Repository Structure

```text
├── CAD/
│   ├── Assemblies/      # Complete CAD assembly files (.STEP, .F3D, .SLDASM)
│   └── Components/      # Individual part models (Tracer Arm, Anchor, Wheel Housing)
├── STL/                 # Ready-to-print 3D STL files
├── Documentation/       # Assembly guide, mathematical derivation, and calibration chart
└── README.md

```

---

## 🖨️ Recommended Print Settings

| Parameter | Recommended Value |
| --- | --- |
| **Material** | PLA, PETG, or ABS |
| **Layer Height** | 0.12mm – 0.20mm (lower layer height for smooth joints) |
| **Infill** | 20% – 30% (increase anchor pole infill to 80%+ for stability) |
| **Supports** | Minimal / Touching Buildplate Only |
| **Perimeters/Walls** | 3 - 4 walls |

> **Note on Mechanical Tolerances:** Ensure your printer's flow rate/extrusion multiplier is calibrated to prevent joint binding.

---

## 🔧 Assembly Instructions

1. **Prep Parts:** Lightly sand pin joints and the contact edge of the integrating wheel to remove burrs or seam ridges.
2. **Assemble Linkages:** Connect the anchor pole arm to the tracer arm using the central revolute joint pin. Verify that the tracer arm swings freely without vertical play.
3. **Install the Wheel:** Mount the measuring wheel perpendicularly to the tracer arm. Ensure it spins smoothly on its axis with minimal axial friction.
4. **Calibration:** Trace a known square or circle (e.g., $10\text{ cm} \times 10\text{ cm} = 100\text{ cm}^2$) to calculate your model's wheel scale multiplier.

---

## 📜 License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE).