# NZS 7000 Conductor Blowout Calculator

A free community screening tool for in-fill property developers to calculate conductor blowout compliance using the AS/NZS 7000:2016 Appendix Q methodology.

**[🚀 Launch Calculator](https://yourusername.github.io/nzs7000-blowout-calculator/)** *(update this link after setup)*

## About

When building near overhead power lines, New Zealand regulations require minimum safe distances between conductors and buildings. This calculator helps property developers screen whether their proposed building position is likely to comply with:

- **AS/NZS 7000:2016** — Overhead line design standard (Appendix Q blowout methodology)
- **NZECP34:2001** — New Zealand Electrical Code of Practice for Electrical Safe Distances (Table 3)

The tool compares conductor blowout at your specific building position versus the theoretical worst-case mid-span position, giving you a more accurate assessment than using conservative mid-span assumptions.

## Features

- ✅ Full AS/NZS 7000:2016 Appendix Q blowout calculations
- ✅ Building position vs mid-span comparison
- ✅ Complete NZECP34 Table 3 clearance requirements for all voltage levels (sub-1kV through to 220kV+)
- ✅ Bare, covered, and insulated conductor classifications
- ✅ Wind speed analysis (90 km/h to 142 km/h Vector requirement)
- ✅ Common conductor reference data
- ✅ Mobile-responsive design
- ✅ Works entirely in your browser — no data sent anywhere

## How to Use

1. Enter your conductor properties (or select from common types)
2. Enter the span geometry (length, sag, position from pole)
3. Enter the building proximity (horizontal distance, height above building)
4. Select the correct NZECP34 voltage level and conductor classification
5. Review the compliance results

## Important Disclaimer

⚠️ **This is a screening tool only.** 

- Results should be verified by a qualified electrical engineer
- Always obtain professional engineering assessment for consent applications
- This tool does not replace Vector or other lines company close approach consent processes
- The developer accepts no liability for decisions made based on these calculations

## Technical Basis

### Blowout Calculations (AS/NZS 7000:2016 Appendix Q)

- **Mid-span sag**: `S_mid = S(x) × L² / (4 × x × (L−x))`
- **Blowout angle**: `φ = tan⁻¹(P × d / w)`
- **Lateral displacement**: `d₁ = S × sin(φ)`
- **Vertical rise**: `d₂ = S × (1 − cos(φ))`

Where:
- `S(x)` = measured sag at position x
- `L` = span length
- `P` = wind pressure (Pa)
- `d` = conductor diameter (m)
- `w` = conductor weight (N/m)

### NZECP34 Clearances

The calculator uses NZECP34:2001 Table 3, Column C clearances (distance in any direction from normally accessible parts) which apply when specific engineering calculation of conductor movement has been carried out.

## Contributing

Contributions are welcome! This is a community tool and improvements benefit everyone.

### Ways to Contribute

- **Report bugs** — Use the [Issues](../../issues) tab
- **Suggest features** — Open an issue describing the enhancement
- **Submit code** — Fork the repository, make changes, and submit a pull request
- **Improve documentation** — Help make the tool more accessible

### Development

The calculator is a single HTML file using React (loaded from CDN). To modify:

1. Fork this repository
2. Edit `index.html`
3. Test locally by opening the file in your browser
4. Submit a pull request

## Licence

This project is licensed under the MIT Licence — see the [LICENSE](LICENSE) file for details.

You are free to use, modify, and distribute this tool for any purpose, including commercial use.

## Credits

- **Original development**: Kirsty Merriman ([kirstymerriman.com](https://kirstymerriman.com))
- **Purpose**: Supporting New Zealand in-fill property developers and construction professionals
- **Standards**: Based on AS/NZS 7000:2016 and NZECP34:2001

## Related Resources

- [NZECP34:2001 — Electrical Safe Distances](https://www.worksafe.govt.nz/laws-and-regulations/electrical-and-gas-codes-of-practice/electricity-codes-of-practice/)
- [AS/NZS 7000:2016 — Overhead Line Design](https://www.standards.govt.nz/)
- [Vector Close Approach Consents](https://www.vector.co.nz/)

---

*Made with ❤️ for the New Zealand property development community*
