# 🛣️ Day 5 - Routing

Routing is the process of creating physical electrical connections between placed standard cells, macros, and I/O pins using metal layers while satisfying design rules and timing constraints.

---

# 📚 Objectives

By the end of this session, I was able to:

- Understand the Routing stage in ASIC Physical Design.
- Learn the routing flow in Synopsys ICC2.
- Differentiate between Global Routing and Detailed Routing.
- Understand metal layers and vias.
- Analyze routing congestion and Design Rule Checks (DRC).
- Prepare the design for physical verification and signoff.

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
Placement
      │
      ▼
Clock Tree Synthesis (CTS)
      │
      ▼
⭐ Routing
      │
      ▼
Physical Verification
      │
      ▼
Timing Closure
      │
      ▼
GDSII Generation
```

---

# 📖 What is Routing?

Routing is the process of connecting all placed components using metal wires and vias according to the synthesized netlist while ensuring that all design rules and timing constraints are satisfied.

The routing stage aims to:

- Connect all signal nets.
- Minimize wirelength.
- Meet timing requirements.
- Avoid routing congestion.
- Eliminate Design Rule Violations (DRVs).

---

# 📥 Inputs

Routing requires:

- Placed Design
- Clock Tree
- Technology Files
- LEF Files
- DEF Database
- Design Constraints (SDC)
- Power Distribution Network (PDN)

---

# 📤 Outputs

After Routing, the following are generated:

- Routed Design Database
- Wire Connections
- Via Placement
- DRC Reports
- Timing Reports
- Parasitic Information

---

# 🛣️ Types of Routing

## 1️⃣ Global Routing

Global Routing determines the approximate routing paths for all nets.

Objectives:

- Estimate routing resources.
- Identify congestion hotspots.
- Plan routing paths.

At this stage, exact wire geometries are not created.

---

## 2️⃣ Detailed Routing

Detailed Routing creates the actual metal connections.

It ensures:

- Accurate wire placement.
- Via insertion.
- Compliance with design rules.
- Complete connectivity.

---

# 🔩 Metal Layers

ASIC routing uses multiple metal layers.

Example:

| Layer | Preferred Direction |
|---------|---------------------|
| Metal 1 | Horizontal |
| Metal 2 | Vertical |
| Metal 3 | Horizontal |
| Metal 4 | Vertical |
| Metal 5 | Horizontal |

Alternating routing directions help reduce congestion and simplify manufacturing.

---

# 🔗 Vias

A **Via** connects wires between different metal layers.

Example:

```text
Metal 3
────────────

     ● Via

────────────
Metal 2
```

Proper via placement is important for:

- Signal integrity
- Reliable connectivity
- Manufacturability

---

# 🚦 Routing Congestion

Routing congestion occurs when many nets compete for limited routing resources.

### Causes

- High utilization
- Poor floorplanning
- Large fanout
- Inefficient placement

### Effects

- Routing failures
- Increased delay
- DRC violations
- Timing issues

---

# 📏 Design Rule Check (DRC)

DRC ensures that the layout satisfies foundry manufacturing rules.

Common checks include:

- Minimum wire width
- Minimum spacing
- Via spacing
- Metal density
- Antenna violations
- Short circuits
- Open circuits

---

# ⏱ Timing Analysis After Routing

Routing introduces parasitic resistance and capacitance that affect timing.

Post-routing analysis verifies:

- Setup timing
- Hold timing
- Clock latency
- Signal delay

Timing optimization may involve:

- Buffer insertion
- Cell resizing
- Net optimization

---

# 🛠️ Tool Used

**Synopsys IC Compiler II (ICC2)**

Typical routing tasks include:

- Global Routing
- Detailed Routing
- Via Optimization
- DRC Checking
- Timing Analysis
- Routing Optimization

---

# 📸 Lab Activity

During the lab session, the following tasks were performed:

- Loaded the placed design into ICC2.
- Performed Global Routing.
- Executed Detailed Routing.
- Observed metal layer utilization.
- Inserted vias automatically.
- Reviewed DRC reports.
- Analyzed routing quality and timing.


---

# 💡 Best Practices

- Minimize routing congestion during floorplanning.
- Keep wirelength as short as possible.
- Reduce unnecessary vias.
- Maintain proper spacing between wires.
- Review DRC reports before signoff.
- Verify timing after routing.

---

# 📖 Key Takeaways

- Understood the Routing stage in ASIC Physical Design.
- Learned the difference between Global and Detailed Routing.
- Explored metal layers and via insertion.
- Studied routing congestion and optimization.
- Learned the importance of Design Rule Checks (DRC).
- Prepared the design for physical verification and timing closure.

---

# 🎓 Workshop Summary

Throughout this workshop, I gained hands-on exposure to the complete ASIC Physical Design flow using **Synopsys IC Compiler II (ICC2)**, including:

- Linux Fundamentals
- Design Planning
- Floorplanning
- Placement
- Routing

This workshop strengthened my understanding of backend VLSI design and industry-standard Physical Design methodologies.

---

## 📚 Workshop Navigation

⬅️ [Day-4-Placement](../Day-4-Placement/)
