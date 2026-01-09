# NZS 7000 Conductor Blowout Calculator

**Version 2.0.0** | [Live Demo](https://merrimac54.github.io/nzs7000-blowout-calculator/)

A free community screening tool for in-fill property developers to calculate conductor blowout compliance using AS/NZS 7000:2016 Appendix Q methodology.

## What's New in v2.0.0

### Inclined Span Support

When power line poles are at significantly different heights (common in hilly terrain), the simple "drop below pole" measurement from a survey does **not** represent true sag. This can lead to underestimating blowout by a factor of 4× or more.

Version 2.0 adds:

- **Inclined Span Mode** toggle for poles at different heights
- **True sag calculation** from the chord line (imaginary straight line between poles)
- **Automatic correction** when you enter pole height difference
- **Side-by-side comparison** of level vs inclined span results

### Why This Matters

For a span with poles 4.36m apart in height:
- Survey measurement near lower pole: **0.22m** (drop below pole)
- True sag at that point: **~0.93m** (from chord line)
- This changes mid-span sag from 0.4m to **1.7m**
- And mid-span blowout from 356mm to **1,670mm**

## Features

- **AS/NZS 7000:2016** Appendix Q3 methodology
- **NZECP34:2001** Table 3 clearance requirements for all voltage levels
- **Building position vs mid-span** comparison
- **Wind speed sensitivity** analysis (90–142 km/h)
- **Common conductor library** with click-to-apply
- **Real-time calculations** as you type
- **Print-friendly** styling

## How to Use

### Basic (Level Span)

1. Select your conductor type or enter custom values
2. Enter span length (distance between poles)
3. Enter measured sag at building position
4. Enter position from nearest pole
5. Enter horizontal distance to building
6. Select conductor classification for NZECP34 clearance

### Inclined Span (Poles at Different Heights)

1. Complete basic inputs as above
2. Toggle **ON** "Inclined Span Mode"
3. Enter **Pole Height Difference** (higher pole RL minus lower pole RL)
4. Select whether building is near the **Lower Pole** or **Higher Pole**
5. The calculator will automatically correct for true sag

## Understanding the Results

| Colour | Meaning |
|--------|---------|
| 🟢 Green | Results at BUILDING position |
| 🔵 Blue | Results at MID-SPAN (worst case) |
| 🔷 Cyan | Inclined span corrected values |

## Technical Background

### Level Span Formula

For a level span, sag at any position x from the pole:

```
S(x) = S_mid × 4 × x × (L-x) / L²
```

### Inclined Span Correction

When poles are at different heights, the survey "drop below pole" must be converted to true sag:

```
True sag at position x = Chord height at x + Survey drop

Where chord height at x = (h/L) × x
      h = pole height difference
      L = span length
```

### Blowout Calculation (AS/NZS 7000 Appendix Q3)

```
Blowout angle: φ = tan⁻¹(P × d / w)
Lateral displacement: d₁ = S × sin(φ)
Vertical rise: d₂ = S × (1 - cos(φ))
```

Where:
- P = wind pressure (Pa)
- d = conductor diameter (m)
- w = conductor weight (N/m)
- S = sag at the point of interest (m)

## Standards Referenced

- **AS/NZS 7000:2016** — Overhead Line Design
- **NZECP34:2001** — NZ Electrical Code of Practice for Electrical Safe Distances

## Disclaimer

⚠️ **This tool is for preliminary screening only.**

Always obtain professional engineering verification for consent applications. The author accepts no liability for decisions made based on this calculator.

## Licence

MIT Licence — free to use, modify, and distribute.

## Author

Kirsty Merriman  
[kirstymerriman.com](https://kirstymerriman.com)

## Changelog

### v2.0.0 (2026-01-09)
- Added Inclined Span Mode for poles at different heights
- Added warning banner explaining level vs inclined span differences
- Added true sag calculation from chord line
- Added comparison between level and inclined span results
- Added pole height difference and measurement location inputs
- Updated default values for typical site conditions

### v1.0.0 (2025-12-XX)
- Initial release
- Level span calculations based on AS/NZS 7000:2016 Appendix Q3
- NZECP34 Table 3 clearance requirements
- Wind speed sensitivity analysis
- Building position vs mid-span comparison
