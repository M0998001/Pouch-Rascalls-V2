# Pouch Rascalls — Hollowvale Beginnings

A cozy creature-taming RPG built with **RPG Maker MZ 1.10.0**, intended for keyboard, touch, and iPhone Safari via GitHub Pages.

## Current status

**Milestone 1 is being developed:** Burrowby Village, Professor Hazel, starter selection (Sprigling / Emberkit / Puddlepip), Clover Path, initial wild battles and catching, and browser/iOS controls. This repository is initialized with documentation and deployment scaffolding; the full RPG Maker game files and art must still be uploaded before GitHub Pages can run the game.

The editable MZ project is supplied separately as a downloadable ZIP in the development conversation. Extract it, open `game.rmmzproject` in RPG Maker MZ, and use Playtest. Its `index.html` is the browser entry point.

## Add the RPG Maker project to this repository

1. Download and extract **PouchRascalls_MZ_Milestone1.zip** from the project conversation.
2. Clone this repository locally with `git clone https://github.com/M0998001/Pouch-Rascalls-V2.git`.
3. Copy the **contents** of the extracted game folder into the repository root (the root must contain `index.html`, `game.rmmzproject`, `data/`, `js/`, `img/`, and `audio/`). Preserve this README and the `.github/` folder.
4. `git add . && git commit -m "Add playable RPG Maker MZ milestone 1" && git push origin main`.
5. In repository **Settings → Pages**, choose **GitHub Actions** as the build/deployment source. The workflow in `.github/workflows/pages.yml` is configured to publish the static game files once `index.html` is present.
6. After deployment, open `https://m0998001.github.io/Pouch-Rascalls-V2/` in iPhone Safari and choose Share → Add to Home Screen.

> RPG Maker MZ itself is required for editing/playtesting within the editor. The published **web build** runs in browsers without installing the editor. Do not publish third-party RTP or art files unless you hold the necessary rights.

## First milestone's scope

- Two illustrated maps and editable RPG Maker events.
- Six rascal reference-card portraits (original starter art supplied by the project owner).
- Starter selection, basic 1-on-1 wild battles with typed attacks, catching, party recovery, and persistence through RPG Maker saves.
- Keyboard controls and added on-screen iOS buttons.
- PWA manifest and a cache-as-visited service worker (not yet guaranteed completely offline from the first launch).

## Long-term vision

The game design document targets Hollowvale's 18 outdoor maps, 37 interiors, 220 Pouchdex entries, 10 types, 8 Warden badges, raising/breeding/ranch systems, Honor, and progression through Champion and postgame. These are **planned**, not completed. See `docs/ROADMAP.md` for the implementation sequence.

## Controls

- **Keyboard:** Arrow keys or WASD to move; Enter/Space/Z to confirm; Esc/X to cancel/menu.
- **Touch:** D-pad, A, B and Menu overlay controls; RPG Maker's built-in taps also work.

## Known limitations

This is an early vertical slice, not the complete design. Battle scenes use reference-card images pending dedicated sprites; the custom combat is a prototype; advanced systems (camera/2.5D, breeding, Warden battles, etc.) have not been built. Confirm actual iOS Safari/PWA behavior on hardware before claiming full iPhone support.
