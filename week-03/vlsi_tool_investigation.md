# Week 3 — Open-Source VLSI Tool Investigation

## 1. Tool Selected
**Tool name:** OpenROAD

**Track:** Physical Design (PD)

**Official website:** https://openroad.org/

**GitHub repository:** https://github.com/The-OpenROAD-Project/OpenROAD

## 2. What Problem Does the Tool Solve?
OpenROAD helps automate digital chip physical implementation. It supports the process of transforming a synthesized digital design into a physical layout through stages such as floorplanning, placement, clock tree synthesis, routing, and finishing.

## 3. Main Inputs and Outputs

**Main inputs:**
- Synthesized Verilog netlist or RTL through the complete flow
- Timing constraints, commonly provided in SDC format
- Standard-cell libraries and technology files
- LEF files describing physical cells and layout information
- Flow configuration and design parameters

**Main outputs:**
- Placed and routed design data
- Timing and physical-design reports
- Log files and implementation metrics
- GDSII layout output from a completed flow

The exact files depend on the selected flow and configuration.

## 4. Basic Workflow
A typical OpenROAD-flow-scripts workflow includes:

1. **Synthesis:** Convert RTL into a gate-level netlist.
2. **Floorplanning:** Define the chip/core area and plan power distribution.
3. **Placement:** Position standard cells and optimize their arrangement.
4. **Clock Tree Synthesis (CTS):** Build the clock distribution network.
5. **Routing:** Connect cells using metal interconnects.
6. **Finishing and checks:** Generate final layout data and review timing and physical-design reports.

## 5. What I Explored
I reviewed the official OpenROAD website and documentation to understand its purpose, basic workflow, inputs, and outputs.

I learned how the main implementation stages connect and how the flow produces design data and reports.

**Practical trial status:** Documentation reviewed. I have not yet run a complete OpenROAD implementation flow.

## 6. Where Could AI or ML Help?
AI/ML could potentially help with:
- Predicting timing violations from earlier implementation results.
- Identifying designs that may have high congestion.
- Analysing placement and routing reports to highlight possible problem areas.
- Exploring implementation parameters more efficiently.

These are possible applications, not results from an experiment I performed.

## 7. Limitations and Considerations
- Running a complete flow requires compatible design files, technology libraries, constraints, and configuration.
- Understanding the reports requires knowledge of Physical Design concepts.
- Results depend on the design, technology platform, and flow settings.
- Generated layouts and reports must be checked; successful execution alone does not establish that a design is ready for manufacturing.

## 8. Sources and Verification
I used the following official sources to investigate the tool:

1. OpenROAD documentation: https://openroad.readthedocs.io/en/latest/
2. OpenROAD-flow-scripts documentation: https://openroad-flow-scripts.readthedocs.io/en/latest/mainREADME.html
3. OpenROAD source-code repository: https://github.com/The-OpenROAD-Project/OpenROAD

I used these sources to check the tool's purpose and the stages of its implementation flow.

## 9. What I Learned
I learned that OpenROAD provides an open-source way to study digital Physical Design workflows. Its stages connect floorplanning, placement, clock tree synthesis, routing, and finishing. AI/ML could assist engineers in analysing reports and exploring design options, but engineering results still require verification.
