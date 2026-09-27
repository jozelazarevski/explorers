# explorers

**Shardlands**: a small explore-build-conquer game drawn only with squares and triangles. It's one file (`index.html`) with no build step and no dependencies.

**Play:** open `index.html` in any browser. It works on desktop and on phones.

## How to play

| | Desktop | Touch |
|---|---|---|
| Move | WASD / arrow keys, or click the ground | Tap the ground |
| Auto-explore | X | Auto-explore button |
| Gather | Space next to trees, rocks or gold | Tap a tree, rock or gold vein |
| Build | Keys 1–8, then click a green square | Tap a building, then tap a green square |
| Train | T soldier · Y archer · U knight · I upgrade arms | Buttons above the build bar |
| Attack | Walk up to enemies or click them | Tap enemies |
| Zoom | Mouse wheel or +/− | Pinch or +/− |
| Travel | Click an explored spot on the minimap | Tap the minimap |

- **Explore:** the map starts in fog. Auto-explore sends your hero to the nearest unexplored edge and any chests or shrines it can see. It stays away from enemy camps and walks home to heal when badly hurt. Moving or tapping the map takes back control. Chests hold loot, maps or a free soldier. Purple shrines make your hero permanently stronger.
- **Build:** Farms make food. Lumber Camps and Quarries collect from nearby forest and hills. Gold Mines must touch a gold vein. Houses raise troop capacity. Towers shoot raiders and widen your land. Walls slow raiders down.
- **Conquer:** red camps get tougher the farther they are from home, and the farthest one is a fortress with a warlord. Destroy a camp to claim its land and loot. Take every camp to win.
- **Defend:** after the first nights, camps send raids at your Town Hall. If it falls, the game is over.

Progress saves automatically in your browser.

## Performance

Terrain is drawn once into cached 16×16-tile chunks. Each frame only redraws units, buildings, fog and effects. The pixel ratio is capped at 1.5×, and each world is 160×160 tiles, so it runs smoothly on modest hardware.
