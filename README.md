# explorers

**Shardlands**: a small explore-build-conquer game in a low-poly 3/4 view, drawn only with flat-shaded triangles and boxes. It's one file (`index.html`) with no build step and no dependencies.

**Play:** https://jozelazarevski.github.io/explorers/, or open `index.html` in any browser. It works on desktop and on phones.

## How to play

You are the lord. You rule from your keep: villagers gather, scouts explore, and the army fights on your orders. The camera stays on your realm instead of chasing anyone around.

| | Desktop | Touch |
|---|---|---|
| Look around | WASD / arrow keys or right-drag | Drag with one finger |
| Back to your keep | Space | Home button |
| Select | Click anything | Tap anything: buildings, units, camps, trees, rocks |
| Send the army | Click an enemy camp, then Send the army | Same, with taps |
| Command units | Select them, then click the ground to move or an enemy to attack | Same, with taps |
| Select many | Left-drag a box (Shift adds) | Hold a finger, then drag a box |
| Quick select | Q whole army · E your lord | Army / Lord buttons |
| Your lord | Select them, then click where to ride or an enemy to charge; Z Whirlwind | Same, with taps |
| Send a scout | X | Scout button |
| Build | Keys 1–8, then click a green square | Build, pick a building, then tap a green square |
| Town Hall | H: hire villagers and scouts, set jobs, trade | Town button |
| Tech tree | R | Tech button |
| Game speed | F cycles 1× / 2× / 4× | Speed button by the minimap |
| Train | V villager · T soldier · Y archer · U knight | Tap a Barracks |
| Zoom | Mouse wheel or +/− | Pinch or +/− |
| Jump camera | Click the minimap | Tap the minimap |
| Sound on/off | M | Sound button on the pause screen |

- **Difficulty:** pick Relaxed, Normal or Hard on the title screen before starting a new world. It sets how early, how often and how big raids are, when rams join them, how fast camps grow, and your starting resources.
- **Goals:** a chain of 14 goals under the resource bar guides the early game and pays out resources for each one.
- **Market:** the Town Hall trades wood, stone and food for gold and back.
- **Rally points:** set one on a Barracks and new troops march there and hold.
- **Idle villagers:** a chip at the top counts villagers with nothing to do; tap it to select them.
- **Scouts:** the map starts in fog. You begin with one scout, and more can be sent from the Town Hall. Each rides on its own to the nearest unexplored edge or treasure, spreads out from the others, keeps away from enemy camps and runs home to heal when anything hurts it. Chests hold loot, maps or a free soldier. Purple shrines make your lord permanently stronger.
- **Villagers:** hire them at the Town Hall and split them between wood, stone, gold and farming. They carry what they gather to the Town Hall or the nearest Lumber Camp, Quarry or Gold Mine, and run home when attacked.
- **War:** tap an enemy camp or raider and choose Send the army. Your troops march out, deal with defenders on the way, take the camp and come home to guard your lord. Or ride out yourself.
- **Command units separately:** whatever you select takes your orders. Troops sent somewhere hold that spot and fight anything within about 5 tiles. Tap an enemy to attack it, or use Back to the lord to regroup. Villagers can be sent to any spot, tree, rock, gold vein or farm.
- **Tap to act:** every building, unit, camp and resource opens a panel with its stats and actions. From there you can upgrade, demolish, train, send the army or send a villager.
- **Development tree:** 14 technologies in six branches (Economy, Farming, Defense, Military, Arms, Exploration). Research runs at the Town Hall, one at a time.
- **Your lord:** wears the crown and stays at the keep, where the troops guard them. Select them to ride out or lead a charge; they ride home once the fight is won. They gain experience from battles near them and from every camp you take.
- **Upgrades:** buildings go up to level 3 for more output, health and range.
- **Build:** Farms make food. Lumber Camps and Quarries collect from nearby forest and hills. Gold Mines must touch a gold vein. Houses raise troop capacity. Towers shoot raiders and widen your land. Walls slow raiders down.
- **Conquer:** red camps get tougher the farther they are from home, and the farthest one is a fortress with a warlord. Destroy a camp to claim its land and loot. Take every camp to win.
- **Defend:** after the first nights, camps send raids at your Town Hall. A red chip at the top counts down the last 30 seconds before each raid sets out. Red arrows at the screen edge and red dots on the minimap show where raiders are. From day 4 (on Normal) raids bring battering rams: slow, tough machines that ignore people and smash walls and buildings, so meet them on the road. Every two days (on Normal) the remaining camps grow a level stronger. If your Town Hall falls, the game is over.
- **Sound:** every hit, arrow, axe blow, build and fanfare is synthesized in the browser, with no audio files. Sounds fade with distance from the view.
- **Stats:** the pause screen and the end screen show the day, camps taken, enemies defeated, units raised and lost, buildings, resources gathered and treasures found.

Progress saves automatically in your browser.

## On phones

- One row of seven icon buttons along the bottom: Town, Scout, Army, Lord, Home, Tech and Build. Build opens a tray of buildings above the row and closes it again.
- The top bar keeps to one line per row, and the goal fits on one line. Tap the goal to read it in full.
- Tapping something opens its panel as a sheet above the buttons. Units are easier to hit with a finger than with a mouse.
- The view is framed between the top bar and the buttons, in portrait and landscape, around notches and home bars.
- The how-to-play list shows touch instructions instead of keys.
- Add it to your home screen (Share → Add to Home Screen on iPhone, or Install app in Chrome) and it runs full screen, without the browser bars.

## Look

The camera looks north from high up. Every face is flat-shaded by one light from the north-west, so the ground is a mesh of lit and shaded triangles, and slopes toward hills and mountains catch or lose the light. Trees, rocks, peaks and buildings stand up out of their tiles and cast short shadows down and to the right. People are seen from above and shaded on the side away from the light as they turn.

## Performance

Terrain, trees, rocks and peaks are drawn once into cached 16×16-tile chunks. Each frame only redraws units, buildings, fog and effects. After a zoom, the old chunks are shown stretched while new ones are drawn a few per frame, so zooming never stalls. The pixel ratio is capped at 1.5×, and each world is 160×160 tiles, so it runs smoothly on modest hardware.

## Publishing

`.github/workflows/pages.yml` deploys `index.html`, `manifest.webmanifest` and the `icon-*.png` home-screen icons to GitHub Pages on every push to `main`. Pages has to be switched on once by hand: Settings → Pages → Build and deployment → Source: **GitHub Actions**. On a free account the repository must be public for Pages to be available.
