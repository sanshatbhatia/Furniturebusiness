# Build plan (draft, no code yet)

Based on `QUESTIONS.md`. Open answers become editable defaults, so they don't block the build.

## What it is

An app that turns a measured wall into a cut list, hardware list and quote, for a shop that cuts on a panel saw.

## Stack (recommended)

- **Installable web app**: opens from a link, "Add to home screen" on the phone, same app on the laptop. No Play Store.
- **v1 data on the phone**, with a backup file. **v2** adds login + sync so phone and laptop share jobs.
- PDF made on the phone, shared to WhatsApp from the phone's share button.
- Every label in a Hindi file and an English file, with a switch.

## Screens (step by step, big buttons, pictures, number keypad)

1. **Jobs**: list of jobs, "New job"
2. **Customer**: name, phone, site
3. **Wall**: length and height in mm (one wall first, more walls later)
4. **Cabinets**: tap picture tiles (base, wall, tall, loft, drawer unit); they line up on the wall; leftover shows as a filler
5. **Cabinet details**: width / height / depth, board + thickness, shutters, drawers (channel or tandem), handle (4 to 12 inch), legs or skirting
6. **Result**: cut list by board, hardware list, edge band metres, sheets needed
7. **Quote**: per square metre, or material + labour; margin; GST 18%; PDF; WhatsApp
8. **Settings**: prices, default sizes, gaps, kerf, edge band, hinge rule, language

## Calculation rules (defaults, all editable, all to confirm with dad)

| Rule | Default |
|---|---|
| Board thickness | 18 mm |
| Bottom vs sides (Q13) | choice per cabinet; default bottom between the sides |
| Top of base units | full top panel |
| Back panel | 6 mm, grooved into the carcass; TV unit: no back |
| Shutter fit | overlay; laminate / acrylic / PU; gaps 3 mm between, 1.5 mm outer, 1.5 mm top/bottom |
| Edge band | carcass front edges; shutters all 4 edges; 0.8 mm; cut size reduced by tape thickness |
| Hinges | soft-close; 2 up to 900 mm door height, 3 up to 1500, 4 up to 2000 |
| Handles | 1 per shutter / drawer |
| Legs | 4 per base cabinet |
| Fillers | always; width = leftover wall length |
| Starting sizes | base 720 x 560, wall 720 x 300, tall 2100 x 560, loft 450 x 300 (height x depth) |
| Sheet | 2440 x 1220 mm, kerf 2.5 mm, edge trim 0 |

## Panel saw note

A panel saw only makes straight cuts right across the board. The sheet layout must use cuts like that, so expect lower sheet use than the ~95% CNC software claims.

## Build order

1. **One cabinet -> its panels and hardware.** Check against dad's paper calculation.
2. **Full wall:** cabinets line up, filler worked out, cut list + hardware list.
3. **Quote + PDF + WhatsApp.**
4. **Sheet layout** for the panel saw.
5. **Hindi / English, big-button polish**, test with a real user from the shop.
6. **Login + phone / laptop sync.**

Later: CNC files (once the machine is chosen), 2D wall drawing, 3D view, more walls and rooms.
