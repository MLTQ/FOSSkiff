# FOSSkiff: Open-Source Eurorack Skiff Case
<img width="2048" height="1536" alt="image" src="https://github.com/user-attachments/assets/b3cf7fbb-44ad-440d-8e2b-cae64d6ac962" />

## Overview

FOSSkiff is a free and open-source (FOSS) CAD design for a modular Eurorack skiff case made primarily from laser-cut sheet metal (aluminum or steel). It eliminates traditional extruded aluminum rails by using nut strips and integrated structural bends for rigidity. The design supports 184HP in a 3U format (with 1U and 4U variants planned), internal power supply, conditioning, and expansion capabilities. Total build cost is approximately $150 using commodity parts and services like SendCutSend for fabrication.

This repo contains CAD files (STEP) for fabrication. The design is modular, allowing daisy-chaining of additional "satellite" units for expansion.

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

### Laser Cut Parts
- Main chassis (Steel or aluminum)
- Face panel with slots (Steel or aluminum)
- Plexiglass bus board mounting plate (laser-cut acrylic)

Fabricate via services like SendCutSend. Material: 16-gauge aluminum or steel. Cost: ~$40-60 for core parts. Their online reviewer will give you grief about bending offsets, just ignore those- there are some signs of minor stress but the paint convers them up quite well.

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
<img width="1290" height="1632" alt="image" src="https://github.com/user-attachments/assets/855319af-913e-4203-91de-5d692db88610" />

### Tools Needed
- Screwdriver/bit driver.
- Sandpaper (800 grit for prep).
- Paint supplies (self-etching primer, gloss black enamel, 2K automotive clear coat).
- 3D printer (if not using wood endcaps).

## Fabrication Instructions

1. **Download CAD Files**:
   - You gotta do it to do it

2. **Order Sheet Metal**:
   - Upload STEP to a service like SendCutSend.
   - Specify material: Aluminum for lightness, steel for durability.
   - Avoid integrated threading on nut strips to keep costs low (~$40 vs. $300).
   - Order plexiglass plate separately (acrylic sheet, laser-cut).

3. **3D Print or Mill Endcaps**:
   - Print endcap files for temporary/prototype endcaps.
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
<img width="1536" height="2048" alt="image" src="https://github.com/user-attachments/assets/c0ee0a1f-a8bc-4bc0-b95c-36a96dfec723" />

4. **Install Power System**:
   - Screw Mean Well RT-65B directly into the chassis.
   - Mount power conditioner board on standoffs.
   - Connect inductors, fuses, and plugs for ripple conditioning.
   - Wire USB power module.
   - Install 8-pin marine connector for future expansions (leave unconnected if single unit).
<img width="2048" height="1536" alt="image" src="https://github.com/user-attachments/assets/4dec2ca3-825c-4659-81e6-14c5d085b11c" />

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
<img width="1536" height="2048" alt="image" src="https://github.com/user-attachments/assets/e0f99562-bac1-4a00-9f2f-84c3c7e7b872" />

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

This project is released under MIT License.

For questions or contributions, open an issue or PR on GitHub.*
