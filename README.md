# ArchFeasibility

Early-stage architectural feasibility tool built with **C#**, **RhinoCommon** and **Grasshopper**.

The tool helps architects check, in the first design stage, whether a space program fits inside the planning constraints of a site.

## Workflow

Site → Setbacks → Buildable Envelope → Coverage → FAR → Max GFA → Space Program → Feasibility Report

## Current prototype (Grasshopper C# Script components)

| Component | Inputs | Outputs |
|---|---|---|
| Site Analysis | length, width, FAR, coverage, floors, envelope area | site area, max GFA, max footprint, area per floor, fits (true/false) |
| Buildable Envelope | length, width, front / rear / side setbacks | site curve, buildable curve, buildable area |
| Space Program | room names, counts, unit areas | total required area, space schedule |
| Feasibility Report | max GFA, required area | remaining area, GFA usage %, report |

## Example

Site 30 x 40 m, FAR 2, coverage 60%:

- Site area: 1200 m2
- Max GFA: 2400 m2
- Max footprint: 720 m2
- Required program: 300 m2 -> remaining 2100 m2 (12.5% used)

## Tech

C# | RhinoCommon | Grasshopper | Rhino 8

## Roadmap

- [x] Grasshopper C# prototype
- [ ] Convert to a real Grasshopper plugin (.gha) with Visual Studio
- [ ] Custom icons and component documentation
- [ ] Screenshots and demo video
