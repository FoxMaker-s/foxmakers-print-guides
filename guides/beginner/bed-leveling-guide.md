# 🔧 Bed Leveling Complete Guide — FoxMakers

> Every method explained: manual, CR Touch, BLTouch, PINDA, Beacon, Bambu ABL

## Why Bed Leveling Matters

The first layer is the foundation of every print. A poorly leveled bed causes:
- Warping and detachment mid-print
- Elephant foot (too close)
- Poor adhesion / spaghetti (too far)
- Inconsistent layer width

**Rule of thumb:** nozzle should be 0.1–0.2mm from bed (the thickness of a sheet of paper).

---

## Method 1: Manual Leveling (all printers)

### Tools needed
- A sheet of regular A4 paper (0.1mm thick)
- Patience

### Steps
1. Home all axes (`G28`)
2. Disable steppers or use the printer's "move" menu
3. Move nozzle to **front-left** corner
4. Slide paper under nozzle — adjust corner knob until you feel **slight resistance**
5. Repeat for **front-right**, **back-right**, **back-left**, **center**
6. Do 2-3 passes until all corners feel the same

### Tips
- Do this with the bed at printing temperature (thermal expansion matters!)
- PLA: bed 60°C, ABS: bed 110°C
- Always re-level after moving the printer

---

## Method 2: Automatic Bed Leveling (ABL) — CR Touch / BLTouch

### Setup in Cura
```
G28 ; Home
G29 ; Run ABL probe
M500 ; Save to EEPROM
```

### Offset calibration
Run `M851 Z-X.XX` to set Z offset. Start conservative (less negative = further from bed).

**Live Adjust Z during first layer:**
- Too far: increase `|Z offset|` (more negative)
- Too close: decrease `|Z offset|` (less negative)

---

## Method 3: Bambu Lab Auto-Calibration

Bambu printers (X1C, P1S, A1 mini, H2D) use **Lidar + vibration sensing**:

1. Start a print — calibration runs automatically
2. If first layer is bad:
   - `Settings → Calibration → First Layer Inspection`
   - Adjust `Z offset` in 0.05mm steps
3. For persistent issues: `Settings → Calibration → Full Calibration`

**Common Bambu first layer problems:**
| Problem | Fix |
|---------|-----|
| Gaps between lines | Z offset too high → more negative |
| Lines merging/squishing | Z offset too low → less negative |
| Curling edges | Bed temp too low or fan speed too high |

---

## Method 4: Prusa PINDA/SuperPINDA (MK3S+, MK4S)

PINDA is a temperature-sensitive inductive sensor:
1. Home → Mesh Bed Leveling runs automatically before every print
2. For fine-tuning: `LCD → Calibration → Live Adjust Z`
3. Run `First Layer Calibration` from menu after any major change

**SuperPINDA** (MK4S, XL): temperature-compensated, more accurate.

---

## Method 5: Beacon / Cartographer (Klipper)

Beacon uses **eddy current sensing** at 10kHz — sub-micron resolution.

```ini
[beacon]
serial: /dev/serial/by-id/usb-Beacon_...
x_offset: -20
y_offset: 0
mesh_runs: 2
```

After homing: `BEACON_AUTO_CALIBRATE` for first time setup.

---

## 🛠️ Fix STL Before Printing

A non-manifold STL will cause slicer errors regardless of bed level:  
👉 **[Free STL Repair Tool](https://hub.foxmakers.it/en/tools/stl-repair)** — browser-based, no install

---

## 🌍 FoxMakers Network

European distributed 3D printing | Free CAD tools  
🔗 [www.foxmakers.it](https://www.foxmakers.it) | [hub.foxmakers.it](https://hub.foxmakers.it)