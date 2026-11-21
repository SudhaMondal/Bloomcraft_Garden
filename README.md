# Bloomcraft_Garden

# 🌸 BloomCraft: 4-Garden Explorer & World Flora Cards

> **Not Just a Garden but a Garden ❤️**

---

## 👋 Welcome, Player

¡Hola, Explorer! Step into **BloomCraft**, a 3D voxel survival and gardening sandbox where Minecraft-style building and crafting meet Dora-inspired expeditions and Pokémon-style plant card collecting. Whether you're tilling hydrated farmland in the Central Meadow, dodging falling pink petals in the Sakura Grove, admiring cacti in the Desert Oasis, or brewing herbal tea inside the Glass Greenhouse, there's always a new plant to discover.

---

## 💡 Why I Built It

I wanted to create a cozy, collaborative web game that anyone can play instantly in their browser—no downloads, no installs, and no complicated setup. Beyond relaxing voxel gardening, I wanted players to learn real-world botanical facts (like Latin names, native biomes, and plant adaptations) while enjoying the thrill of collecting rare cards, trading with friends, and exploring as a 3D character.

---

## 🛠️ Technologies Used

| Technology | Role in BloomCraft |
| :--- | :--- |
| **HTML5 & Vanilla JavaScript** | Core game loop, voxel world state, physics, crafting, and persistence (`localStorage`) |
| **Three.js (`r128`)** | 3D voxel rendering, dynamic day/sunset/night lighting, shadows, clouds, stars, and VFX |
| **Tailwind CSS (`3.4.17`)** | Responsive HUD, hotbar, Pokémon-style card binder, crafting table, and modals |
| **Web Audio API** | Procedural sound effects (planting, digging, water splashes, chimes, and celebration fanfare) |
| **GitHub Pages** | Zero-cost static hosting so any visitor or collaborator can play live from a single `index.html` |

---

## ⚙️ Core Features & Mechanics

- **3D Explorer Character (3rd & 1st Person):** Play as an animated 3D voxel explorer complete with an explorer hat, purple backpack, swinging limbs, and held tools—toggle anytime between 3rd-person orbit and 1st-person view.
- **4 Distinct Garden Biomes (40×40 World):**
  - **Central Meadow & Whispering Pond:** Starter turf, oak trees, and fertile soil.
  - **Sakura Blossom Grove:** Pink cherry blossom trees with drifting petal VFX and garden lanterns.
  - **Desert Oasis:** Warm sand dunes, 3D Saguaro Cacti, and an oasis pool.
  - **Glass Greenhouse & Starlight Garden:** Transparent glass dome with beehives and glowing Moonlight Lilies.
- **Minecraft-Style Survival & Crafting:** Mine Coal Ore, Iron Ore, Stone, and Wood; smelt Iron Ingots and Greenhouse Glass in the Furnace; craft tiered Pickaxes, Axes, Hoes, Swords, and Torches; and manage Health & Hunger.
- **Botanical Cross-Breeding & Irrigation:** Till soil with a Hoe near Water to create **Hydrated Farmland** (2.5× faster growth) and cross-pollinate adjacent blooms into rare hybrids.
- **Dora-Inspired Expedition Twist:** Follow **The Map's** 3-stop quest, carry gear in **Backpack**, receive apples from **Boots** the monkey companion, and stop **Swiper the Fox** before he swipes a bloom!
- **16 Pokémon-Style World Flora Cards:** Unlock cards with rarity tiers (*Common*, *Uncommon*, *Rare*, *Legendary*), Power/Hydration/Resilience stats, scientific names, and real botanical facts.

---

## 🎮 What Users Can Do

- **Create an Explorer Gaming ID:** Pick an avatar and custom handle (e.g., `Maya#4821`) saved in your browser.
- **Plant, Water & Harvest:** Grow 8 flower species from Seedling → Budding → Full Bloom, and harvest blooms for extra seeds, XP, and collectible cards.
- **Trade Plant Cards:** Swap duplicates at the **Expedition Trade Post** (with Dora, Boots, or Prof. Flora) or generate shareable `TRADE-...` codes to exchange cards with friends.
- **Collaborate in Groups:** Create or join a Group Code and merge **Group Garden Snapshots** so teammates can combine their planted flowers and discoveries into one shared world.
- **Switch Modes Anytime:** Play in **Survival Mode** for resource gathering and night slime defense, or toggle **Creative Mode** and **Fly Mode** for pure architectural and garden design.

