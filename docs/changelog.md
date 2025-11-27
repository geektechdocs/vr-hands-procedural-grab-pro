# 🧾 Version History

## 🆕 Version 1.2.4 (Alyx Gravity Pull Update)

- **Improved:**  
  Disabled the speed-drop slow-motion effect when the item gets close to the hand, resulting in a more natural pull finish.  
  *(You can toggle this behavior via `EnableSlowMo` on `ASC_RemoteGrabComponent` in the Details panel.)*

- **Added:**  
  **New Catch Mode selection enum:**
    - **Requires Second Trigger Press** — classic Alyx-style catch.  
    - **Auto Catch When Near Hand** — automatically catches when item reaches the hand. *(Default)*

---

## 🔧 Version 1.2

- Half-Life Alyx-like Gravity Pull mechanic (remote object grab)
- Remote Grab Filter Priority (added enum for procedural grab components)
- Updated `VRHandsProceduralGrab.uplugin`: added  
  **`"PlatformAllowList": ["Win64", "Android"]`**  
  *(Fixes instant crash on Android standalone devices — Quest 2/3)*

---

## 🔧 Version 1.1

- Removed unused Input Context
- Reparented main Player Pawn → Character
- Added extra constraint option for `AttachHandToObject`
- Added locomotion movement (walk forward, left/right)

---

## 🔧 Version 1.0

- Improved finger trace accuracy
- Added VRPrintString system for in-headset debugging
- Optimized physics defaults

---
