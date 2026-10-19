# Recon map: Haixun Furniture Software (Windows desktop)

Vendor: Qingdao Haixun Software Engineering Co., Ltd. (hisoonsoft.com), China, est. 2013
Scope: the design-to-cut-list slice (measure a space, fill it with cabinets, get panels, hardware and a quote)
For: a family modular-kitchen / woodwork shop (own use, not for sale)
Date: 2026-10-19

## How this was researched (and its limits)

- hisoonsoft.com is blocked from this environment, so the vendor pages were read
  only through search-result extracts. No screenshots, no demo, no account.
- Everything below is the vendor's own marketing claims. No independent reviews found.
- Newest release notes found: V4.0 / 4.0.15 (~2022). Downloads page last updated Nov 2019.
- Because of this, there is no real screen inventory. Screens below are inferred
  from features, marked `guess`.

## Sources

| # | source | URL | notes |
| --- | --- | --- | --- |
| 1 | home page | https://www.hisoonsoft.com/ | product family overview |
| 2 | product list | https://www.hisoonsoft.com/product/ | all modules |
| 3 | design system | https://www.hisoonsoft.com/haixun-furniture-design-system/ | design + BOM/quote |
| 4 | production system | https://www.hisoonsoft.com/haixun-furniture-production-system/ | nesting, CNC, labels |
| 5 | V4.0 release notes | https://www.hisoonsoft.com/latest-news/new-upgrade-on-haixun-v4.0-series.html | hardware, edge banding, QR |
| 6 | Speed 4.0 intro | https://www.hisoonsoft.com/latest-news/speed-4.0-series-of-haixun-furniture-design.html | size association, angled cuts |
| 7 | process flow | https://www.hisoonsoft.com/process-flow/ | store -> factory -> machine |
| 8 | cutting optimization | https://www.hisoonsoft.com/haixun-plate-cutting-optimization-system/ | nesting |
| 9 | door carving | https://www.hisoonsoft.com/haixun-door-plank-carving-system/ | CNC door carving |
| 10 | packaging & delivery | https://www.hisoonsoft.com/haixun-packaging-and-delivery-system/ | pack check, labels |
| 11 | cloud rendering | https://www.hisoonsoft.com/haixun-cloud-rendering-system/ | in-store renders |
| 12 | production mgmt (ERP) | https://www.hisoonsoft.com/haixun-furniture-production-management-system/ | no details found |
| 13 | downloads | https://www.hisoonsoft.com/download/ | Baidu Netdisk installers |
| 14 | India reseller | https://www.indiamart.com/proddetail/haixun-furniture-design-and-production-software-2856877314862.html | Windows, lifetime, 1 device, free demo |
| 15 | EC21 listing | https://hisoonsoft.en.ec21.com/ | ~US$1,500 export price (not official) |

## What the product actually is

Not one tool. A suite of 7 modules for **panel furniture factories** (board/plywood/MDF cabinets):

1. **Furniture Design System** - 3D cabinet design + one-click reports
2. **Furniture Production System / Plate Cutting Optimization** - sheet nesting, CNC output, labels
3. **Cloud Rendering System** - photo-style renders for customers in the showroom
4. **Door Plank Carving System** - CNC carving of shutter/door designs
5. **Packaging and Delivery System** - check every panel is cut, pack by order/cabinet, labels
6. **Production Management System** - ERP (no detail found)
7. Plug-ins

Pipeline in their words: store designer designs -> sends to factory -> factory checks, places
production order -> software generates machine programs -> machines cut/drill -> pack -> deliver.

## Important correction to the brief

- The brief said the tool builds the plan "just looking at the place". **No evidence of that.**
- No photo / room-scan / AI auto-layout was found.
- What it does: a designer types the room size, places cabinets by hand, and the software
  **auto-resizes** cabinets and panels to fit ("size association"). If the room size changes
  later, the design updates.
- The "magic" is the step after: once cabinets are placed, every panel, hole, hinge,
  handle and channel is counted automatically.

## Core loop

Enter the space -> place parametric cabinets -> one click gives panel cut list, hardware list,
quotation (and in their full suite: nesting + CNC files).

## Features (from vendor claims)

Design:
- Cloud + local cabinet library ("dual database"), save any cabinet as a reusable module
- Reuse a module with new width/height/depth, board thickness, scaling
- Size association: auto-place cabinets, shift/scale panels to fit a space; edit room size after
- One-key angled cut for standard and stair cabinets; inclined panels and holes auto-calculated
- Add hardware in one step: slide channels, handles, hinges, wardrobe rods; holes auto-generated
- Hardware hole collision check
- Mark parts as "non-produced" (bought-in hardware) so they show separately in reports
- Edge banding per edge, with colour preview by thickness (e.g. "3 thin 1 thick")
- Exploded drawings of each cabinet; QR code on the material list opens it on a phone

