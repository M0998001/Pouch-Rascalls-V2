# Pouch Rascalls — Development Roadmap

**Engine:** RPG Maker MZ 1.10.0 (uploaded blank project). **Delivery:** static web export on GitHub Pages, then iPhone Safari / Add to Home Screen.

The PDF game specification describes the *target product*, not currently built features. It also proposes a separate custom WebGL/one-file architecture; the current implementation instead follows the owner's explicit RPG Maker MZ choice. Incompatibilities should be addressed deliberately rather than presenting the old technical plan as complete.

## Phase 1 — Playable opening (prototype ZIP)

- Burrowby Village, Hazel NPC and 3-way starter selection
- Clover Path, 3 wild rascal species, first battles and pouches
- Basic type advantage, HP, leveling, creature party, healing and save data
- Portraits cropped from the supplied concept sheet, original placeholder town/path art
- iOS touch controls, web manifest, initial cache-as-visited service worker
- Publish all original MZ project files and verify on iPhone Safari

**Definition of done:** Start a new game, choose a starter, move to the route, defeat or catch a wild rascal, return to heal, save/reload, and play through GitHub Pages on a real iPhone. The editor ZIP is an initial implementation, not yet fully device-verified.

## Phase 2 — Core progression

- Tamer/rascal data, 10 types, physical/magic/status moves, move sets and abilities
- Proper rascal front/back/follower sprite sheets (instead of portrait cards)
- Pouchdex with first 20 species, 6-creature party and ranch storage
- Mossbrook, first Warden Fern, badge, story quests and guidebook/tutorials
- Work out combat systems and editor tooling before scaling content

## Phase 3 — Raising and ranch

- Mood (0–100), bond (0–255), personalities, care and follower behavior
- Cooking and home after Badge 1
- Breeding and Honor after Badge 2
- Jobs, crafting and Bloom/Feral/Iron branches after Badge 3

## Phase 4 — Hollowvale campaign

- 18 outdoor maps and 37 interiors, full 8-badge arc
- Rival Andrew W., Heidi K., Nightjackals/Rangers factions
- Full 220-entry Pouchdex, 111 moves and six legends
- Clock/seasons/weather, festivals, field skills and fast travel

## Phase 5 — Ship-ready iOS web app

- Touch layouts tested on portrait and landscape iPhone/iPad
- Full offline precaching/update strategy, save-code portability and data migrations
- Performance/quality options and audio resume behavior
- Accessibility, license audit, backups, regression tests and live Pages verification

## Architecture notes

- Keep RPG Maker MZ map/event JSON editable with the RPG Maker editor.
- Keep custom RPG systems in `js/plugins/`, with stable saved-data schema.
- Original concept-card portraits are temporary UI art; MZ sprites require atlas layout.
- Browser hosting requires the complete `index.html` + engine + data + image/audio bundle, not the `.rmmzproject` file alone.
- GitHub Pages is static hosting, not an iOS native App Store build.