---

## ⌨️ Keyboard Shortcuts & Controls

| Action | Keyboard / Mouse | Mobile / Touch |
| :--- | :--- | :--- |
| **Walk / Sprint** | `W` `A` `S` `D` or Arrow Keys (+ `Shift` to sprint) | On-screen D-Pad (`🕹️`) |
| **Jump / Fly Up** | `Space` | `JMP` button |
| **Look Around** | Click & Drag (or Double-Click for FPS Lock) | Drag anywhere on screen |
| **Mine / Harvest / Attack** | `Q` (or Left-Click in Mine mode) | `⛏️ Mine / Attack` button |
| **Plant / Till / Place / Eat** | `E` or Right-Click (or Left-Click in Use mode) | `🌱 Use / Place` button |
| **Toggle 3rd / 1st Person** | `R` | `📷 3rd` HUD button |
| **World Flora Cards & Trade** | `K` | `🃏 Cards` HUD button |
| **Explorer ID & Group Hub** | `G` | `👥 Group` HUD button |
| **The Map (3-Stop Quest)** | `M` | `🗺️ Map` HUD button |
| **Purple Backpack (Inventory)** | `I` | `🎒 Bag` HUD button |
| **Crafting & Furnace** | `C` | `⚒️ Craft` HUD button |
| **Stop Swiper** | `V` | Tap the Swiper Alert banner |
| **Toggle Fly Mode** | `F` | `🕊️` HUD button |
| **Select Hotbar Slot** | `1` – `9` or Mouse Wheel | Tap hotbar slot |

---

## 🏗️ How I Built It

1. **Zero-Dependency Single-File Architecture:** Everything—3D geometry, procedural 16×16 pixel-art canvas textures, Web Audio sound synthesis, UI modals, and state persistence—lives inside one self-contained `index.html` file.
2. **Procedural Pixel Textures & Voxel Meshing:** Instead of loading external image files that can fail or lag, every block texture (grass, ores, wood, sakura blossoms, glass) is generated dynamically on an offscreen `<canvas>` with `THREE.NearestFilter` for crisp voxel edges.
3. **Hybrid Input System:** Built dual raycasting (mouse cursor raycasting when unlocked + center-screen raycasting in Pointer Lock) plus auto-step collision so players never get stuck on 1-block hills, whether on desktop, trackpad, or mobile.
4. **Static-First Collaboration:** Designed Base64 `TRADE-...` codes and JSON Group Garden Snapshots so players can share cards and merge gardens without needing a paid backend server.

---

## 📚 Learnings

- **Iframe & Browser Compatibility Matters:** Pointer Lock can be restricted in embedded previews, so pairing drag-to-look, cursor raycasting, and an on-screen D-pad makes a 3D game playable everywhere.
- **Auto-Step Movement Changes Everything:** Adding smooth 1-block step-up collision immediately makes voxel exploration feel fluid instead of frustrating.
- **Procedural Assets Keep Hosting Effortless:** Generating textures and sound effects in code keeps the entire project in a single `index.html` that deploys on GitHub Pages in seconds.

---

## 🚀 Future Expansion

- **Real-Time Multiplayer Rooms:** Add WebRTC or WebSocket sync so group members can see each other's 3D Explorers walking and planting live.
- **More Biomes & Seasons:** Introduce an Alpine Snow Peak, Tropical Coral Reef, and dynamic seasonal weather cycles.
- **Custom Explorer Skins & Hats:** Let players unlock new outfits and flower crowns as they complete their World Flora Card Binder.

---

## ▶️ How to Run the Game

### Option 1: Play Live on GitHub Pages
Open the live GitHub Pages link for this repository (`https://sudhamondal.github.io/Bloomcraft_Garden/`) in any modern browser—no installation required!

### Option 2: Run Locally
1. Download or clone this repository.
2. Open `index.html` directly in Chrome, Edge, Firefox, or Safari—or start a quick local server:
   ```bash
   python3 -m http.server 8000
