# 🕸️ Stringing & Oozing Fix Guide — FoxMakers

> Stop those annoying hair-thin strings between parts. Retraction tuning, temperature calibration, and slicer tricks.

## What Causes Stringing?

Stringing happens when molten plastic oozes from the nozzle while **traveling** (moving without extruding). Main causes:
1. **Retraction too low** — not enough filament pulled back
2. **Temperature too high** — plastic too runny to hold
3. **Travel speed too slow** — nozzle lingers at positions
4. **Wet filament** — moisture makes plastic more fluid

---

## Quick Fix Checklist

| Setting | Start Here | Direction if Stringing |
|---------|-----------|------------------------|
| Retraction distance | 1mm (direct) / 4mm (bowden) | ↑ increase |
| Retraction speed | 25 mm/s | ↑ increase |
| Print temperature | -5°C from default | ↓ decrease |
| Travel speed | 150 mm/s | ↑ increase |
| Combing | On (all / infill) | Enable |
| Z-hop | 0.2mm | Enable |

---

## Retraction Tuning (Step by Step)

### 1. Print the Retraction Test Tower
Download from: [Thingiverse #2563897](https://www.thingiverse.com/thing:2563897)

### 2. Start values
| Printer type | Start retraction |
|-------------|-----------------|
| Bambu Lab (AMS) | 0.8mm |
| Prusa (direct) | 1.0–1.5mm |
| Creality Ender (Bowden) | 4.5mm |
| Creality K1/K2 (direct) | 1.0mm |
| Voron 2.4 (direct) | 0.5mm |

### 3. Tune in 0.2mm increments
- Too much retraction → **gaps, blobs, grinding**
- Too little → **strings**

---

## Temperature Tower

Print a **temperature tower** (5°C steps) to find the sweet spot:
- Lower temp = less stringing BUT less layer adhesion
- Higher temp = better adhesion BUT more stringing

**Recommended ranges for minimal stringing:**
| Material | No-String Zone |
|----------|----------------|
| PLA | 195–210°C |
| PETG | 225–235°C |
| ABS | 240–250°C |
| TPU | 220–230°C |

---

## Slicer Settings (Bambu Studio)

```
Filament → Retraction → Length: 0.8mm
Filament → Retraction → Speed: 30mm/s
Quality → Avoid crossing wall: ON
Quality → Max detour length: 5mm
Speed → Travel: 200mm/s
```

## Slicer Settings (PrusaSlicer)

```
Printer Settings → Extruder 1 → Retraction → Length: 1.0mm
Print Settings → Speed → Travel: 150mm/s
Print Settings → Travel → Avoid crossing perimeters: ON
```

---

## 🛠️ Still having issues? Fix the STL

Sometimes stringing is caused by non-manifold geometry — invisible holes that confuse the slicer:  
👉 **[Free STL Repair Tool](https://hub.foxmakers.it/en/tools/stl-repair)**

---

*Guide by [FoxMakers Network](https://www.foxmakers.it) | [Free CAD Tools](https://hub.foxmakers.it/en/tools)*