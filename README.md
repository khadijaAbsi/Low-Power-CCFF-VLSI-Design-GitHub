# Low-Power Conditional Capture Flip-Flop (CCFF) — VLSI Design

A university hardware design project exploring a **Conditional Capture Flip-Flop (CCFF)** through CMOS schematic/layout work and documented simulation measurements.

## Project contents

- **Electric VLSI design:** `Electric-VLSI/ccff_N.jelib` is the primary design library. Inspection of its contents shows CCFF schematic, layout, icon, generated VHDL/netlist views, and a `Reg-Bank` schematic containing repeated CCFF instances.
- **Earlier versions:** `Electric-VLSI/archive/` holds two other supplied `.jelib` files for reference. These are not separately validated releases.
- **Reported measurements:** `Results/pro.docx` contains waveform screenshots, layout screenshots, and captured timing/power measurement results.
- **Screenshots:** `Results/images/` contains selected images **extracted directly from the supplied document**, not newly generated simulation runs.

## Preview

### CCFF layout
![CCFF layout from supplied report](Results/images/cell-layout.png)

### Extended layout
![Extended layout from supplied report](Results/images/extended-layout.png)

### Example simulation waveforms
![Waveforms from supplied report](Results/images/waveforms-1.png)

## Tools and design files

- **Electric VLSI** — `.jelib` library with schematic and layout views (file header reports Electric version 9.07).
- **Simulation evidence** — screenshots of transient waveforms and measurements included in the supplied document. The original simulator project files / model cards were not included in this package.

## Measurement evidence

The supplied report screenshots include `trise`, `tfall`, `pavg`, `tcq_rise`, and `tcq_fall` outputs, alongside setup/hold measurements. **These screenshots reflect various cases, and the source document does not identify a single definitive case-to-design mapping**; no improvement percentage or conclusive benchmark is claimed here.

## Opening the design

1. Install a compatible version of **Electric VLSI**.
2. Open `Electric-VLSI/ccff_N.jelib` as an Electric library.
3. Examine the `ccff_N` schematic and layout cells and the `Reg-Bank` schematic.
4. **Dependency note:** The primary file references external libraries named `CCFF` and `IC_PROJ_1191375_1200902_1200078_1201369`. They are not included in the supplied uploads; missing-cell/dependency warnings may appear. The archive designs reference other libraries as well.
5. For reproducible circuit simulation, add the original simulator schematics, transistor models, stimuli, and scripts when available. The report images are evidence only, not an executable test setup.

## Repository structure

```text
Electric-VLSI/
  ccff_N.jelib
  archive/
    ccff_N_earlier.jelib
    ccff_old.jelib
Results/
  pro.docx
  images/
    cell-layout.png
    extended-layout.png
    waveforms-layout.png
    waveforms-1.png
    waveforms-2.png
    waveforms-3.png
    measurement-example.png
README.md
```

## Project status

**Archived student project; independently unverified in this repository.** The original files are preserved. Layout screenshots and measurements come from the provided document, not from a new simulation or DRC/LVS run. The `Reg-Bank` schematic appears to use 16 instances; function and physical verification have not been independently confirmed here.
