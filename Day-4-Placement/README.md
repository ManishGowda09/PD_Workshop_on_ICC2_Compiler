# 📍 Day 4 - Placement
Placement is the process of positioning standard cells within the floorplanned core area while optimizing timing, power, area, and routing congestion. It is one of the most important optimization stages in ASIC Physical Design.

---

# 📚 Objectives

By the end of this session, I was able to:

- Understand the Placement stage in the ASIC Physical Design flow.
- Learn different types of placement.
- Understand placement optimization techniques.
- Analyze congestion and timing.
- Prepare the design for Clock Tree Synthesis (CTS).

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
Floorplanning
      │
      ▼
Power Planning
      │
      ▼
⭐ Placement
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

# 📖 What is Placement?

Placement is the stage where **standard cells** are positioned inside the predefined core area created during floorplanning.

The placement engine aims to optimize:

- Timing
- Area
- Power
- Wirelength
- Routing Congestion

A good placement improves overall design quality and simplifies the subsequent Clock Tree Synthesis (CTS) and Routing stages.

---

# 📥 Inputs

The Placement stage uses:

- Floorplanned Design
- Standard Cell Libraries
- Technology Files
- LEF Files
- Timing Constraints (SDC)
- Power Distribution Network (PDN)

---

# 📤 Outputs

After Placement, the design contains:

- Standard Cell Locations
- Optimized Netlist
- Congestion Reports
- Timing Reports
- Placement Database

---

# 🧩 Types of Placement

## 1️⃣ Global Placement

Cells are placed approximately to optimize:

- Wirelength
- Timing
- Congestion

At this stage, cells may overlap.

---

## 2️⃣ Legalization

Legalization adjusts the placement to ensure:

- No overlapping cells
- Cells aligned to placement rows
- Compliance with design rules

---

## 3️⃣ Detailed Placement

Detailed placement fine-tunes cell locations to improve:

- Timing
- Congestion
- Power
- Signal integrity

---

# 📊 Placement Optimization Goals

A placement tool attempts to:

- Minimize wirelength
- Reduce congestion
- Improve setup timing
- Improve hold timing
- Reduce power consumption
- Improve routability

---

# 📈 Congestion

Congestion occurs when too many wires compete for the same routing resources.

### Causes

- High utilization
- Poor macro placement
- Large fanout
- Inefficient placement

### Effects

- Routing failures
- Timing violations
- Increased power
- Longer design closure time

---

# ⏱ Timing Optimization

Placement optimization helps reduce:

- Setup Violations
- Hold Violations
- Clock Latency
- Signal Delay

The placement engine may:

- Move cells
- Resize cells
- Insert buffers
- Optimize net connections

---

# ⚡ Power Optimization

Placement also considers power consumption by:

- Reducing switching activity
- Minimizing wirelength
- Optimizing cell locations
- Reducing clock power

---

# 📐 Placement Quality Metrics

| Metric | Description |
|---------|-------------|
| Wirelength | Total interconnect length |
| Congestion | Routing demand |
| Timing | Setup and Hold Slack |
| Utilization | Core occupancy |
| Power | Dynamic and Leakage Power |

---

# 🛠️ Tool Used

**Synopsys IC Compiler II (ICC2)**

Typical Placement tasks:

- Initialize Placement
- Global Placement
- Legalization
- Detailed Placement
- Congestion Analysis
- Timing Optimization

---

# 📸 Lab Activity

During the lab session, the following tasks were performed:

- Loaded the floorplanned design into ICC2.
- Executed Global Placement.
- Performed Legalization.
- Ran Detailed Placement.
- Observed congestion maps.
- Checked timing reports.
- Analyzed placement quality.


---

# 💡 Best Practices

- Maintain core utilization between **60–70%**.
- Reduce congestion before CTS.
- Keep critical paths as short as possible.
- Minimize unnecessary wirelength.
- Review timing reports after placement.
- Ensure proper legalization before moving to CTS.

---

# 📖 Key Takeaways

- Learned the objectives of Placement.
- Understood Global Placement, Legalization, and Detailed Placement.
- Explored congestion analysis.
- Learned timing optimization techniques.
- Prepared the design for Clock Tree Synthesis.

---

# 🚀 Next Topic

➡️ **Day 5 – Clock Tree Synthesis (CTS) and Routing**

The next session focuses on building the clock distribution network, minimizing clock skew, and routing signal connections across the chip.

---

## 📚 Workshop Navigation

⬅️ [Day-3-Floor_Planning](../Day-3-Floor_Planning/)

➡️ [Day-5-Routing](../Day-5-Routing/)
