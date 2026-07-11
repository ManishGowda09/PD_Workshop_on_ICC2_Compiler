# 🏗️ Day 2 - Design Planning

Design Planning is the first stage of the ASIC Physical Design flow after logic synthesis. It involves defining the chip layout, allocating the core area, placing macros, and preparing the design for floorplanning and placement.

---

# 📚 Objectives

By the end of this session, I was able to:

- Understand the purpose of Design Planning.
- Learn the inputs and outputs of the Design Planning stage.
- Calculate core utilization and aspect ratio.
- Understand macro placement and I/O planning.
- Prepare the design for Floorplanning.

---

# 🔄 ASIC Physical Design Flow

```text
RTL Design
      │
      ▼
Logic Synthesis
      │
      ▼
⭐ Design Planning
      │
      ▼
Floorplanning
      │
      ▼
Power Planning
      │
      ▼
Placement
      │
      ▼
Clock Tree Synthesis (CTS)
      │
      ▼
Routing
      │
      ▼
Physical Verification
      │
      ▼
GDSII Generation
```

---

# 📖 What is Design Planning?

Design Planning is the process of defining the overall chip layout before placing standard cells. It determines the chip size, core dimensions, macro locations, and I/O pin arrangement, ensuring that the design can be implemented efficiently while meeting timing, power, and area constraints.

---

# 📥 Inputs to Design Planning

The Design Planning stage typically requires:

- Synthesized Netlist
- Standard Cell Library
- Technology Library
- Timing Constraints (SDC)
- Design Rules
- LEF Files
- Floorplanning Constraints

---

# 📤 Outputs of Design Planning

After completing Design Planning, the following are generated:

- Chip Boundary
- Core Area
- Macro Placement
- I/O Pin Locations
- Blockages
- Placement Constraints

These outputs are used in the Floorplanning stage.

---

# 📐 Core Area

The **Core Area** is the region where standard cells are placed.

```text
+--------------------------------------+
|             Chip Area                |
|                                      |
|  +-------------------------------+   |
|  |          Core Area            |   |
|  |                               |   |
|  | Standard Cells & Macros       |   |
|  |                               |   |
|  +-------------------------------+   |
|                                      |
+--------------------------------------+
```

---

# 📊 Utilization

Utilization is the percentage of the core area occupied by standard cells.

### Formula

```text
Utilization (%) =
(Standard Cell Area / Core Area) × 100
```

Typical utilization values:

| Utilization | Description |
|--------------|------------|
| 50–60% | Low congestion |
| 60–70% | Recommended |
| 70–80% | High utilization |
| >80% | Difficult routing and timing closure |

---

# 📏 Aspect Ratio

The Aspect Ratio determines the shape of the core.

### Formula

```text
Aspect Ratio = Height / Width
```

Examples:

| Height | Width | Aspect Ratio |
|---------|-------|--------------|
| 1000 µm | 1000 µm | 1.0 (Square) |
| 1200 µm | 800 µm | 1.5 |
| 800 µm | 1200 µm | 0.67 |

A balanced aspect ratio helps improve placement and routing efficiency.

---

# 🧩 Macro Placement

Macros are large pre-designed blocks such as:

- SRAM
- ROM
- PLL
- Analog IP
- DSP Blocks

### Guidelines

- Place macros near related logic.
- Avoid placing macros at the center of the core unless required.
- Leave routing channels between macros.
- Reserve space for power planning.

---

# 📍 I/O Planning

I/O Planning determines the location of input and output pins around the chip boundary.

Good I/O placement helps:

- Reduce wirelength.
- Improve timing.
- Minimize routing congestion.

---

# 🚧 Placement Blockages

Placement blockages reserve specific regions where standard cells cannot be placed.

They are used to:

- Protect macro regions.
- Reduce congestion.
- Reserve routing space.

---

# 📈 Design Constraints

Important constraints considered during Design Planning include:

- Area
- Timing
- Power
- Congestion
- Manufacturability

Balancing these constraints is essential for achieving an optimized layout.

---

# 🛠️ Tool Used

- Synopsys IC Compiler II (ICC2)

Typical tasks performed in ICC2:

- Import synthesized netlist
- Load technology libraries
- Define chip boundary
- Configure core utilization
- Place macros
- Define I/O pins

---

# 📸 Lab Activity

During the lab session, the following tasks were performed:

- Opened the design in ICC2.
- Imported the synthesized netlist.
- Examined the chip boundary.
- Defined the core area.
- Explored macro placement.
- Observed utilization settings.
- Prepared the design for Floorplanning.

<img width="1416" height="842" alt="Screenshot 2026-07-10 161511" src="https://github.com/user-attachments/assets/5d77b97a-1354-4d1a-adc7-b6df3c07af1a" />


---

# 💡 Best Practices

- Choose an appropriate core utilization (typically 60–70%).
- Maintain a balanced aspect ratio.
- Leave enough routing channels between macros.
- Plan power distribution early.
- Keep critical macros close to associated logic.

---

# 📖 Key Takeaways

- Understood the role of Design Planning in the ASIC flow.
- Learned how to define the chip and core area.
- Calculated utilization and aspect ratio.
- Explored macro placement and I/O planning.
- Prepared the design for the Floorplanning stage.

---

# 🚀 Next Topic

➡️ **Day 3 – Floorplanning**

The next session focuses on Floorplanning, where the chip layout is refined by placing macros, creating the power distribution network (PDN), and preparing the design for standard-cell placement.
💡 Tip for Your Repository
