# Entryfern 1.0 TEST
Native Android Haisu room-entry path puzzle. Android8+ (min26), target35. Package com.gg007.entryfern.

## Rules
Haisu: draw one path from S to G through every cell exactly once, moving only between side neighbors. A cell number N means this cell must be crossed during the Nth entry into its outlined room, not on the Nth step. S counts as the first entry to its room. Moving within a room keeps its count; leaving and returning adds one. Revisit rooms but never cells. This edition has cell visit clues only, no small room-total clues. Tap a neighboring cell to extend; tap the previous cell to step back. Undo/reset/next/levels and saved entry palette/room labels. Twelve unique 4x4 room layouts and unique routes.

## Download and status
https://mega.co.nz/#!ockB0LBb!zg8cSQds_IRBebNk8eg2wKeqmIRTfeiR0CrBBJYyJpU
APK SHA256 ca5c254ab8806fe768516975117c5ddce94af4a9b029a0cfc0aec74d24496d7b; 20974 bytes. Original signing certificate SHA256 1651d9e269ece8a76f36ed4bba24ebc50f9de1e5f856e0567e0e8169fcb25597. Anonymous download bytes match.

## Checks
Independent contiguous-room-run oracle agrees with production incremental entry counters for all25332 simple path prefixes on12boards,60bounds/nullcases and120000invalid/random states. Each board has one solution among all52full Hamiltonian routes from S; room layouts and solutions are all distinct. Each route re-enters at least two rooms, with a visible clue of2or higher. Bounds, invalid levels/arrays, early goal, revisited cells, wrong visit, solved lock, solve/undo/replay/tap-back/reset pass. Actual archived generator regeneration and Java tests pass. Drawing-adapter neighbor step/tap-back/undo, menu/settings/privacy/levels/next and saved preference/completion checks pass. Actual game/solved/menu/settings/privacy/levels drawing pixels inspected, not phone screenshots. Phone runtime, performance and external-browser handoff QA remain incomplete. Signed TEST, not final or Play published.

## Functional difference
Live803-entry registry,124 recovered partial READMEs and semantic review of all150 prior studio cards found no Haisu match. Cloverroad requires a loop visiting each room in one stretch and counts room cells; Springloop balances per-room cell visits between two loops. Entryfern uses a directed all-cell S-to-G path and temporal room-entry ordinals at numbered cells. Returning to a room changes its visit count without revisiting a cell. Known Haisu genre by William Hu/TheGreatEscaper, not a global invention; recovered corpus is partial. Rules https://puzzling.stackexchange.com/questions/48029/haisu-room-count-an-original-grid-logic-challenge https://www.cross-plus-a.com/html/cros7hsu.htm https://puzzles.covering.space/genres/haisu https://ihnnpuzzles.blogspot.com/2019/09/puzzle-66-path-less-traveled.html https://morassgames.com/games/haisu/ .

## Build
JDK17 and AndroidSDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. Board.java embeds generated rooms/clues/goals/solutions. javac -d /tmp/entry-test src/com/gg007/entryfern/Board.java BoardTest.java and java -cp /tmp/entry-test com.gg007.entryfern.BoardTest. bash build.sh creates an unsigned aligned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to private original signing inputs. No credentials in source. Release build settings, signed TEST artifact, not final store release.

## Privacy and branding
Entryfern runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Entry palette, room labels and solved-board marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 icon byte-equal to original. Menu studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and websites
Complete source and APK privately preserved at https://files.instinct.com/mowg1j95r3dk-entryfern-source-archive, including exact cumulative151-card studio and published catalog/studio sources/updater. Repository https://github.com/iLanis-agent/entryfern holds README only; full Git source commit pending. Both website publications checked separately. No Pages settings change or Play rollout. November7,2026.
