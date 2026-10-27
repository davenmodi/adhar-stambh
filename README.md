# Aadhar Stambh · V2

Interactive 3D mockup and build plan for **Section 6, Aadhar Stambh**, of the BAPS Diwali 2026 exhibition *Light Beyond Lamps*.

- `index.html`: the whole site in one file (Three.js r128 from cdnjs, all textures drawn in code)
- `portrait.jpg`: the Mahant Swami Maharaj portrait used on the split portrait and in the Shanti room

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

### Mandir
- **Chaos hallway** (about 9 × 5 ft, widened so the entrance isn't tight): walls black from floor to ceiling, with one continuous stream of phone notifications and photos running at eye level and two cold flicker bulbs. No sound. It doubles as the queue.
- **Shanti room** (9 × 8 ft, sealed, with a ceiling; shrunk from 9 × 9 to widen the hallway): a backlit carved jali wall on the west wall with three arches and three framed photos, a glossy white floor, and a kirtan instrumental. **No screens, no projector.** Groups of about 8 for 90 seconds. People enter at the NE corner and **exit through the south wall, facing the Better Living (BLS) booth**.
- **Booths:** BKY is an L in the corner by the hallway: one 6 ft wall on the north wall joined to a second 6 ft wall on the blank end of the hallway and Shanti room. Better Living Sessions is on the side wall right outside the Shanti exit (not on the Charities wall). BAPS Charities is on the south wall. All are booth kits (wall, header, ledge, spot, outlet). Volunteers stand there and talk with visitors. Each activity lead decides what happens in their booth. **No people figures in the model.**

### Shastra
- **Floating pages:** 5 long fabric scrolls, 1.5 × 9.5 ft, hanging from a truss, with a clear aisle down the middle. Keep it to a few scrolls; more felt crowded.
- **Spine wall:** 8 giant book spines; 4 of them open (Vachanamrut, Swamini Vato, Shikshapatri, Satsang Diksha).
- **4 glass cases**, one scripture each, spread to the four corners of the zone.
- **2 NFC stations, side by side** on one wall. Each has a tablet as the tap point and a TV above that shows the answer.
- The text lantern was dropped.

### Sant
- **Split portrait:** 5 panels form one portrait of Mahant Swami Maharaj from the front; the backs carry 5 topics. Two angled fins hide the rest of Sant until you walk past.
- **Birthday wall** behind the portrait: a TV on the south wall with an iPad on a floor stand in front. Type a birthday on the iPad; the TV shows where Pramukh Swami Maharaj or Mahant Swami Maharaj was that day. Printed words around the TV explain it.
- **2 prasangs** (the bicycle and the book) stand in front of the portrait's two wings (fins), one on each side, facing Shastra.
- **Closing wall** (minimal): matte black, no border; "AADHAR STAMBH · The pillars that sustain a legacy" set small and left-aligned (an exhibition line, not a quotation); one row of five frameless Sant prints, all 18 in tall, at eye level; one slim linear light above the row. Keep it clean. No take-home cards.

### Signage
- **No banners or hanging signs.** Each part is named inside its own piece: "Mandir" is carved into the jali lintel over the Shanti room door, "Shastra" is the first word on the first scroll, and "Sant" is lettered on the portrait base. Each name is in English and Gujarati.

### Content rules
- Anything not decided yet stays as a placeholder in [brackets].
- Never invent quotes or teachings attributed to Pramukh Swami Maharaj, Mahant Swami Maharaj or the scriptures. Leave a placeholder until the approved wording arrives.

## Technical notes
- Keep the scene to **about 18 lights or fewer** (spot plus point lights). More than that leaves the 3D view blank on some devices.
- Room coordinates are in feet: x runs 0–40 along the length, z runs 0–20 across. Item info lives in `ITEMS`; the 2D materials list in `MATERIALS`; the media list in `MEDIA` (inside `build2D`).
- The 2D plan, the dimensions and the walk-through stops are hand-placed. If you move a piece, update its `ITEMS.at`, its collider in `addColliders`, its dimension lines in `buildDims` and `build2D`, and the `ROUTE` and `STOPS` if the walk passes it.
- Test before you merge: open the page, check Overview, Floor plan, Walk through, Walk around and the 2D tabs, and look at the browser console for errors.

## Walking space
- The **Walking space** toggle shades clear walkway (green), people using a piece (amber) and viewers (blue), and measures clear widths at the places people pass. Aim for 4 ft or more; under 3 ft shows red.

## Working together
- One person changes a part at a time, or works on a branch and opens a pull request.
- Write a clear commit message for each change (for example "Move NFC stations side by side").