Reports (one click):
- Panel BOM (cut list), accessory BOM, hardware list, quotation, electronic-saw list, hole info

Production:
- Nesting: ~95% sheet utilisation claimed; nests odd shapes, fills scrap with small parts
- Separate layouts per board thickness and colour; leftover stock tracked
- Cutting/drilling path optimisation
- Output files for panel saw, labeller, CNC router, PTP, 5/6-sided drill (G-code)
- Labels per panel: order, layout, panel info, side-hole direction

After production:
- Check for missing/wrong panels before packing
- Pack by order or by cabinet, weight + area, box labels, multi-device sync

## Screens (inferred, all `guess`)

| ID | screen | purpose | key components | confidence |
| --- | --- | --- | --- | --- |
| S01 | Project / order list | open or start a customer job | table, search | guess |
| S02 | Room / space setup | enter wall lengths, height, openings | dimension inputs, 2D plan | guess |
| S03 | 3D design canvas | place and resize cabinets | 3D view, library panel, properties | medium |
| S04 | Cabinet library | pick base / wall / tall / corner modules | grid of modules, cloud + local tabs | medium |
| S05 | Cabinet editor | change size, thickness, shelves, doors, edge banding | parametric form, panel list | medium |
| S06 | Hardware picker | add hinges, channels, handles, rods | catalog, auto-hole preview | medium |
| S07 | Reports | cut list, hardware list, quote, saw list | tables, export, print | high |
| S08 | Nesting / layout | sheet layouts, utilisation % | sheet diagrams, manual adjust | high |
| S09 | Machine export + labels | CNC files, label printing | export dialog, label preview | high |
| S10 | Pack / delivery check | scan panels, pack, box labels | scanner input, checklist | medium |

## Flows

```
F01 Quote a kitchen (the core loop)
    S01 new job -> S02 enter 11ft x 6ft wall -> S04 pick cabinets -> S03 place/auto-fit
    -> S06 add hardware -> S07 one-click cut list + hardware + quote
    edge: corner cabinet, wall not square, window/pipe in the way, odd leftover gap (filler)

F02 Send to production
    S07 -> S08 nest panels on 8x4 sheets -> S09 export saw/CNC files + print labels

F03 Pack and deliver
    S09 labels -> S10 scan each panel, pack per cabinet, box labels
```

## Inferred data model

```
Customer   name, phone, site address                      confidence: guess
Project    customer, room(s), status, date                confidence: guess
Room       walls (length, height), openings (window/door/pipe)  confidence: medium
Cabinet    type (base/wall/tall/corner), w/h/d, carcass board, shutter board,
           shelves, drawers, doors, position on wall      evidence: S03/S05 features  confidence: high
Panel      cabinet, name (side/top/bottom/back/shelf/shutter), length, width,
           thickness, material, grain, edge banding per edge, holes   confidence: high
Hardware   type (hinge/channel/handle/rod/leg), qty, unit price, linked panel  confidence: high
Material   board type, sheet size, thickness, colour, price per sheet  confidence: high
SheetLayout  material, sheet index, placed panels (x, y, rotated), waste %  confidence: high
Quote      line items (boards, edge band, hardware, labour, margin), total  confidence: high
```

Relationships: Customer 1-n Project, Project 1-n Room, Room 1-n Cabinet, Cabinet 1-n Panel,
Cabinet 1-n Hardware, Panel n-1 Material, Material 1-n SheetLayout.

## Feature matrix

See `features.csv`. Must: 13, should: 9, could: 6, skip: 6.

## Out of scope (cannot or should not be cloned)

- CNC G-code / machine post-processors: only useful if the shop owns a CNC; very machine-specific
- Door carving CNC: same
- Photoreal cloud rendering: big effort, low value for a small shop (simple 3D is enough)
- ERP / multi-factory sync / packaging scanners: factory-scale, not a family shop
- Their cabinet library and models: theirs, build our own from the shop's real standards
- "Look at the room and plan it" via photo/AI: the original does not do this either

## Size

- Full suite clone: **XL** (years of work by a company). Rescope.
- Dad's slice (F01 + simple F02 nesting + PDF/Excel export): **M** (a few weeks).
- Hard parts:
  1. Getting the cabinet construction rules right (how panels are derived from a cabinet
     size, board thickness deductions, back panel groove, shutter gaps) - needs dad's input
  2. Sheet nesting with grain direction and saw kerf
  3. A usable 2D/3D layout editor
