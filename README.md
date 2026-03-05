# FOSSkiff: Open-Source Eurorack Skiff Case

## Overview

FOSSkiff is a free and open-source (FOSS) CAD design for a modular Eurorack skiff case made primarily from laser-cut sheet metal (aluminum or steel). It eliminates traditional extruded aluminum rails by using nut strips and integrated structural bends for rigidity. The design supports 184HP in a 3U format (with 1U and 4U variants planned), internal power supply, conditioning, and expansion capabilities. Total build cost is approximately $150 using commodity parts and services like SendCutSend for fabrication.

This repo contains CAD files (DXF for sheet metal parts, STL for 3D-printable endcaps, etc.) for fabrication. The design is modular, allowing daisy-chaining of additional "satellite" units for expansion.

Inspired by re-examining Eurorack standards, this case prioritizes affordability, lightness, and simplicity while maintaining compatibility with standard modules.

## Features

- **Rail-less Design**: Uses nut strips for module mounting, reducing cost and complexity.
- **Capacity**: 184HP per unit (3U standard; 1U and 4U TBD).
- **Power System**:
  - Internal Mean Well RT-65B power supply.
  - Power conditioning with fuses, inductors for ripple reduction.
  - USB peripheral charging/power.
- **Compatibility**: Works with any bus board (e.g., Synthrotek filtered bus board; customizable plexiglass mounting plate).
- **Lighting**: Internal RGB LED strips for illumination.
- **Modularity**: Daisy-chain multiple units (up to 3-4 depending on power draw) via 8-pin marine connectors.
- **Materials**: Sheet metal body (cheaper and lighter than wood), optional wood or 3D-printed endcaps.
- **Rigidity**: Structural bends and standoffs prevent deflection under cable pressure.
- **Cost-Effective**: No expensive rails; total ~$150 including fabrication.

## Bill of Materials (BOM)

### Sheet Metal Parts (Laser-Cut)
- Main chassis (from DXF files in `/cad/sheet_metal/`)
- Face panel with slots
- Nut strips (or use off-the-shelf; threading holes optional but increases cost)
- Plexiglass bus board mounting plate (laser-cut acrylic)

Fabricate via services like SendCutSend. Material: 16-gauge aluminum or steel. Cost: ~$40-60 for core parts.

### Hardware
- Mean Well RT-65B power supply (internal mounting).
- Bus board (e.g., Synthrotek filtered or equivalent).
- Inductors and plugs for power conditioning (from AliExpress or similar).
- Fuses for safety.
- Standoffs (M3/M4 for modules, larger for face tensioning).
- Bolts: M5 or M6 for endcaps/face attachment.
- Nuts and screws for assembly.
- 8-pin marine connector for expansion (optional).
- USB power module.
- RGB LED strip + Arduino controller for lighting.
- Endcaps: Wood (e.g., bloodwood) or 3D-printed PLA/ABS. One one endcap is provided, if you need help here don't reach out.

### Tools Needed
- Screwdriver/bit driver.
- Sandpaper (800 grit for prep).
- Paint supplies (self-etching primer, gloss black enamel, 2K automotive clear coat).
- 3D printer (if not using wood endcaps).

## Fabrication Instructions

1. **Download CAD Files**:
   - Sheet metal: Use DXF files for laser cutting.
   - 3D parts: STL files for printing endcaps if desired.
   - Customize bus board holes in plexiglass DXF if using a different board.

2. **Order Sheet Metal**:
   - Upload DXF to a service like SendCutSend.
   - Specify material: Aluminum for lightness, steel for durability.
   - Avoid integrated threading on nut strips to keep costs low (~$40 vs. $300).
   - Order plexiglass plate separately (acrylic sheet, laser-cut).

3. **3D Print or Mill Endcaps**:
   - Print STL files for temporary/prototype endcaps.
   - For premium look, mill from hardwood (e.g., bloodwood) using provided outlines.

4. **Surface Preparation and Painting**:
   - Sand parts with 800 grit sandpaper.
   - Apply self-etching primer.
   - Paint with high-gloss black enamel.
   - Finish with 2K automotive high-gloss clear coat.
   - Allow 24+ hours to dry.

## Assembly Instructions

1. **Prepare the Chassis**:
   - Insert the face panel into the chassis slots.
   - Secure with M5/M6 bolts.

2. **Install Endcaps**:
   - Attach wood or 3D-printed endcaps to the sides using bolts.
   - Ensure alignment for stability.

3. **Mount Nut Strips**:
   - Place nut strips behind the face slots.
   - Secure with standoffs (screw modules into standoffs later).
   - Add 3 holes along top/bottom for backstops (standoffs) to tension the face and prevent deflection.

4. **Install Power System**:
   - Screw Mean Well RT-65B directly into the chassis.
   - Mount power conditioner board on standoffs.
   - Connect inductors, fuses, and plugs for ripple conditioning.
   - Wire USB power module.
   - Install 8-pin marine connector for future expansions (leave unconnected if single unit).

5. **Mount Bus Board**:
   - Attach bus board to plexiglass plate.
   - Mount plate inside chassis for insulation and positioning.

6. **Add Lighting**:
   - Install RGB LED strip inside the case (behind face for shine-through).
   - Wire to Arduino controller.
   - Power from internal supply.
   - Note: while cool, I found that not much light at all actually gets through. Its only observable in very dark environments. I'm planning a module to address this, but I have newborn twins and very little free time.

7. **Install Modules**:
   - Slide modules into slots.
   - Screw into standoffs/nut strips.
   - Connect to bus board.

8. **Final Checks**:
   - Verify power output and ripple (use multimeter).
   - Test for shorts/fuses.
   - Daisy-chain if expanding (connect power/data via marine connector).

## Expansion

For additional units:
- Fabricate "satellite" chassis (simplified, no PSU).
- Connect via 8-pin marine connector for power and data sharing.
- Limit to 3-4 units based on total power draw.

## License

This project is released under Copyleft  (or your preferred FOSS license). See `LICENSE` file for details (there is not one).
## Credits

Design by @puhcko. Thanks to SendCutSend for fabrication inspiration (not sponsored).

For questions or contributions, open an issue or PR on GitHub.*
