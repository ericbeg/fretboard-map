## Overview  

The `_SPECS` folder serves as a **living documentation system** that mirrors the current state of the software.  
It provides structured, human-readable specifications that evolve alongside the source code and other project artifacts.  

This system ensures that **every code change** is reflected in the specifications, keeping development, documentation, and reasoning tools perfectly aligned.  

---

## Folder Structure  

### Index File
The `_SPECS/index.md` file acts as the **table of contents** for the entire specification system.

Its purpose is to:
- Provide a **high-level overview** of all documented modules and components.
- List the relative paths to each `_SPECS/*.md` file.
- Include a brief **summary** of each file’s contents and purpose.
- Help both human readers and LLMs **navigate** the specification folder quickly and accurately.

### `_SPECS/`  
Contains one specification (`.md`) file per module or subsystem.  
Each file documents the following sections:  

- **Title** – Name of the module or component.  
- **Summary** – Brief description of the module’s purpose and functionality.  
- **Features** – Bullet list describing key capabilities.  
- **Inputs / Outputs** – Data accepted and returned by this module.  
You may also include additional sections if they clarify architecture, dependencies, or workflows.  

---

## Maintenance Guidelines  

1. **Update After Every Change**  
   - Whenever you modify a module, function, or configuration, locate its corresponding spec file in `_SPECS/`.  
   - Add or adjust details to match the new implementation.  
   - If a new module is introduced, create a new spec file using the standard structure above.  

2. **Maintain Consistency**  
   - Ensure summaries and features accurately reflect the source code.  
   - Cross-reference related modules where applicable.  

3. **Batch Updates (Optional)**  
   - For large development cycles, specs may be reviewed and synchronized at major milestones or version releases.  
   - During these reviews, the LLM or maintainer should verify that each `_SPECS/*.md` file reflects the latest code state.  

---

## Logs  

The `_LOGS` folder provides a **chronological record** of all software updates and documentation changes.  

- Each file is named using the format:  `YYY-MM-DD-short-[summary-for-the-day].md`