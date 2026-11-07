# 🖨️ 3D Printing: Getting Started

![Level: Beginner to intermediate](https://img.shields.io/badge/Level-Beginner%20to%20Intermediate-2ea44f)
![Covers: FDM and resin](https://img.shields.io/badge/Covers-FDM%20%7C%20Resin-f57c00)
![Slicers: Cura, PrusaSlicer, OrcaSlicer, Bambu Studio](https://img.shields.io/badge/Slicers-Cura%20%7C%20PrusaSlicer%20%7C%20OrcaSlicer%20%7C%20Bambu%20Studio-5c2d91)
[![Last updated](https://img.shields.io/github/last-commit/ImmuneMoon/3D-Printing-Getting-Started?label=updated)](https://github.com/ImmuneMoon/3D-Printing-Getting-Started/commits/main)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey)](LICENSE)

**📄 [Download the PDF](3D-Printing-Getting-Started.pdf)**

## 📖 Overview
**3D Printing: Getting Started** takes you from "what is a 3D printer?" to confidently printing, tuning and fixing your own parts. It covers:
- how FDM (filament) and resin printers work, and the parts of an FDM printer;
- what to look for in a first printer, as criteria rather than brand endorsements;
- safety in depth: fumes and particles, burns, fire, and handling and disposing of resin;
- filament types (PLA, PETG, TPU, ABS and ASA), and storing and drying them;
- free slicers, file formats (STL and 3MF), and what the main slicer settings do;
- your first week: leveling, the Z offset, and calibration prints;
- finding models and respecting their licenses, and designing your own;
- post-processing, maintenance, and a troubleshooting table for common first-print problems;
- time-lapses, research that hints at what's next, and robotics and animatronics as a place this hobby can lead.

## ⚠️ Important Disclaimer
3D printers have hot parts, moving parts and mains power, and printing releases particles and fumes. Resin printers add chemicals that can irritate skin and cause allergies. Read **Section 4** before your first print, follow your printer's manual, and read the Safety Data Sheet (SDS) for every resin and solvent you use. Supervise children. Settings in this guide are starting points: your printer's and filament maker's recommendations come first.

## 🚀 How to Use
Download the PDF above, or read on below. New to 3D printing? Read **Sections 1 to 4** before you buy anything. Once your printer arrives, work through **Section 8** in your first week, and use **Section 16** whenever a print goes wrong.

This guide works alongside these others:
* [Learn 3D Modeling](https://github.com/ImmuneMoon/Learn-3D-Modeling) - Designing your own models in depth, beyond the short introduction in Section 10.
* [Batch Image and 3D Tools: GIMP, Blender and Pillow](https://github.com/ImmuneMoon/Batch-Image-and-3D-Tools-GIMP-Blender-Pillow) - Running Blender from scripts, for example to process many models at once.
* [Learn Game Development](https://github.com/ImmuneMoon/Learn-Game-Development) - If you'd like to turn your 3D models into game assets.

---

<!-- guide:start -->

## Contents

1. [How 3D Printing Works](#1-how-3d-printing-works)
2. [The Parts of an FDM Printer](#2-the-parts-of-an-fdm-printer)
3. [Choosing a First Printer](#3-choosing-a-first-printer)
4. [Safety](#4-safety)
5. [Filament Types, Storage and Drying](#5-filament-types-storage-and-drying)
6. [Slicers and File Formats](#6-slicers-and-file-formats)
7. [Slicer Settings Explained](#7-slicer-settings-explained)
8. [Your First Week: Setup and Calibration](#8-your-first-week-setup-and-calibration)
9. [Finding Models, and Licenses](#9-finding-models-and-licenses)
10. [Designing Your Own Models](#10-designing-your-own-models)
11. [Post-Processing](#11-post-processing)
12. [Maintenance](#12-maintenance)
13. [Time-Lapses and Inspiration](#13-time-lapses-and-inspiration)
14. [A First-Projects Ladder](#14-a-first-projects-ladder)
15. [Communities and Channels](#15-communities-and-channels)
16. [Troubleshooting](#16-troubleshooting)
17. [Sources](#17-sources)

---

## 1. How 3D Printing Works

Every 3D print starts the same way:

1. **Get a 3D model**, by downloading one or designing your own (Sections 9 and 10).
2. **Slice it.** A program called a **slicer** cuts the model into thin layers and works out the path the printer follows for each one (Section 6).
3. **Print it,** one layer on top of the last.
4. **Finish it:** remove supports, and clean, sand or paint it if you like (Section 11).

The two kinds of home printer build those layers in very different ways:

| | FDM (filament) | Resin (MSLA, also called LCD or SLA) |
|---|---|---|
| **How it works** | Melts a plastic strand (**filament**) in a hot nozzle and draws each layer, like a very precise hot-glue gun | A screen shines UV light through a vat of liquid **photopolymer resin**, hardening one whole layer at a time |
| **Best for** | Functional parts, brackets, enclosures, large objects, everyday prints | Very fine detail: miniatures, jewelry models, small figures |
| **Surface** | Visible layer lines | Very smooth, with tiny layer lines |
| **Mess and handling** | Low. Parts come off ready to use. | High. Parts must be washed in a solvent and cured under UV light, and liquid resin needs gloves and careful disposal. |
| **Safety focus** | Heat, fumes and particles, fire | Skin and eye contact with resin, solvent fumes and fire risk, chemical waste |
| **Recommended for a first printer?** | **Yes, for most people** | If you mainly want detailed miniatures and are ready for the safety routine |

FDM is also called FFF (fused filament fabrication). This guide focuses on FDM, with resin safety and post-processing covered too.

---

## 2. The Parts of an FDM Printer

Knowing the parts makes the manual, the settings and the troubleshooting much easier to follow.

| Part | What it does |
|---|---|
| **Frame** | Holds everything square and rigid. A wobbly frame means wobbly prints. |
| **Spool holder** (and sometimes a **runout sensor**) | Holds the filament and, with a sensor, pauses the print if it runs out |
| **Extruder** | Motor-driven gears that grip the filament and push it into the hotend |
| **Hotend** | Melts the filament. It includes the **heater**, a **thermistor** (temperature sensor), the **heat break**, a **heatsink** with its fan, and the **nozzle** (usually 0.4 mm) |
| **Part cooling fan** | Blows on the freshly printed plastic so it sets quickly, which helps overhangs and bridges |
| **Build plate (bed)** | The surface you print on. Most are heated, with a removable flexible sheet, often PEI-coated, so parts pop off when you flex it. |
| **Motion system** | Stepper motors move the nozzle and bed using **belts** (X and Y) and **lead screws** or belts (Z). Common layouts are the "bed slinger", where the bed moves back and forth, and **CoreXY**, where the toolhead moves in X and Y and the bed only moves down. |
| **Probe** | Measures the bed's height at many points for automatic bed leveling (Section 3) |
| **Mainboard and firmware** | The electronics and software that run the motors and heaters, and include safety checks such as thermal runaway protection (Section 4.2) |
| **Screen and connectivity** | Controls on the printer, and often USB, an SD card, Wi-Fi or a camera |

---

## 3. Choosing a First Printer

Models change every few months, so this section gives you the questions to ask rather than a shopping list. Read recent reviews from several sources, and check the manufacturer's own documentation and support pages before you buy.

| Feature | What it means | What to look for as a beginner |
|---|---|---|
| **Automatic bed leveling (ABL)** | A probe measures the bed's surface and the printer compensates for small dips and tilts | Strongly recommended. It removes the most common first-print headache. You may still need to set the **Z offset** (Section 8). |
| **Direct drive or Bowden extruder** | **Direct drive** puts the extruder motor on the toolhead, right above the hotend. **Bowden** keeps it on the frame and pushes filament through a long tube. | Direct drive handles flexible filaments like TPU far better and needs less retraction. Bowden keeps the toolhead lighter. Most current printers use direct drive. |
| **Enclosure** | A closed cabinet around the print area, sometimes with a filter and fan | Needed to print ABS and ASA well. It also keeps fingers, pets and dust out. An enclosure with filtered extraction can reduce what reaches the room (Section 4.1). |
| **Multi-material or multi-color** | Add-on units or toolchangers that switch between several filaments | Fun, but it adds cost, complexity and, on many systems, waste from purging old color. Not needed for your first prints. |
| **Build volume** | The largest object it can print | Around 200 to 250 mm in each direction covers most hobby projects. Bigger printers cost more and take more space. |
| **Speed** | How fast it can move while keeping quality | Modern printers are much faster than older ones, but every printer's quality drops if pushed too hard. Don't choose on headline speed alone. |
| **Assembled or kit** | Ready to use, or built by you | A kit teaches you how the machine works. Pre-assembled gets you printing sooner. |
| **Software and ecosystem** | Which slicers work with it, and whether it needs a cloud account or app | Check it can print offline (USB, SD card or local network) and works with a free slicer you like (Section 6). |
| **Parts and support** | Spare nozzles, hotends, belts and sheets, plus documentation | Look for easy-to-buy spares, good written guides and an active community. |
| **Safety certification** | Testing by an independent lab | NIOSH suggests choosing printers approved by a Nationally Recognized Testing Laboratory (in the US, marks such as UL, ETL or CSA). |
| **Camera and remote monitoring** | Watch prints from your phone or PC | Handy for spotting failures, and useful for time-lapses (Section 13). |

> **Resin printer?** Also check the build plate size, the light source, how easy the vat film is to replace, whether a wash-and-cure station is available, and whether you have a well-ventilated space away from living and eating areas.

---

## 4. Safety

These recommendations come mainly from NIOSH's guide **"Approaches to Safe 3D Printing"** (US National Institute for Occupational Safety and Health, November 2023), written for makerspaces, schools, libraries and small businesses, and from UL Research Institutes' Chemical Insights research on printer emissions. They apply at home too.

### 4.1 Fumes and particles (FDM)

Melting plastic releases **ultrafine particles** and **volatile organic compounds (VOCs)**. Research has linked these emissions to respiratory irritation, and the amount depends on the material, the color and additives, the brand, and the temperature. UL's Chemical Insights research found that ABS generally emits more particles and VOCs than PLA.

1. **Ventilate.** Print in a well-ventilated room, not a small closed bedroom, and don't sleep in the same room as a running printer.
2. **Keep your distance.** Put the printer where you don't sit right next to it for hours, and leave the room when you don't need to watch it.
3. **Use the lowest temperature that gives good results.** NIOSH recommends this, and UK research it cites found lower nozzle temperatures reduced exposure.
4. **Choose lower-emitting materials** when they'll do the job. PLA is the usual choice indoors.
5. **Use an enclosure with filtration or extraction** for ABS, ASA and long or frequent prints. In the research NIOSH cites, a filtered enclosing hood cut particle emissions by 97 to 99%. **Wait about 20 minutes** after a print finishes before opening an enclosure, as the UK research suggests.
6. **No food or drink** near the printer.
7. **Clean with a damp cloth,** not compressed air or dry sweeping, which throws particles back into the air.

### 4.2 Burns, moving parts and fire

* **Hot parts:** the nozzle runs at around 200 to 260 °C and the bed at up to about 110 °C. Let them cool before you touch them, and use a silicone nozzle sock if your printer supports one.
* **Moving parts:** tie back long hair, and keep loose clothing, cables and fingers away from belts and the moving toolhead.
* **Thermal runaway protection:** this firmware check shuts the heaters off if a temperature reading stops making sense, for example when a sensor falls out. Without it, a heater can keep heating until something catches fire. The Marlin firmware documentation is blunt: never disable thermal protection to make an error go away. Find and fix the cause instead.
* **Fire precautions:**
  1. Place the printer on a stable, non-flammable surface, with clear space around it and nothing flammable on top.
  2. Fit a working **smoke alarm** in the room.
  3. Don't leave a new printer, or one you've just repaired, printing unattended. Watch the first prints from start to finish.
  4. Keep cables in good condition, and don't overload extension cords.
  5. Store solvents such as isopropyl alcohol (IPA) away from heat and ignition sources. They're flammable.
* **Children and pets:** supervise children, and keep pets away from the printer and from resin.

### 4.3 Resin safety, in depth

Liquid resin is the biggest safety difference between resin and FDM printing. NIOSH notes that some chemicals in these resins **can cause skin irritation or sensitization**. Sensitization means you can develop an allergy through repeated contact, after which even small amounts may trigger a reaction, so avoid all skin contact from the very first print.

**Before you start**
1. **Read the SDS** (Safety Data Sheet) for your resin and your cleaning solvent. It lists hazards, protective equipment and first aid. Manufacturers publish them on their websites.
2. **Set up a dedicated, well-ventilated space,** away from where people eat, sleep and relax, and away from children and pets.
3. **Cover your work surface** with something easy to clean, such as a silicone mat or disposable paper, and keep paper towels and a bag for resin waste nearby.

**While you work**
1. **Wear nitrile (or other chemical-resistant) gloves** whenever you handle resin, uncured prints, the vat, the build plate or used solvent. NIOSH recommends nitrile or appropriate chemical-resistant gloves, and Formlabs advises gloves for liquid resin, resin-coated surfaces and solvent. Change them if they tear or get heavily coated, and take them off before touching door handles, phones or your face.
2. **Wear eye protection** (safety glasses or goggles) when pouring resin, using solvents, or removing supports, which can flick off.
3. **Keep the printer's UV cover closed** while it prints, and don't look into the curing light.
4. **If resin gets on your skin or in your eyes,** follow the first-aid steps in the SDS straight away.
5. **Keep resin away from drains,** and label any container you put it in.

**Washing and curing** are covered in Section 11.

### 4.4 Disposing of resin waste safely

This follows Formlabs' guidance on disposing of resin, and university safety offices give similar advice:
* **Liquid resin is chemical waste.** Never pour it, or solvent containing dissolved resin, down a drain or into household trash. Rules differ by area, so check with your local waste authority.
* **Cure small amounts before disposal.** Formlabs' method: wearing clean nitrile gloves, pour a small amount of leftover resin into a labeled, clear, resin-safe container, and leave it in sunlight for 1 to 10 days until it's fully hard. Cured, hardened resin can then go in household waste.
* **Paper towels, gloves and failed prints** with liquid resin on them can be cured in sunlight or under UV in the same way, then thrown away.
* **Used IPA or other solvent** with resin in it must not go down the drain or in household trash either. Disposal rules vary by area, so follow the solvent's SDS and your local hazardous waste service.
* **Cured prints and supports aren't recyclable** in normal plastic recycling.

---

## 5. Filament Types, Storage and Drying

### 5.1 The common filaments

The temperatures below are from Prusa's material guides for its own filaments. Other brands differ, so **use the range printed on your spool** as your starting point.

| Material | Typical nozzle / bed | Good for | Watch out for |
|---|---|---|---|
| **PLA** | 210 to 215 °C / 60 °C | Your first prints: models, prototypes, decorations, organizers. Easy to print, low warping, good detail. | Softens above about 60 °C, so not for hot cars or near heat. Brittle on impact. Low UV resistance. |
| **PETG** | 230 to 240 °C / 85 to 90 °C | Tougher functional parts that need more heat and chemical resistance than PLA | Strings more than PLA. Can stick **too** well to smooth PEI sheets, so Prusa recommends glue stick as a release layer. |
| **TPU** (flexible) | 230 to 245 °C / 60 to 75 °C | Flexible parts: bumpers, phone cases, gaskets, feet | Print slowly (Prusa suggests about 20 mm/s). Much easier on a direct drive printer. Absorbs moisture. |
| **ABS** | About 255 °C / about 100 °C | Heat-resistant, tough parts | Warps significantly. Emits more particles and fumes than PLA, so needs an enclosure and good ventilation. |
| **ASA** | About 260 °C / 105 to 110 °C | Like ABS, with better UV resistance, so it suits outdoor parts | Warps significantly. Needs an enclosure and ventilation, like ABS. |

> **Start with PLA.** Learn your printer on the easiest material, then move to PETG when you need tougher parts. Leave ABS and ASA until you have an enclosure and good ventilation.

**Abrasive filaments** (carbon-fiber or glass-filled, glow-in-the-dark, and some metal-filled blends) wear out standard brass nozzles quickly. Use a hardened nozzle if your printer supports one.

### 5.2 Storage and drying

Many filaments absorb moisture from the air. Prusa's guide says TPU, nylon (polyamide) and PVA most often need drying, while PLA is much less affected.

**Signs of wet filament:** poor surface quality, more stringing than usual, weak layers, blobs, and popping, bubbling or steam as it extrudes.

**Storage:** keep spools you aren't using in a sealed box or bag with **desiccant** (silica gel), or in a drybox.

**Drying temperatures** from Prusa's guide, for its own filaments:

| Material | Drying |
|---|---|
| PLA | 45 °C for 6 hours |
| PETG | 55 °C for 6 hours |
| TPU | 60 °C for 4 to 6 hours |
| ASA | 80 °C for 4 hours |

Don't go hotter than recommended, or the filament softens and the spool fuses together. A dedicated filament dryer is the safest option. Prusa warns that kitchen ovens often can't hold a temperature that low accurately, so if you use one, check it with a separate thermometer, and never leave it unattended.

---

## 6. Slicers and File Formats

### 6.1 Free slicers

All four of these are free and open source. Use the one your printer maker recommends first, since it will have tested profiles for your machine.

| Slicer | Made by | License | Notes |
|---|---|---|---|
| **[UltiMaker Cura](https://ultimaker.com/software/ultimaker-cura/)** | UltiMaker | LGPL-3.0 | Long-established, with profiles for many brands of printer |
| **[PrusaSlicer](https://www.prusa3d.com/page/prusaslicer_424/)** | Prusa Research | AGPL-3.0 | Built on the earlier Slic3r. Includes profiles for many non-Prusa printers. |
| **[OrcaSlicer](https://www.orcaslicer.com/)** | Community project | AGPL-3.0 | Grew out of Bambu Studio and PrusaSlicer. Known for its built-in calibration tests (Section 8). |
| **[Bambu Studio](https://bambulab.com/en/download/studio)** | Bambu Lab | AGPL-3.0 | Made for Bambu Lab printers. Based on PrusaSlicer. |

> **⚠️ Download slicers only from official sources.** OrcaSlicer's own project page warns that fake sites, including `orca-slicer[.]com` and `orcaslicer[.]net`, pretend to be official and may offer dangerous downloads. Its only official website is **www.orcaslicer.com**, and its code lives at **github.com/OrcaSlicer/OrcaSlicer**. The same caution applies to every slicer: use the links above or the maker's GitHub page.

### 6.2 File formats

| Format | What it holds | Use it for |
|---|---|---|
| **STL** | Only the surface shape, as a mesh of triangles. No color, no materials and no units, so it's assumed to be in millimeters. | The most common download format. Every slicer opens it. |
| **3MF** | Geometry plus units, colors, materials and print settings in one file. It's an open format from the 3MF Consortium, and became an international standard (ISO/IEC 25422) in 2025. | Saving and sharing a ready-to-print project, including multi-color prints and your slicer settings |
| **OBJ** | A mesh, optionally with color or texture information | Models from 3D art programs such as Blender |
| **STEP** | Exact CAD geometry, not a triangle mesh | Exchanging designs between CAD programs. Some slicers can import it directly. |
| **G-code** | The printer's step-by-step instructions, made by the slicer | What you send to the printer. It's made for one printer and one filament, so don't reuse G-code made for a different machine. |

Exporting from Blender? It saves STL and OBJ out of the box, but needs a free extension for 3MF, and its default unit is the meter, so models can arrive in the slicer far too small. [Learn 3D Modeling](https://github.com/ImmuneMoon/Learn-3D-Modeling#14-exporting-for-3d-printing) covers setting units, checking for a watertight mesh, and the 3D Print Toolbox.

---

## 7. Slicer Settings Explained

Start from your printer maker's profile for your filament, and change **one setting at a time** so you know what made the difference.

| Setting | What it does | A sensible start |
|---|---|---|
| **Layer height** | The thickness of each layer. Thinner layers look smoother but take longer. | 0.2 mm with a 0.4 mm nozzle. Try 0.1 to 0.15 mm for detailed models, 0.28 mm for quick drafts. Keep it well under the nozzle size. |
| **Walls (perimeters)** | The number of outlines around each layer | 2 for decorations, 3 or 4 for parts that need strength. Extra walls usually add strength faster than extra infill. |
| **Top and bottom layers** | Solid layers that close off the top and bottom | Enough for about 0.8 to 1 mm of thickness, so the top doesn't show gaps |
| **Infill** | The internal pattern that fills the inside | 10 to 20% for most prints, more for parts under load. Gyroid and grid are common patterns. |
| **Supports** | Temporary structures under overhangs that would otherwise print in mid-air | Only where needed. **Tree** (organic) supports use less material and are often easier to remove. |
| **Brim** | Extra rings around the bottom of the part to help it stick | Use for small contact areas, tall thin parts, and materials that warp |
| **Raft** | A thick base printed under the whole part | Rarely needed on a modern heated bed. It wastes material and leaves a rough bottom. |
| **Skirt** | A loop around the part that doesn't touch it | Primes the nozzle and shows whether the first layer looks right |
| **Speed** | How fast the nozzle moves | Use your profile's defaults. Slow down the first layer and fine details if quality suffers. |
| **Temperature** | Nozzle and bed temperature | From the spool label, tuned with a temperature tower (Section 8) |
| **Cooling** | Part cooling fan speed | High for PLA, lower for PETG, and per your profile for ABS and ASA |
| **Retraction** | Pulls filament back slightly before travel moves to stop oozing | Use the profile. Direct drive printers typically need much shorter retraction than Bowden ones. |
| **Seam position** | Where each layer starts and ends, which leaves a small mark | Aligned or rear, to hide the seam on one side |

---

## 8. Your First Week: Setup and Calibration

Do these in order. Most printers come close to tuned from the factory, so you're checking more than fixing. Your printer's manual comes first; the steps below are general.

1. **Unbox and assemble carefully.** Remove all transport locks, cable ties and foam. Check that screws are tight, the frame is square, and belts feel firm rather than floppy.
2. **Update the firmware and slicer** using the manufacturer's official instructions.
3. **Prepare the bed.** Clean the print sheet with isopropyl alcohol (90% or stronger) and a paper towel, and avoid touching it with your fingers afterwards. Prusa's guide recommends IPA for routine cleaning, and warm water with a little dish soap for residue IPA doesn't shift.
4. **Level the bed.** Run the automatic leveling routine, or follow the manual's paper method for a manually leveled printer.
5. **Set the Z offset.** This is the gap between the nozzle and the bed for the first layer, and it's the single most important setting. Print a first-layer test (many printers have one built in, and Prusa calls it **Live Adjust Z**) and adjust while it prints:
   * **Too high:** lines are round, don't touch each other, and peel off easily.
   * **Too low:** lines are very thin or see-through, rough or ridged, or almost nothing comes out.
   * **Just right:** lines are slightly flattened, joined together, and the surface feels smooth.
6. **Print a calibration cube** (a 20 mm cube is the usual test). Measure it with calipers. Each side should be close to 20 mm. Large errors point to a mechanical or setup problem; small ones are normal.
7. **Print a temperature tower.** It prints the same shape at several temperatures. Pick the lowest temperature that gives good layer bonding, clean overhangs and little stringing. Repeat this for each new brand or type of filament.
8. **Calibrate flow** (also called extrusion multiplier or flow ratio), so the printer pushes out exactly the right amount of plastic. Too much gives rough, bulging surfaces; too little gives gaps and weak parts.
9. **Tune retraction** if you see stringing, with a retraction test. Small changes go a long way.
10. **Print something you'll use,** like a hook or a cable clip, and celebrate.

**Free calibration tools:**
* **OrcaSlicer** has built-in calibration tests for temperature, flow ratio, pressure advance, retraction, volumetric speed and tolerance, with a guide to the order to run them in.
* **[Teaching Tech's 3D printer calibration site](https://teachingtechyt.github.io/calibration.html)** generates test prints for the first layer, temperature, retraction and more. Its G-code is made for Marlin firmware but often works with others.
* **[Ellis' Print Tuning Guide](https://ellis3dp.com/Print-Tuning-Guide/)** covers first layer squish, pressure advance, extrusion multiplier, retraction and more, for Klipper, Marlin and RepRapFirmware printers.

> **Write down what you change.** A simple note of each setting and the result saves hours when something changes later.

---

## 9. Finding Models, and Licenses

### 9.1 Where to find models

* **[Printables](https://www.printables.com/)** (run by Prusa Research)
* **[Thingiverse](https://www.thingiverse.com/)** (one of the oldest model libraries)
* **[MakerWorld](https://makerworld.com/)** (run by Bambu Lab)

All three host free models from the community, with comments and photos of other people's prints ("makes"), which are a good way to see whether a model prints well.

### 9.2 Read the license before you share or sell

Every model has a license chosen by its designer. You can almost always print a free model for yourself. Sharing your changes, or **selling prints**, depends on the license.

| License | Print for yourself | Share a remix | Sell prints |
|---|---|---|---|
| **CC BY** (Attribution) | Yes | Yes, with credit | Yes, with credit |
| **CC BY-SA** (ShareAlike) | Yes | Yes, with credit, under the same license | Yes, with credit, under the same license |
| **CC BY-NC** (NonCommercial) | Yes | Yes, with credit, non-commercially | **No** |
| **CC BY-ND** (NoDerivatives) | Yes | **No** | Check the full terms |
| **Platform or custom licenses** | Read them | Read them | Read them |

* **Platform licenses:** MakerWorld's default "Standard Digital File License" is more restrictive than Creative Commons, and Printables also offers Prusa's own Open Community License. Read the exact terms on the model's page.
* **Characters, brands and logos** from films, games and companies are usually protected regardless of what the uploader picked. A fan-made model doesn't give you the right to sell prints of someone else's character.
* **When in doubt, ask the designer.** Many sell commercial licenses or are happy to give permission.

This is general information, not legal advice. The [Creative Commons license pages](https://creativecommons.org/share-your-work/cclicenses/) explain each license fully.

---

## 10. Designing Your Own Models

This is where 3D printing really opens up. Here's a short introduction; [Learn 3D Modeling](https://github.com/ImmuneMoon/Learn-3D-Modeling) goes much further.

### 10.1 Which tool?

| Tool | Best for | Cost |
|---|---|---|
| **[Tinkercad](https://www.tinkercad.com/)** | Complete beginners. You build models from simple shapes in your web browser, and it exports STL, OBJ and glTF files. | Free, from Autodesk |
| **Autodesk Fusion** (personal use) | Precise mechanical parts with exact dimensions, using parametric CAD | Free for personal, non-commercial use. Autodesk limits this license to home hobby use earning under $1,000 a year, with fewer features than the paid version. Check the [current terms](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Is-there-a-free-version-of-Autodesk-Fusion.html) before you rely on it. |
| **[Blender](https://www.blender.org/)** | Organic and artistic shapes: figures, sculpts, decorative pieces | Free and open source |

Tinkercad and Fusion are **CAD** tools: you design with exact measurements, which suits brackets, boxes and parts that must fit. Blender is a **mesh** modeler: you shape surfaces freely, which suits characters and sculptures. To process many models at once, see [Batch Image and 3D Tools](https://github.com/ImmuneMoon/Batch-Image-and-3D-Tools-GIMP-Blender-Pillow#8-blender-running-in-the-background).

### 10.2 Designing for printing

* **Overhangs and the 45-degree rule:** each layer needs something underneath it. As a rule of thumb, overhangs up to about 45 degrees from vertical print without supports. Prusa notes that well-cooled printers can manage 45 to 60 degrees, and sometimes more. Add chamfers instead of rounded fillets on bottom edges, since fillets there often need supports.
* **Bridges:** short horizontal spans between two supports can print in mid-air. Keep them short.
* **Wall thickness:** make thin walls at least two nozzle widths thick (about 0.8 mm with a 0.4 mm nozzle). Thinner features may not print at all. For walls that need strength, 1 to 1.2 mm or more is safer.
* **Tolerances for fit:** printed parts usually come out slightly larger than designed, so holes come out small and pegs come out big. Start with a gap of about 0.2 to 0.3 mm between parts that must slide or fit together, then print a small test piece with a few different gaps and keep the one that works on your printer.
* **Orientation for strength:** FDM parts are weakest between layers. Lay a part so the forces it will face run **along** the layers, not across them. For example, print a hook lying flat rather than standing up.
* **Flat bottom:** give the part a flat face to sit on the bed. It improves adhesion and avoids supports.
* **Split big or awkward models** into parts that each print well, and join them with pins, glue or screws.

---

## 11. Post-Processing

### 11.1 FDM prints

1. **Remove supports** with flush cutters and pliers. Wear eye protection, since pieces can flick off.
2. **Trim** brims and blobs with a deburring tool or a craft knife, cutting away from yourself.
3. **Sand,** starting coarse (about 120 to 220 grit) and working finer. Wet sanding keeps dust down. NIOSH recommends eye protection for sanding, cutting and grinding, and a dust mask is sensible too.
4. **Prime** with a filler primer to hide layer lines, then sand again lightly. Spray outdoors or in a well-ventilated space.
5. **Paint** with acrylics or spray paint, and seal with a clear coat if it will be handled a lot.

### 11.2 Resin prints

Wear nitrile gloves and eye protection throughout, and follow your resin maker's instructions and SDS.
1. **Remove the print** from the build plate with the plate over the vat or a tray, so drips go back into the resin or onto a disposable surface.
2. **Wash** off the uncured resin in isopropyl alcohol (IPA) or the cleaner your resin maker recommends, by hand or in a wash station. Keep solvent containers closed and away from flames and heat.
3. **Let it dry** completely before curing.
4. **Remove supports.** Many people find this easier before curing, while the resin is slightly softer.
5. **Cure** under UV light (a cure station or sunlight) for the time your resin maker recommends.
6. **Dispose of waste** as described in Section 4.4.

---

## 12. Maintenance

| How often | What to do |
|---|---|
| **Every print** | Check the bed is clean and free of leftover plastic. Wipe with IPA if it's been touched. |
| **Every few weeks** | Check belts are firm and screws are tight. Clean dust and plastic strands from the printer with a damp cloth or brush, not compressed air. |
| **As your manual says** | Lubricate rods, rails and lead screws with the lubricant the manufacturer specifies. Don't over-grease. |
| **When quality drops** | Inspect the **nozzle**. It's a wear part: brass nozzles wear out faster with abrasive filaments. Replace it following your printer's guide, with the hotend hot only if the guide says so. |
| **When needed** | Replace a worn print sheet, check the PTFE tube (on Bowden printers), and update firmware from the official source. |
| **Resin printers** | Check the vat film for cloudiness or damage, filter or replace old resin, and keep the screen clean. Wear gloves. |

---

## 13. Time-Lapses and Inspiration

### 13.1 Making a time-lapse

**"EASIEST way to make a 3D printing time-lapse! | Beagle Camera V2"** ([Shirahaha](https://youtube.com/shorts/Crl49BPmc9k), 1 min, July 2023) explains why a good print time-lapse is harder than it looks. A photo every 60 seconds gives a jittery result, because each layer takes a different time to print and the print head is somewhere different in every shot. Smooth time-lapses take **one photo per layer**, with the head in the same place. The manual way is a camera with a remote shutter, plus printer commands (G-code) that bump the shutter button at the end of every layer, then hundreds of photos joined in an editor.

The short then shows the Beagle Camera V2, a plug-in camera from Mintion that makes time-lapses automatically and lets you watch the printer remotely. It's essentially a product showcase: the description has purchase links and discount codes. Mintion publishes a [compatibility list](https://www.mintion.net/pages/3d-printer-camera-compatibility), so check your printer is on it before you buy.

**Other options:**
* **A built-in camera:** some printers include a camera with a time-lapse option. Check your printer's manual.
* **[OctoPrint](https://octoprint.org/)** with the free **[Octolapse](https://plugins.octoprint.org/plugins/octolapse/)** plugin: OctoPrint is free software that runs your printer from a small computer such as a Raspberry Pi. Octolapse moves the print head out of the way before each snapshot, so every frame looks steady. Check its compatibility notes, since its latest release (November 2023) lists support for Python versions below 3.12.
* **A phone or webcam** on a stand, using a time-lapse app. This works with any printer, but without the head moved aside each frame, the result looks busier.

### 13.2 Research: printing with sound

**"3D printing with acoustic holograms"** ([Freethink](https://www.freethink.com/hard-tech/3d-printing-acoustic-holograms), February 2023) describes **laboratory research**, not a product you can buy. Researchers at the Max Planck Institute for Medical Research and Heidelberg University shaped ultrasound into **acoustic holograms**, using several plates that form the sound waves, to push particles, hydrogel beads and biological cells floating in water into a 3D shape all at once, without touching them. The work was published in *Science Advances*. The researchers suggested it could one day help with **bioprinting** tissues and cell cultures, because sound doesn't damage cells and ultrasound can travel through tissue, but that's a possible future use, not something it does today.

### 13.3 Where this can lead: robotics and animatronics

**"Can 3D printers get this good?"** ([Will Cogley](https://youtube.com/shorts/pD6oljrRDCM), under a minute, June 2025) shows strikingly realistic eyeballs for his animatronic eye mechanisms, and explains how they were made. They're printed with the **White Jet Process (WJP)**, a full-color resin service from the print bureau JLC3DP. It's a material-jetting process that sprays and cures layers of photopolymer like an inkjet, not something a home printer does. The realism comes from design choices as much as the printer:
* **A concave iris,** dished inwards, so the eye has real depth.
* **Hand-drawn iris detail:** the creases, folds and craters of a real iris, then textured and colored.
* **A clear dome** over the whole front, like a cornea.

His **[YouTube channel](https://www.youtube.com/@WillCogley)** shows more 3D-printed animatronics and robots, such as mechanical eyes and robot heads, and his EyeMech eye mechanisms are free to download and print. It's a great example of where printing leads once you add mechanical design, motors and electronics.

To head that way:
1. Learn to design parts that fit and move (Section 10.2, and [Learn 3D Modeling](https://github.com/ImmuneMoon/Learn-3D-Modeling)).
2. Print simple mechanisms: hinges, gears and print-in-place joints.
3. Add electronics: hobby servo motors driven by a microcontroller board such as an Arduino or a Raspberry Pi Pico.
4. Check each design's license before you print, remix or sell it (Section 9.2).

---

## 14. A First-Projects Ladder

Climb one rung at a time. Each step teaches something new.

| Step | Project | What it teaches |
|---|---|---|
| 1 | The printer's sample files and a first-layer test | Bed adhesion and the Z offset |
| 2 | A calibration cube, then a temperature tower | Measuring, and tuning for your filament |
| 3 | Simple useful prints: hooks, cable clips, a phone stand | Choosing settings, orientation and infill for real use |
| 4 | A box with a lid, or a part that fits something you own | Tolerances and measuring with calipers |
| 5 | A print-in-place model with moving joints | Clearances, and when supports aren't needed |
| 6 | Your own design in Tinkercad: a name tag, a replacement knob | The full workflow: design, export, slice, print, fix, reprint |
| 7 | A functional part in PETG, or a flexible part in TPU | New materials and their settings |
| 8 | A multi-part model, painted and finished | Splitting models, assembly and post-processing |
| 9 | A simple mechanism with a motor or servo | Mechanical design and electronics |

---

## 15. Communities and Channels

### 15.1 Communities

* **Reddit:** r/3Dprinting for general discussion, and r/FixMyPrint for diagnosing failed prints. Post a clear photo, your printer, filament, slicer and settings.
* **[Prusa's community forum](https://forum.prusa3d.com/):** discussion of Prusa printers, PrusaSlicer and Printables, with plenty of general advice.
* **[Bambu Lab's forum](https://forum.bambulab.com/):** discussion of Bambu Lab printers, Bambu Studio and MakerWorld.
* **Your printer's official community,** support pages and knowledge base, which are often the fastest source of answers for your exact machine.
* **Makerspaces and libraries:** many have printers, run classes, and have experienced people who'll help.

### 15.2 Free learning channels

None of these channels is affiliated with this guide.

| Channel | What it's like |
|---|---|
| **[CNC Kitchen](https://www.youtube.com/@CNCKitchen)** | Engineering-style experiments: material strength, settings and techniques tested and measured. Posting regularly. |
| **[Teaching Tech](https://www.youtube.com/@TeachingTech)** | Clear calibration guides, upgrades and printer reviews, plus the calibration website in Section 8. In January 2026 the creator announced a return to full-time teaching, so new videos are rare, but the back catalog remains useful. |
| **[Made with Layers (Thomas Sanladerer)](https://www.youtube.com/channel/UCb8Rde3uRL1ohROUVg46h1A)** | In-depth printer and hardware reviews, and commentary on the 3D printing industry. Posting regularly. |
| **[Shirahaha](https://www.youtube.com/@Shirahaha3D)** | Short tips, hacks and time-lapses. Posting regularly. |
| **[Will Cogley](https://www.youtube.com/@WillCogley)** | 3D-printed animatronics and robotics design. |

---

## 16. Troubleshooting

| What you see | Why | What to do |
|---|---|---|
| **The first layer won't stick, or the print comes loose** | Nozzle too high (Z offset), a dirty or greasy bed, wrong bed temperature, or too small a contact area | Re-check the Z offset (Section 8). Clean the sheet with IPA, or dish soap and warm water. Use the bed temperature for your filament, raise it by 5 to 10 °C, add a brim, and slow the first layer. |
| **The first layer is see-through, ridged, or nothing comes out** | Nozzle too low | Raise the Z offset a little. Don't lower the nozzle to fix adhesion: Prusa warns that too low can damage the sheet. |
| **PETG sticks so well it damages the sheet** | PETG bonds strongly to smooth PEI | Use glue stick as a release layer, as Prusa recommends |
| **Stringing (thin hairs between parts)** | Temperature too high, retraction not tuned, or wet filament | Lower the temperature by 5 to 10 °C, run a retraction test, dry the filament (Section 5.2), and reduce travel across open space in your slicer |
| **Warping (corners lift)** | The plastic shrinks as it cools; drafts make it worse. Common with ABS, ASA and large parts. | Use a brim, clean the bed, keep drafts away, use an enclosure for ABS and ASA, and consider PLA or PETG if the part allows |
| **Layer shifts (the print steps sideways)** | Loose belts or pulleys, the nozzle hitting a curled part, or moving too fast | Check belt tension and pulley screws, fix the curling (cooling and adhesion), and lower speed or acceleration for large prints |
| **Gaps, thin walls or weak parts (under-extrusion)** | Partial clog, wet filament, temperature too low, tangled spool, or flow too low | Check the spool turns freely, raise the temperature a little, dry the filament, calibrate flow, and clean or replace the nozzle |
| **Saggy or messy overhangs** | Overhang too steep, too little cooling, or temperature too high | Add supports, increase cooling, lower the temperature, or re-orient the part (Section 10.2) |
| **Spaghetti (a mess of loose strands)** | The print came loose or a support failed | Stop the print, then fix adhesion and supports. A camera helps you catch it early. |
| **"Thermal runaway" or heater error** | The firmware detected a temperature problem, often a loose sensor | Turn the printer off and let it cool. Follow the maker's guide to reseat the sensor or heater. **Never disable thermal protection.** |
| **Resin print stuck to the vat film, not the plate** | Poor plate adhesion, plate not level, or bottom exposure too short | Wear gloves. Clear the vat as the maker describes, re-level the plate, and check the bottom layer exposure for your resin. |

---

## 17. Sources

**Safety**
- NIOSH, "Approaches to Safe 3D Printing: A guide for makerspace users, schools, libraries, and small businesses" (Publication 2024-103, November 2023): https://www.cdc.gov/niosh/publications/numbered/2024-103.html
- UL Research Institutes, Chemical Insights, 3D printing research: https://chemicalinsights.ul.org/
- Marlin firmware, Thermal Protection: https://marlinfw.org/docs/features/thermal_protection.html
- Formlabs, Disposing of resin: https://formlabs.com/support/Disposing-of-resin/

**Materials and troubleshooting (Prusa Knowledge Base)**
- PLA: https://help.prusa3d.com/article/pla_2062
- PETG: https://help.prusa3d.com/article/petg_2059
- ABS: https://help.prusa3d.com/article/abs_2058
- ASA: https://help.prusa3d.com/article/asa_1809
- Flexible materials: https://help.prusa3d.com/article/flexible-materials_2057
- Drying filament: https://help.prusa3d.com/article/drying-filament_332086
- First layer issues: https://help.prusa3d.com/article/first-layer-issues_1804
- Stringing and oozing: https://help.prusa3d.com/article/stringing-and-oozing-issues_1805
- Warping: https://help.prusa3d.com/article/warping_2011
- Layer shifting: https://help.prusa3d.com/article/layer-shifting_2020
- Support material (overhang threshold): https://help.prusa3d.com/article/support-material_1698
- Modeling with 3D printing in mind: https://help.prusa3d.com/article/modeling-with-3d-printing-in-mind_164135

**Slicers and formats**
- UltiMaker Cura: https://ultimaker.com/software/ultimaker-cura/
- UltiMaker Cura on GitHub (license): https://github.com/Ultimaker/Cura
- PrusaSlicer: https://www.prusa3d.com/page/prusaslicer_424/
- PrusaSlicer on GitHub (license): https://github.com/prusa3d/PrusaSlicer
- OrcaSlicer: https://www.orcaslicer.com/
- OrcaSlicer on GitHub (license, official-site warning): https://github.com/OrcaSlicer/OrcaSlicer
- OrcaSlicer wiki (calibration tests): https://www.orcaslicer.com/wiki/
- Bambu Studio: https://bambulab.com/en/download/studio
- Bambu Studio on GitHub (license): https://github.com/bambulab/BambuStudio
- 3MF Consortium: https://3mf.io/

**Calibration**
- Teaching Tech, 3D printer calibration: https://teachingtechyt.github.io/calibration.html
- Ellis' Print Tuning Guide: https://ellis3dp.com/Print-Tuning-Guide/

**Models, licenses and design tools**
- Printables: https://www.printables.com/
- Thingiverse: https://www.thingiverse.com/
- MakerWorld: https://makerworld.com/
- Creative Commons licenses: https://creativecommons.org/share-your-work/cclicenses/
- Tom's Hardware, "Prusa Research introduces the Open Community License": https://www.tomshardware.com/3d-printing/prusa-research-introduces-the-open-community-license-to-protect-open-source-3d-printing-hardware-new-rules-aimed-at-addressing-industry-abuses
- Tinkercad: https://www.tinkercad.com/
- Tinkercad, exporting 3D models for 3D printing: https://www.tinkercad.com/help-center/exporting-3d-models-for-3d-printing
- Autodesk, "Is there a free version of Autodesk Fusion?": https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Is-there-a-free-version-of-Autodesk-Fusion.html
- Blender: https://www.blender.org/

**Time-lapses**
- Mintion, Beagle Camera compatibility: https://www.mintion.net/pages/3d-printer-camera-compatibility
- OctoPrint: https://octoprint.org/
- Octolapse plugin: https://plugins.octoprint.org/plugins/octolapse/

**Animatronic eyes**
- JLC3DP, "What is WJP 3D printing": https://jlc3dp.com/help/article/what-is-wjp-3d-printing
- Hackster.io, "You Can Use These Incredibly Realistic Animatronic Eyeballs in Your Projects": https://www.hackster.io/news/you-can-use-these-incredibly-realistic-animatronic-eyeballs-in-your-projects-96b20b8253a7

**Videos and articles**
- Freethink, "3D printing with acoustic holograms": https://www.freethink.com/hard-tech/3d-printing-acoustic-holograms
- Shirahaha, "EASIEST way to make a 3D printing time-lapse! | Beagle Camera V2": https://youtube.com/shorts/Crl49BPmc9k
- Will Cogley, "Can 3D printers get this good?": https://youtube.com/shorts/pD6oljrRDCM

**Communities and channels**
- Prusa forum: https://forum.prusa3d.com/
- Bambu Lab forum: https://forum.bambulab.com/
- CNC Kitchen: https://www.youtube.com/@CNCKitchen
- Teaching Tech: https://www.youtube.com/@TeachingTech
- Made with Layers (Thomas Sanladerer): https://www.youtube.com/channel/UCb8Rde3uRL1ohROUVg46h1A
- Shirahaha: https://www.youtube.com/@Shirahaha3D
- Will Cogley: https://www.youtube.com/@WillCogley

<!-- guide:end -->

## ☕ Support the Project

If you find this project helpful and want to support further development by Fulllion Creative Works, consider leaving a tip!

* [Donate via PayPal](https://www.paypal.com/donate/?hosted_button_id=LCDZX75HR4CLC)
* [Support on Ko-fi](https://ko-fi.com/fulllion)

---
© 2026 Fulllion Creative Works. All rights reserved.
