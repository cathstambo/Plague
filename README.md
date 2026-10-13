# Escape the Sanctuary — Plague Protocol

A four-room, portrait-only browser escape game for the Gremlins alliance.
Intended URL: `https://cathstambo.github.io/Plague/`

## Files

```
index.html         all HTML, CSS and JavaScript (no frameworks, CDNs or external fonts)
assets/room1.png   The Infirmary            (approved art, unmodified)
assets/room2.png   The Apothecary           (approved art, unmodified)
assets/room3.png   The Main Sanctuary Hall  (approved art, unmodified)
assets/room4.png   The Final Escape         (approved art, unmodified)
README.md
```

## Deploying to GitHub Pages

1. Upload the contents of this ZIP to the root of the `Plague` repository (keep the `assets/` folder).
2. Settings → Pages → Deploy from branch → `main` / root.
3. Open `https://cathstambo.github.io/Plague/`.

## How it plays

- Tap the small magnifying glasses on the artwork to investigate.
- The satchel button (top right) opens the inventory. Documents can be re-read there, which is how clues from earlier rooms reach the final room.
- In Room 4, choose a stained-glass piece from the satchel, then tap one of the four circles above the doors. Tap a filled circle to take a piece back. The magnifier in the centre of the cross opens the same puzzle as a dialog.
- Progress saves automatically in the browser (`localStorage`). The restart button asks for confirmation before wiping it.

## Solutions (organiser only)

| Room | Solution |
|---|---|
| 1 | Chest code `472` (Crow 4, Gravebloom 7, Frostmoss 2) |
| 2 | Silverleaf, then Frostmoss, then Moonwater |
| 3 | Gate order Serpent, Sun, Crow, Moon |
| 4 | Top Gold Unicorn, Right Red Plague Doctor, Bottom Green Gremlin, Left Blue Taco |

Escape code: `GREMLIN-ESCAPED`

**Security note:** the escape code and all solutions are readable in the page source. Anyone who views source can skip the game. Treat the code as a fun confirmation, not proof of solving, if prizes are at stake.

## Change log from the recovered implementation

Wording was preserved wherever it existed. Additions and fixes:

1. Layout, zoom, pan, camera, rectangle hotspots, journal panel and object list removed and replaced with a static portrait image plus magnifier icons, as specified.
2. The "Carvings in the Beams" dialog gained one introductory line explaining where the carvings are.
3. Medicine chest: reopening after it is solved now says it is empty instead of showing the code entry again. Wrong codes show feedback inside the same dialog for retry.
4. Room 1 door: an explicit "Unlock the door" button uses the key (the key is consumed).
5. Room 2 doorway is a new hotspot. Before the brew: "The passage leads to the Main Sanctuary Hall, where someone is very sick. Going without a cure would be pointless." After: a button to enter the Main Hall.
6. Cauldron: tapping a filled slot removes that ingredient. Reopening after success shows the brew is done.
7. Recipe book: the margin note is introduced with "Scrawled in the margin:".
8. Guard: an explicit "Give the antidote" button (antidote is consumed). Desk: "Use the iron key" button (iron key is consumed).
9. Desk revisit text says "The drawer held…" instead of "Inside you find…".
10. Revised watch orders became their own satchel item so they can be re-read.
11. The brass cog is consumed when the gate opens. The watchman's seal is kept because its engraving is a Room 4 clue.
12. Rusty key: the art shows no hearth, so the magnifier sits on the tiny chest on the desk. The established wording is unchanged.
13. Cabinet: the art shows a locked cabinet, so a first step was added: "A sturdy cabinet with an iron padlock. On closer inspection, the padlock hangs from a single rusted screw." with a "Wiggle the padlock" button. The original line ("…never properly locked. Typical.") follows unchanged.
14. Quarantine notice revisit: "The loose wax seal hangs open. Nothing else is hidden behind it."
15. Repeat finds say "You already have the … piece." instead of re-announcing it.
16. Lever messages are now split by cause: missing pieces ("You must collect all four stained-glass pieces first."), empty sockets ("…until all four witnesses are in their sockets."), and wrong arrangement (the established "glass flashes" line). The original incomplete-socket line said "correct sockets", which hinted the arrangement was wrong before the player tried it.
17. Short intro dialog added on first launch, using the established Room 1 objective.
