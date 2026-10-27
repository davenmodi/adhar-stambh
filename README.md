# Aadhar Stambh · V2

Interactive 3D mockup and build plan for **Section 6, Aadhar Stambh**, of the BAPS Diwali 2026 exhibition *Light Beyond Lamps*.

- `index.html`: the whole site in one file (Three.js r128 from cdnjs, all textures drawn in code)
- `portrait.jpg`: the Mahant Swami Maharaj portrait used on the split portrait and in the Shanti room
- `plans/`: alternative 2D floor plans shown in the 2D view under **Floor plan options** (a PDF plus a JPG preview for each). The tab shows **Current mockup** (drawn from the model's own data), **Option 1** (a PDF plan) and **Option 2** (the current mockup with the Shastra columns turned into east–west rows, drawn in code from `ALT`, `ROUTE2` and `FIX2` in `build2D`). Drawn options show the visitor path, spotlights, volunteers, guides, a legend and the spot list; this replaced the old Lighting tab. To add a PDF option, drop `option-N.pdf` and `option-N.jpg` in `plans/` and add a row to `PLAN_OPTS` in `index.html`. These are reference layouts only and do not change the 3D model.

The site is served by GitHub Pages from the `main` branch. Any change merged into `main` is live within a minute or two.

## For anyone (or any Claude) editing this

Read this section before changing anything. These decisions were made deliberately. Don't undo them unless the section lead asks.

### Space
- 40 × 20 ft, one open room. Plywood walls, 8 ft high, built from 4 × 8 ft modules. No walls between the three parts.
- Gym floor covered with black loop carpet.
- Entrance at the top-left (5 ft opening, from the Mulyo section), exit at the top-right.
- Walk order: **Mandir → Shastra → Sant**.
- Mood: dark, quiet and museum-like. Light comes from warm spotlights on each piece; hall lights are off.
- Each part has one statement piece plus supporting pieces.
- **Spot lights:** 23 fixtures (buy 25), warm white: 17 clamp-on spots on wall tops and the two Shastra T-posts, plus 6 small picture lights on the Sant pillars. No ceiling rigging is needed. The full list is under Floor plan options in the 2D view.

### Mandir
- **Chaos hallway** (about 9 × 5 ft, widened so the entrance isn't tight): walls black from floor to ceiling, with one continuous stream of phone notifications and photos running at eye level and two cold flicker bulbs. No sound. It doubles as the queue.
- **Shanti room** (9 × 8 ft, sealed, with a ceiling; shrunk from 9 × 9 to widen the hallway): a backlit carved jali wall on the west wall with three arches and three framed photos, a glossy white floor, and a kirtan instrumental. **No screens, no projector.** Groups of about 8 for 90 seconds. People enter at the NE corner and **exit through the south wall, with the Better Living (BLS) booth on their right**.
- **Booths:** BKY is an L in the corner by the hallway: one 6 ft wall on the north wall joined to a second 6 ft wall on the blank end of the hallway and Shanti room. Better Living Sessions is on the side wall right outside the Shanti exit (not on the Charities wall). BAPS Charities is on the south wall. All are booth kits (wall, header, ledge, spot, outlet). Volunteers stand there and talk with visitors. Each activity lead decides what happens in their booth. **No people figures in the model.**

### Shastra
- **Layout:** two columns of glass case, scroll, scroll, glass case (P S S P), running from the spine wall toward the NFC wall, with a 6 ft aisle between them. Each column is packed into about 7.5 ft, which leaves about 5.3 ft walking bands at both ends.
- **Walk order:** from Mandir up to the spine wall, along it, down the aisle between the columns, along the NFC wall, then on to Sant. There is no path across the middle of the columns.
- **Floating pages:** 4 fabric scrolls, 1.5 × 9.5 ft, two in each column, facing the aisle. Each pair hangs from a black T-post hidden in the gap between the two scrolls.
- **Spine wall:** 8 giant book spines; 4 of them open (Vachanamrut, Swamini Vato, Shikshapatri, Satsang Diksha).
- **4 glass cases**, one scripture each, at the ends of the two columns. Name plates face the aisle.
- **2 NFC stations, side by side** on one wall. Each has a tablet as the tap point and a TV above that shows the answer.
- The text lantern was dropped.

### Sant
- **Sant pillars:** 3 freestanding pillars (2 ft wide, 8 in deep, 7 ft 8 in tall) in one straight row across the middle of Sant, 3 ft apart. The front, facing Shastra, has one large photo each. The back explains one idea each: What is a Guru?, Pramukh Swami Maharaj, Mahant Swami Maharaj. A small picture light sits on top of each face.
- **Birthday wall** on the east wall of Sant, beside the exit, facing the back of the pillars: a TV with an iPad on a floor stand in front. Type a birthday on the iPad; the TV shows where Pramukh Swami Maharaj or Mahant Swami Maharaj was that day. Printed words around the TV explain it.
- **2 prasangs** (the bicycle and the book) stand between Shastra and the pillar row, one in front of each end, facing Shastra.
- **Closing wall** (minimal), on the north wall of Sant, the last thing before the exit: matte black, no border; "AADHAR STAMBH · The pillars that sustain a legacy" set small and left-aligned (an exhibition line, not a quotation); one row of five frameless Sant prints, all 18 in tall, at eye level; one slim linear light above the row. Keep it clean. No take-home cards.

### Signage
- **No banners or hanging signs.** Each part is named inside its own piece: "Mandir" is carved into the jali lintel over the Shanti room door, "Shastra" is the first word on the first scroll, and "Sant" is lettered under the photo on the middle Sant pillar. Each name is in English and Gujarati.

### Content rules
- Anything not decided yet stays as a placeholder in [brackets].
- Never invent quotes or teachings attributed to Pramukh Swami Maharaj, Mahant Swami Maharaj or the scriptures. Leave a placeholder until the approved wording arrives.

## Technical notes
- Keep the scene to **about 18 lights or fewer** (spot plus point lights). More than that leaves the 3D view blank on some devices. All spot lights come from the `FIX` table: every row draws a fixture, but only rows with an intensity add a real light, which keeps the count at 18.
- Room coordinates are in feet: x runs 0–40 along the length, z runs 0–20 across. Item info lives in `ITEMS`; the 2D materials list in `MATERIALS`; the media list in `MEDIA` (inside `build2D`).
- The 2D plan, the dimensions and the walk-through stops are hand-placed. If you move a piece, update its `ITEMS.at`, its collider in `addColliders`, its dimension lines in `buildDims` and `build2D`, and the `ROUTE` and `STOPS` if the walk passes it.
- Test before you merge: open the page, check Overview, Floor plan, Walk through, Walk around and the 2D tabs, and look at the browser console for errors.

## Walking space
- The **Walking space** toggle shades clear walkway (green), people using a piece (amber) and viewers (blue), and measures clear widths at the places people pass. Aim for 4 ft or more; under 3 ft shows red.

## Working together
- One person changes a part at a time, or works on a branch and opens a pull request.
- Write a clear commit message for each change (for example "Move NFC stations side by side").
