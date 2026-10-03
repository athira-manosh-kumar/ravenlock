# Ravenlock

Atmospheric browser investigation game. This repository contains the latest playable source snapshot, artwork, narrative canon and checks.

## Run in Visual Studio Code

Install Node.js (20 or newer), clone this repository and open its folder in VS Code. In the integrated terminal:

```sh
npm run dev
```

Open http://localhost:4173. No npm dependencies or account are required. Progress is saved in the browser; local and hosted saves are separate.

## Project layout

- `dist/`: editable, directly served game source and assets (no build step).
- `dist/ravenlock.js`, `dist/ravenlock.css`: game UI and interactions.
- `dist/ravenlock-engine.js`: state and progression.
- `dist/case-one.js`, `dist/case-two.js`: case content.
- `dist/room-scenes.js`: environmental interaction regions.
- `docs/`: character canon, implementation decisions and master screen inventory.
- `tests/`: narrative, scene and asset checks.
- `dist/legacy/`, `retained/`: earlier prototype material, not canonical progression.

## Checks

```sh
node tests/canon.mjs
node tests/room-scenes.mjs
python3 tests/validate-assets.py
```

## Scope

Cases 01 and 02 are the current playable scope. Case 03 remains on hold. Character canon overrides generated artwork; reconstruction is contextual to the investigation.

Public test build: https://missing-moonstone-mystery.athiramanosh29.chatgpt.site/

GitHub changes do not automatically deploy to that test URL. Publish separately after verification.
