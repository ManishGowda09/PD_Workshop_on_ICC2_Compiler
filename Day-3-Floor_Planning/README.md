# 🏢 Day 3 - Floorplanning

Floorplanning is one of the most critical stages in ASIC Physical Design. It defines the physical layout of the chip by determining the core area, placing macros, planning power distribution, and allocating routing resources before standard-cell placement.

---

# 📚 Objectives

By the end of this session, I was able to:

- Understand the purpose of Floorplanning.
- Learn how to define the chip and core boundaries.
- Place macros efficiently.
- Plan the Power Distribution Network (PDN).
- Create routing channels and keep-out margins.
- Prepare the design for Placement.

---

# 🔄 ASIC Physical Design Flow

```text
RTL Design
      │
      ▼
Logic Synthesis
      │
      ▼
Design Planning
      │
      ▼
⭐ Floorplanning
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

# 📖 What is Floorplanning?

Floorplanning is the process of defining the physical layout of an integrated circuit by arranging the core area, placing macros, planning power delivery, and reserving routing resources.

A well-designed floorplan helps achieve:

- Better timing
- Lower congestion
- Reduced wirelength
- Lower power consumption
- Improved manufacturability

---

# 📥 Inputs

Floorplanning requires:

- Synthesized Netlist
- Technology Library
- LEF Files
- Design Constraints (SDC)
- Standard Cell Libraries
- Macro Information

---

# 📤 Outputs

After Floorplanning, the design contains:

- Chip Boundary
- Core Boundary
- Macro Placement
- I/O Pin Locations
- Power Rings
- Power Stripes
- Placement Blockages
- Routing Blockages
- Keep-Out Margins

---

# 🏗️ Floorplan Structure

```text
+------------------------------------------------+
|                  Chip Boundary                 |
|                                                |
| +--------------------------------------------+ |
| |                Core Area                   | |
| |                                            | |
| |   SRAM        Routing Channel      SRAM    | |
| |                                            | |
| |          Standard Cell Region              | |
| |                                            | |
| +--------------------------------------------+ |
|                                                |
+------------------------------------------------+
```

---

# 🧩 Macro Placement

Macros are large pre-designed blocks such as:

- SRAM
- ROM
- PLL
- Analog IP
- DSP Blocks

### Best Practices

- Place macros near related logic.
- Keep macros close to the chip boundary when appropriate.
- Avoid overlapping macros.
- Leave routing channels between macros.
- Reserve space for power routing.

---

# ⚡ Power Planning

Power Planning ensures reliable power delivery across the chip.

It consists of:

- Power Rings
- Power Stripes
- VDD Network
- VSS (Ground) Network

Example:

```text
+--------------------------+
|==========================| ← VDD Ring
|                          |
| ||  ||  ||  ||  ||  ||   | ← Power Stripes
|                          |
|==========================| ← VSS Ring
+--------------------------+
```

---

# 🚧 Keep-Out Margins

Keep-Out Margins reserve space around macros where standard cells cannot be placed.

Benefits include:

- Reduced congestion
- Improved routing
- Better timing
- Easier ECO implementation

---

# 🚫 Placement Blockages

Placement blockages prevent standard cells from being placed in specific regions.

Common uses:

- Around macros
- Reserved routing areas
- Analog regions
- Clock routing paths

---

# 🛣️ Routing Channels

Routing channels are spaces intentionally left between macros to allow signal routing.

Benefits:

- Reduced congestion
- Easier routing
- Improved timing closure

---

# 📍 Pin Placement

I/O pins should be placed to:

- Reduce wirelength
- Minimize congestion
- Improve timing
- Simplify routing

---

# 📊 Important Floorplanning Parameters

| Parameter | Description |
|-----------|-------------|
| Core Utilization | Percentage of area occupied by standard cells |
| Aspect Ratio | Height / Width of the core |
| Core Margin | Distance between chip boundary and core |
| Routing Channel | Space between macros |
| Keep-Out Margin | Reserved space around macros |

---

# 🛠️ Tool Used

**Synopsys IC Compiler II (ICC2)**

Typical Floorplanning tasks:

- Create Floorplan
- Define Core Area
- Place Macros
- Create Power Rings
- Create Power Stripes
- Define Placement Blockages
- Configure Routing Constraints

---

# 📸 Lab Activity

During the lab session, the following tasks were performed:

- Opened the synthesized design in ICC2.
- Created the chip floorplan.
- Defined the core boundary.
- Placed macros.
- Observed routing channels.
- Configured keep-out margins.
- Explored the Power Distribution Network (PDN).

---

# 💡 Best Practices

- Keep utilization between **60–70%**.
- Minimize macro-to-macro congestion.
- Leave sufficient routing channels.
- Keep critical macros close to related logic.
- Plan the power network before placement.
- Use keep-out margins around large macros.

---

# 📖 Key Takeaways

- Understood the purpose of Floorplanning.
- Learned how to define chip and core boundaries.
- Explored macro placement strategies.
- Understood Power Distribution Network (PDN) planning.
- Learned about routing channels and keep-out margins.
- Prepared the design for the Placement stage.

---

# 🚀 Next Topic

➡️ **Day 4 – Placement**

The next stage focuses on placing standard cells within the floorplan while optimizing timing, area, congestion, and power consumption.

---

## 📚 Workshop Navigation

⬅️ [Day-2-Design_Planning](../Day-2-Design_Planning/)

➡️ [Day-4-Placement](../Day-4-Placement/)
