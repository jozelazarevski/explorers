# explorers

**Shardlands**: a small explore-build-conquer game in a low-poly 3/4 view, drawn only with flat-shaded triangles and boxes. It's one file (`index.html`) with no build step and no dependencies.

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
| Hero Whirlwind | Z (20 s cooldown) | Whirlwind button |
| Gather | Space next to trees, rocks or gold | Tap a tree, rock or gold vein |
| Build | Keys 1–8, then click a green square | Tap a building, then tap a green square |
| Town Hall | H: hire villagers, set jobs | Town button |
| Tech tree | R | Tech tree button |
| Game speed | F cycles 1× / 2× / 4× | Speed button by the minimap |
| Train | V villager · T soldier · Y archer · U knight | Tap a Barracks |
| Attack | Walk up to enemies or click them | Tap enemies |
| Zoom | Mouse wheel or +/− | Pinch or +/− |
| Jump camera | Click the minimap | Tap the minimap |
| Sound on/off | M | Sound button on the pause screen |

- **Difficulty:** pick Relaxed, Normal or Hard on the title screen before starting a new world. It sets how early, how often and how big raids are, when rams join them, how fast camps grow, and your starting resources.
- **Goals:** a chain of 13 goals under the resource bar guides the early game and pays out resources for each one.
- **Market:** the Town Hall trades wood, stone and food for gold and back.
- **Rally points:** set one on a Barracks and new troops march there and hold.
- **Idle villagers:** a chip at the top counts villagers with nothing to do; tap it to select them.
- **Explore:** the map starts in fog. Auto-explore sends your hero to the nearest unexplored edge and any chests or shrines it can see. It stays away from enemy camps and walks home to heal when badly hurt. Moving or tapping the map takes back control. Chests hold loot, maps or a free soldier. Purple shrines make your hero permanently stronger.
- **Villagers:** hire them at the Town Hall and split them between wood, stone, gold and farming. They carry what they gather to the Town Hall or the nearest Lumber Camp, Quarry or Gold Mine, and run home when attacked.
- **Command units separately:** whatever you select takes your orders. Troops sent somewhere hold that spot and fight anything within about 5 tiles. Tap an enemy to attack it, or use Follow hero to regroup. Villagers can be sent to any spot, tree, rock, gold vein or farm.
- **Tap to act:** every building, unit, camp and resource opens a panel with its stats and actions. From there you can upgrade, demolish, train, attack, gather or send a villager.
- **Development tree:** 14 technologies in six branches (Economy, Farming, Defense, Military, Arms, Exploration). Research runs at the Town Hall, one at a time.
- **Upgrades:** buildings go up to level 3 for more output, health and range. Your hero gains experience from fights and levels up.
- **Build:** Farms make food. Lumber Camps and Quarries collect from nearby forest and hills. Gold Mines must touch a gold vein. Houses raise troop capacity. Towers shoot raiders and widen your land. Walls slow raiders down.
- **Conquer:** red camps get tougher the farther they are from home, and the farthest one is a fortress with a warlord. Destroy a camp to claim its land and loot. Take every camp to win.
- **Defend:** after the first nights, camps send raids at your Town Hall. A red chip at the top counts down the last 30 seconds before each raid sets out. Red arrows at the screen edge and red dots on the minimap show where raiders are. From day 4 (on Normal) raids bring battering rams: slow, tough machines that ignore people and smash walls and buildings, so meet them on the road. Every two days (on Normal) the remaining camps grow a level stronger. If your Town Hall falls, the game is over.
- **Sound:** every hit, arrow, harvest, build and fanfare is synthesized in the browser, with no audio files. Sounds fade with distance from the view.
- **Stats:** the pause screen and the end screen show the day, camps taken, enemies defeated, units raised and lost, buildings, resources gathered and treasures found.

Progress saves automatically in your browser.

## Look

The camera looks north from high up. Every face is flat-shaded by one light from the north-west, so the ground is a mesh of lit and shaded triangles, and slopes toward hills and mountains catch or lose the light. Trees, rocks, peaks and buildings stand up out of their tiles and cast short shadows down and to the right. People are seen from above and shaded on the side away from the light as they turn.

## Performance

Terrain, trees, rocks and peaks are drawn once into cached 16×16-tile chunks. Each frame only redraws units, buildings, fog and effects. After a zoom, the old chunks are shown stretched while new ones are drawn a few per frame, so zooming never stalls. The pixel ratio is capped at 1.5×, and each world is 160×160 tiles, so it runs smoothly on modest hardware.

## Publishing

`.github/workflows/pages.yml` deploys `index.html` to GitHub Pages on every push to `main`. Pages has to be switched on once by hand: Settings → Pages → Build and deployment → Source: **GitHub Actions**. On a free account the repository must be public for Pages to be available.
