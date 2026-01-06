# ❄️ Belle's Winter Adventure

![Belle's Winter Adventure Papercraft World](papercraft-preview.png)

## 📖 Project Overview
**Belle's Winter Adventure** is a developmentally appropriate Progressive Web Application (PWA) designed for *and with* a 30-month-old toddler. It combines science-backed interaction design (fine motor skill calibration, immediate contingency feedback, and scaffolding) with a local theme (Wisconsin Christmas 2025 with family).

### The Development Journey
This project represents a rapid, iterative development cycle driven by real-world playtesting feedback:
* **Research Phase:** Analysis of neurological capabilities of a 2.5-year-old (symbolic representation, "video deficit" mitigation).
* **Initial Release (v1.0):** Single-file HTML/JS sorting task featuring custom family avatars.
* **The "Papercraft" Evolution (v2.0+):** UI overhauled into a high-contrast "Paper Mario" aesthetic to improve visibility and engagement.
* **Dynamic Expansion:** Engine upgraded to support randomized categories (Faces, Animals, Food, Vehicles) and procedural environments.

---

## 📜 Changelog

### Version 2.1.3 (Current)
* **Polish:** Reduced category zone size by 10% for better screen real estate.
* **Polish:** Lowered maximum ground decoration height to 15% to match terrain.
* **Fix:** Hide active item when entering Parent Mode to prevent UI obstruction.

### Version 2.2 (The Stability Update)
* **CRITICAL:** Refactored drag physics to use `transform: translate3d`.
    * Fixes "Scale Feedback Loop" bug where items drifted left/up on tap.
    * Decoupled visual scale animations from logical coordinate system.
* **Fix:** Attempted fix for drag drift using center-point calculation.

### Version 2.1 (The Papercraft Update)
* **VISUAL OVERHAUL:** Implemented Papercraft Aesthetic.
    * Added global noise texture overlay.
    * Applied white borders and drop shadows to all emojis.
    * Converted background elements to HTML layers for aspect ratio preservation.
* **UX:** Implemented "Instant Success" trigger on drop (removed delay).
* **UX:** Added "Forgiving Drag" logic (400ms grace period on touch loss).
* **Feature:** Added "Chicken Coop" decoration (7 chickens) when Animals active.

### Version 2.0 (Dynamic Categories)
* **Feature:** Dynamic Backgrounds. Scenery now changes based on active categories (e.g., Lake for Animals, Airport for Vehicles).
* **Feature:** Snowstorm Event. Random heavy snow triggers every 3-6 minutes.
* **Feature:** Parent Mode 2.0.
    * Added Category Config UI (Left/Right selection).
    * Added Blocklist functionality (tap emoji to ban).
    * Prevented selecting the same category on both sides.
* **Assets:** Added Nature (Outside) and Shapes categories.
* **Polish:** Connected rainbow emojis in background to form double arch.
* **Fix:** Swapped Lion 🦁 for Lizard 🦎 as Animal icon.
* **Fix:** Removed scary faces (skulls) from Smiley pool.

### Version 1.5 (Refinements)
* **Feature:** Replaced "Box" with "House" emoji + Doorbell sound.
* **Feature:** Strict Parent Mode. Requires 5s hold on Star+Angel with exactly 2 touch points (anti-palm).
* **Feature:** Implemented "Vacuum" success animation (Pop -> Spin -> Shrink).
* **Polish:** Increased gravity radius for drop zones to 250px.
* **Polish:** Increased confetti particle count to 60.

### Version 1.2 (Audio & Physics)
* **Audio:** Switched to Additive Synthesis (3-oscillator triangle wave) for "Wooden Purr" to fix mobile audio issues.
* **Audio:** Added global `touchstart` listener to unlock WebAudio API on iOS.
* **Physics:** Added invisible screen boundaries to prevent throwing items off-screen.
* **Physics:** Implemented circular, oversized hitboxes for toddler fine-motor variance.
* **Polish:** Items now stay in place for 3s after drop before resetting.

### Version 1.1 (The "Beau" Update)
* **Feature:** Added `beau.png` support for Angel icon with fallback.
* **Feature:** Added "Christmas Pickle" easter egg logic (Speech bubble vs Alert).
* **Polish:** Centered game title and added drop shadow.

### Version 1.0 (Initial Release)
* **Feature:** Smart Spawning. Items calculate safe landing Y-pos based on screen aspect ratio.
* **Visuals:** Added organic horizon SVG (curved snow, trees, lake).
* **Audio:** Implemented "Magical Hum" and "Fanfare" synths.
* **Logic:** Added "Success Lock" to prevent double-triggering sounds/spawns.

### Version 0.x (Prototype & Development)
* **Feature:** Added "Idle Wiggle" animation to attract attention.
* **Feature:** Replaced SVGs with Giant Emojis for Home/Tree.
* **Fix:** Fixed touch event cleanup causing game freeze on second item.
* **Feature:** Added "Toy Box" launch physics (Bouncing trajectory).
* **Feature:** Interactive Clouds (Tap to snow).
* **Init:** Initial PWA shell, `manifest.json`, and service worker.
