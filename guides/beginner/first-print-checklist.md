# ✅ First Print Checklist — FoxMakers

> Run through this checklist before every new print, especially with a new filament or printer.

## 🔴 Before Starting the Print

- [ ] **Bed leveled** — paper test or ABL mesh updated
- [ ] **Nozzle clean** — no old filament hanging, do a cold pull if needed
- [ ] **Filament dry** — if stored >3 days after opening, dry at 50°C for 4-6h (PLA) / 65°C (PETG/ABS)
- [ ] **STL repaired** — run through [FoxMakers STL Repair](https://hub.foxmakers.it/en/tools/stl-repair) if mesh errors found
- [ ] **Slicer profile correct** — right printer, nozzle diameter, material
- [ ] **Bed surface clean** — IPA wipe, no fingerprints
- [ ] **Z offset calibrated** — 0.1-0.2mm gap (paper test)
- [ ] **First layer preview** checked in slicer

## 🟡 First Layer (Watch the first 5 minutes!)

| What you see | What it means | Fix |
|---|---|---|
| Lines not sticking, lifting at edges | Z too high | Lower Z offset |
| Lines merging, over-squished | Z too low | Raise Z offset |
| Gaps between lines | Under-extrusion or Z too high | Check extrusion/Z |
| Blobs at start | Ooze during heating | Add prime tower or wipe |
| Good adhesion, slight sheen | ✅ Perfect | Do nothing! |

## 🟢 Mid-Print Checks (10-15 min in)

- [ ] No spaghetti / layer shifts
- [ ] Walls looking solid
- [ ] Infill connecting properly
- [ ] Fan running (for PLA)
- [ ] No grinding sound from extruder (= clog forming)

## 🔵 After Print

- [ ] Wait for bed to cool below 35°C before removing (reduces warping)
- [ ] Store filament in zip bag with desiccant
- [ ] Clean bed surface with IPA
- [ ] Inspect part for layer adhesion, warping, stringing

---

## 🛠️ Common Issues Quick Fix

| Problem | Cause | Solution |
|---------|-------|----------|
| Print detaches mid-print | Bed too cold / dirty | +5°C bed, IPA clean |
| Elephant foot | Z too close | Raise Z 0.1mm |
| Stringing | Temp too high / bad retraction | -5°C, tune retraction |
| Layer splitting | Temp too low / speed too high | +5°C, -20% speed |
| Clog | Bad filament / too fast | Cold pull, reduce speed |

---

## 🔧 Free Tools

- Repair broken STL: [hub.foxmakers.it/en/tools/stl-repair](https://hub.foxmakers.it/en/tools/stl-repair)
- Convert STL to STEP: [hub.foxmakers.it/en/tools/stl-to-step](https://hub.foxmakers.it/en/tools/stl-to-step)
- Design parametric parts: [hub.foxmakers.it/en/tools](https://hub.foxmakers.it/en/tools)

*By [FoxMakers Network](https://www.foxmakers.it) | CC BY 4.0*