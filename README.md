# mixed-signal-physical-design
Mixed-Signal Physical Design using OpenLane and SKY130 through the RTL-to-GDS flow.
# AI-Assisted Mixed-Signal Physical Design using OpenLane and SKY130

## Project Overview

This repository documents the implementation and analysis of a mixed-signal physical design flow using OpenLane and the SKY130 Process Design Kit (PDK). The work is based on studying the reference repository **vsdmixedsignalflow** and reproducing a similar RTL-to-GDSII flow while incorporating AI-assisted learning, debugging, and documentation techniques.

The project focuses on understanding how an analog IP (2:1 Analog Multiplexer - AMUX2_3V) can be integrated into a digital implementation flow using LEF, Verilog, and OpenLane configuration files.

The complete flow was executed on Ubuntu (WSL) using open-source EDA tools.

---

## Objectives

* Study the fundamentals of mixed-signal physical design.
* Understand analog macro integration within OpenLane.
* Learn the purpose of LEF, LIB, DEF, and GDS files.
* Execute the RTL-to-GDSII flow using OpenLane.
* Debug synthesis and implementation issues.
* Analyze timing, DRC, LVS, and manufacturability reports.
* Explore how AI tools can accelerate engineering workflows.

---

## Reference Repository

This work was inspired by the following repository:

* https://github.com/praharshapm/vsdmixedsignalflow

The goal was not to copy the implementation directly but to understand the methodology and reproduce similar results while documenting the complete learning and debugging process.

---

## AI-Assisted Workflow

AI tools were used throughout the project to:

* Understand repository structure and workflow
* Break the project into smaller milestones
* Explain mixed-signal design concepts
* Analyze OpenLane error logs
* Debug synthesis and configuration failures
* Interpret timing and signoff reports
* Organize technical documentation

All generated suggestions were manually verified before implementation.

Additional details are available in:

```text
prompts/chatgpt_workflow.md
```

---

## Project Structure

```text
mixed-signal-physical-design
│
├── README.md
├── docs
├── debugging
├── screenshots
├── reports
├── prompts
├── resources
└── ieee_report
```

---

## OpenLane Flow Studied

The following stages were explored during implementation:

1. Repository Analysis
2. OpenLane Setup
3. Analog Macro Study
4. Configuration Preparation
5. Synthesis
6. Floorplanning
7. Placement
8. Clock Tree Synthesis
9. Routing
10. Signoff Checks
11. GDS Generation
12. Layout Visualization using Magic

---

## Debugging Journey

Several implementation issues were encountered and resolved during development.

Major issues included:

* Verilog linter failures
* Missing configuration entries
* Duplicate module definitions
* Signal naming mismatches
* Analog macro integration issues
* Synthesis failures

Each issue, root cause, and resolution has been documented in:

```text
debugging/
```

---

## Results

### OpenLane Flow Status

* Flow Status: Completed Successfully
* GDS Generated: Yes
* DEF Generated: Yes
* LEF Generated: Yes

### Verification Results

| Check          | Status     |
| -------------- | ---------- |
| DRC            | Passed     |
| LVS            | Clean      |
| Setup Timing   | Met        |
| Hold Timing    | Met        |
| GDS Generation | Successful |

### Important Metrics

| Metric              | Value   |
| ------------------- | ------- |
| Synthesized Cells   | 301     |
| Total Cells         | 15256   |
| Critical Path       | 6.56 ns |
| Clock Period        | 10 ns   |
| Suggested Frequency | 100 MHz |
| DRC Violations      | 0       |
| LVS Errors          | 0       |

Detailed reports are available in:

```text
reports/
```

---

## Screenshots

The repository contains screenshots from different stages of the implementation flow:

### Flow Execution

```text
screenshots/flow
```

### Magic Layout Visualization

```text
screenshots/magic
```

### Report Analysis

```text
screenshots/reports
```

---

## Key Learnings

Through this project I gained practical exposure to:

* Mixed-signal physical design concepts
* Analog macro integration
* LEF and LIB usage
* OpenLane implementation flow
* Timing analysis
* DRC and LVS verification
* GDSII generation
* AI-assisted engineering workflows
* Systematic debugging techniques

---

## Future Improvements

Potential future extensions include:

* Integration of additional analog macros
* Multi-macro floorplanning studies
* Timing optimization experiments
* Power optimization analysis
* Full custom mixed-signal subsystem implementation
* Comparison with commercial EDA flows

---

## Conclusion

This project successfully reproduced a mixed-signal RTL-to-GDSII implementation flow using OpenLane and SKY130 while documenting an AI-assisted engineering workflow. The work demonstrates how open-source EDA tools combined with structured AI guidance can accelerate learning, debugging, and implementation of physical design concepts.
