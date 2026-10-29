# Aadhar Stambh · V2

Interactive 3D mockup and build plan for **Section 6, Aadhar Stambh**, of the BAPS Diwali 2026 exhibition *Light Beyond Lamps*.

- `index.html`: the whole site in one file (Three.js r128 from cdnjs, all textures drawn in code)
- `portrait.jpg`: the Mahant Swami Maharaj portrait used on the split portrait and in the Shanti room
- `plans/`: alternative 2D floor plans shown in the 2D view under **Floor plan options** (a PDF plus a JPG preview for each). The tab shows **Current mockup** (drawn from the model's own data), **Option 1** (a PDF plan) and **Option 2** (the current mockup with the Shastra columns turned into east–west rows, drawn in code from `ALT`, `ROUTE2` and `FIX2` in `build2D`). Drawn options show the visitor path, spotlights, volunteers, guides, a legend and the spot list; this replaced the old Lighting tab. To add a PDF option, drop `option-N.pdf` and `option-N.jpg` in `plans/` and add a row to `PLAN_OPTS` in `index.html`. These are reference layouts only and do not change the 3D model.

The site is served by GitHub Pages from the `main` branch. Any change merged into `main` is live within a minute or two.

## For anyone (or any Claude) editing this

Read this section before changing anything. These decisions were made deliberately. Don't undo them unless the section lead asks.

### Space
- 40 × 30 ft, one open room (grew from 40 × 20; the extra 10 ft went along the south side, so the entrance and walk order are unchanged). Plywood walls, 8 ft high, built from 4 × 8 ft modules. No walls between the three parts.
- Gym floor covered with black loop carpet.
- Entrance at the top-left (5 ft opening, from the Mulyo section), exit at the bottom-right (south end of the east wall), so Sant is walked as an S: up the photo side, round the north end, back down the information side.
- Walk order: **Mandir → Shastra → Sant**.
- Mood: dark, quiet and museum-like. Light comes from warm spotlights on each piece; hall lights are off.
- Each part has one statement piece plus supporting pieces.
- **Spot lights:** 23 fixtures (buy 25), warm white: 15 clamp-on spots on wall tops and the two Shastra T-posts, plus 8 small picture lights on the Sant panels. No ceiling rigging is needed.

### Mandir
- **Chaos hallway** (about 9 × 5 ft, widened so the entrance isn't tight): walls black from floor to ceiling, with one continuous stream of phone notifications and photos running at eye level and two cold flicker bulbs. No sound. It doubles as the queue.
- **Shanti room** (9 × 8 ft, sealed, with a ceiling; shrunk from 9 × 9 to widen the hallway): a backlit carved jali wall on the west wall with three arches and three framed photos, a glossy white floor, and a kirtan instrumental. **No screens, no projector.** Groups of about 8 for 90 seconds. People enter at the NE corner and **exit through the south wall, with the Better Living (BLS) booth on their right**.
- **Booths:** BKY is an L in the corner by the hallway: one 6 ft wall on the north wall joined to a second 6 ft wall on the blank end of the hallway and Shanti room. Better Living Sessions is on the side wall right outside the Shanti exit (not on the Charities wall). BAPS Charities is on the south wall. All are booth kits (wall, header, ledge, spot, outlet). Volunteers stand there and talk with visitors. Each activity lead decides what happens in their booth. No people figures in the model, except one animated visitor that walks the route (turn it and the floor path off with the Visitor path button).

### Shastra
- **Layout:** two compact columns of case, scroll, scroll, case (about 7.5 ft each) with a 6 ft aisle between them, set 3 ft toward the Shanti room from the earlier plan. The NFC wall is centred on the aisle.
- **Walk order:** from Mandir up to the spine wall, along it, down the aisle between the columns, along the NFC wall, then on to Sant. There is no path across the middle of the columns.
- **Floating pages:** 4 fabric scrolls, 1.5 × 9.5 ft, two between the cases in each column, facing the aisle ("SHASTRA" on the first). Each pair hangs from a black T-post hidden in the gap between the two scrolls.
- **Spine wall:** 6 giant book spines (about 9 ft of wall); every other one opens (1st, 3rd and 5th: Vachanamrut, Swamini Vato, Shikshapatri); the rest stay closed.
- **4 glass cases**, one scripture each, at the ends of the two columns. Name plates face the aisle.
- **2 NFC stations** on the south wall, centred on the aisle, 2.4 ft apart. Each has a tablet as the tap point and a TV above that shows the answer.
- The text lantern was dropped.

### Sant
- **Sant panels:** 4 freestanding panels (2 ft wide, 8 in deep, 7 ft 8 in tall) in one 12 ft row down the middle of Sant, 16 in apart so the row reads as one piece. People walk up the photo side (facing Shastra), turn at the north end past the night-prasang corner, and come back down the information side. The backs explain one idea each: What is a Guru?, The Guru Parampara, Pramukh Swami Maharaj, Mahant Swami Maharaj. A small picture light sits on top of each face.
- **Birthday wall** on the east wall of Sant, facing the back of the panels: a TV with an iPad on a floor stand in front. Type a birthday on the iPad; the TV shows where Pramukh Swami Maharaj or Mahant Swami Maharaj was that day. Printed words around the TV explain it.
- **City at night:** a dark foam-board skyline wrapped around the north-east corner of Sant, where the walk turns: three towers on the north wall, three on the east wall (about 7 ft each), in time order. Headline "AWAKE FOR ALL OF US" (exhibition line). Six towers, each with a time (10:53 PM to 2:30 AM) and one glowing window (frosted acrylic, LED puck). A gold ledge at 4 ft 10 in with a warm LED strip under it lights six tilted cards: time, place and date, a short summary of what Mahant Swami Maharaj was praying for, and the source page. Summaries are drafts to be checked against the book. The bicycle and book plinths were removed.
- **Closing wall** (minimal), on the south wall of Sant, facing people as they come down the back of the panels, the last thing before the exit: matte black, no border; "AADHAR STAMBH · The pillars that sustain a legacy" set small and left-aligned (an exhibition line, not a quotation); one row of five frameless Sant prints, all 18 in tall, at eye level; one slim linear light above the row. Keep it clean. No take-home cards.

### Stanchions
- None for now. The scrolls fill the space between the cases, so the earlier ropes were removed.

### Signage
- **No banners or hanging signs.** Each part is named inside its own piece: "Mandir" is carved into the jali lintel over the Shanti room door, "Shastra" is the first word on the first scroll, and "Sant" is lettered under the photo on the middle Sant panel. Each name is in English and Gujarati.

### Content rules
- Anything not decided yet stays as a placeholder in [brackets].
- Never invent quotes or teachings attributed to Pramukh Swami Maharaj, Mahant Swami Maharaj or the scriptures. Leave a placeholder until the approved wording arrives.

## Technical notes
- Keep the scene to **about 18 lights or fewer** (spot plus point lights). More than that leaves the 3D view blank on some devices. All spot lights come from the `FIX` table: every row draws a fixture, but only rows with an intensity add a real light, which keeps the count at 18.
- Room coordinates are in feet: x runs 0–40 along the length, z runs 0–30 across. Item info lives in `ITEMS`; the 2D materials list in `MATERIALS`; the shopping list in `BOM` and the media list in `MEDIA` (both inside `build2D`). If you change a piece, update its quantities in `BOM` too.
- The 2D plan, the dimensions and the walk-through stops are hand-placed. If you move a piece, update its `ITEMS.at`, its collider in `addColliders`, its dimension lines in `buildDims` and `build2D`, and the `ROUTE` and `STOPS` if the walk passes it.
- Test before you merge: open the page, check Overview, Floor plan, Walk through, Walk around and the 2D tabs, and look at the browser console for errors.

## Walking space
- The **Walking space** toggle shades clear walkway (green), people using a piece (amber) and viewers (blue), and measures clear widths at the places people pass. Aim for 4 ft or more; under 3 ft shows red.

## Working together
- One person changes a part at a time, or works on a branch and opens a pull request.
- Write a clear commit message for each change (for example "Move NFC stations side by side").

- Four red rope stanchion lines (no extra walls) keep the walk in order: one between the Swamini Vato case and the NFC wall, so people coming back from Charities go up to BKY instead of cutting across; one runs south from the corner of the Shanti room (about 11 ft), so people leaving the room go down past Better Living to BAPS Charities before turning back up towards Shastra; one from the end of the spine wall to the Vachanamrut case, so people go down the Shastra aisle instead of cutting across to Sant; one from the south end of the Sant panels to the south wall, so people go up the photo side before the exit. The north-east corner of Sant is saved for the night prasangs.
