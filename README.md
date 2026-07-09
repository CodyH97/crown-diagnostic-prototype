# Crown Appliances — Field Diagnostics (prototype)

A clickable prototype of a guided appliance diagnostic tool for Chadwell Supply maintenance techs.

Enter or "scan" a Crown Appliances refrigerator model number, then diagnose it one of two ways:

- **Guided Q&A** — answer a couple of symptom questions and the tool narrows down the likely cause and the exact part to order.
- **Diagnostic reader** — simulates plugging Chadwell's physical diagnostic reader into the appliance's service port. It "reads" the fault code straight off the control board plus live sensor telemetry (cabinet/freezer temp, compressor draw, fan RPM, etc.) and jumps straight to the cause and part — no questions needed. About 1 in 7 reads come back with no active fault, which falls back to the guided Q&A flow, showing how the two methods work together.

The result screen always shows a source badge (`Read from unit · Fault E8` vs `Guided Q&A · <path>`) and the session log at the bottom tags each entry with `[reader]` or `[guided]`, so the pitch can call out which path a tech used.

**[Live demo](https://codyh97.github.io/crown-diagnostic-prototype/)** 

## Pilot models
- CR-1800
- CR-2400
- CR-3000

## Status
Prototype for internal pitch purposes. Decision-tree data (`TREE` object) and reader fault-code data (`FAULT_CODES` object, in `index.html`) use placeholder causes/parts and simulated telemetry — swap in real failure data and an actual reader integration before using with techs in the field.
