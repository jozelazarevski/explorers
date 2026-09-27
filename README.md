# explorers

**Shardlands**: a small explore-build-conquer game drawn only with squares and triangles. It's one file (`index.html`) with no build step and no dependencies.

**Play:** open `index.html` in any browser. It works on desktop and on phones.

## How to play

| | Desktop | Touch |
|---|---|---|
| Move hero | WASD / arrow keys, or click the ground | Tap the ground |
| Command units | Select them, then click the ground to move or an enemy to attack | Same, with taps |
| Select many | Left-drag a box (Shift adds) | Hold a finger, then drag a box |
| Quick select | E hero · Q whole army | Hero / Army buttons |
| Look around | Right-drag | Drag with one finger |
| Select | Click anything | Tap anything: buildings, units, camps, trees, rocks |
| Auto-explore | X | Auto-explore button |
| Gather | Space next to trees, rocks or gold | Tap a tree, rock or gold vein |
| Build | Keys 1–8, then click a green square | Tap a building, then tap a green square |
| Town Hall | H: hire villagers, set jobs | Town button |
| Tech tree | R | Tech tree button |
| Game speed | F cycles 1× / 2× / 4× | Speed button by the minimap |
| Train | V villager · T soldier · Y archer · U knight | Tap a Barracks |
| Attack | Walk up to enemies or click them | Tap enemies |
| Zoom | Mouse wheel or +/− | Pinch or +/− |
| Jump camera | Click the minimap | Tap the minimap |

- **Explore:** the map starts in fog. Auto-explore sends your hero to the nearest unexplored edge and any chests or shrines it can see. It stays away from enemy camps and walks home to heal when badly hurt. Moving or tapping the map takes back control. Chests hold loot, maps or a free soldier. Purple shrines make your hero permanently stronger.
- **Villagers:** hire them at the Town Hall and split them between wood, stone, gold and farming. They carry what they gather to the Town Hall or the nearest Lumber Camp, Quarry or Gold Mine, and run home when attacked.
- **Command units separately:** whatever you select takes your orders. Troops sent somewhere hold that spot and fight anything within about 5 tiles. Tap an enemy to attack it, or use Follow hero to regroup. Villagers can be sent to any spot, tree, rock, gold vein or farm.
- **Tap to act:** every building, unit, camp and resource opens a panel with its stats and actions. From there you can upgrade, demolish, train, attack, gather or send a villager.
- **Development tree:** 14 technologies in six branches (Economy, Farming, Defense, Military, Arms, Exploration). Research runs at the Town Hall, one at a time.
- **Upgrades:** buildings go up to level 3 for more output, health and range. Your hero gains experience from fights and levels up.
- **Build:** Farms make food. Lumber Camps and Quarries collect from nearby forest and hills. Gold Mines must touch a gold vein. Houses raise troop capacity. Towers shoot raiders and widen your land. Walls slow raiders down.
- **Conquer:** red camps get tougher the farther they are from home, and the farthest one is a fortress with a warlord. Destroy a camp to claim its land and loot. Take every camp to win.
- **Defend:** after the first nights, camps send raids at your Town Hall. If it falls, the game is over.

Progress saves automatically in your browser.

## Performance

Terrain is drawn once into cached 16×16-tile chunks. Each frame only redraws units, buildings, fog and effects. The pixel ratio is capped at 1.5×, and each world is 160×160 tiles, so it runs smoothly on modest hardware.
