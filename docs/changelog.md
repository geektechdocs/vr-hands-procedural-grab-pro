# 🧾 Version History

## 🆕 Version 1.2.7

**Added / Improved / Fixed**

- **Added:** `ChangeCollisionOnPhysicsBody` helper to update collision settings for a specific physics body (bone).

- **Fixed:** Finger–surface collision loss after turning or teleporting.  
  Physics blend weight is now enforced as **1**, removing the need to re-trigger fist input.

- **Improved:** **Attach Hand To Object** no longer disables physics.

- **Fixed:** Left-hand **Layered Blend Per Bone** setup typo  
  (blend depth **0 → 3**).

- **Improved:** Demo VRPawn movement tuning — braking deceleration reduced  
  **2048 → 512** for smoother motion.

- **Fixed:** Visible hand pop when disabling physics (`PausePhysSim`) by caching and restoring the hand transform after reattachment.

- **Added:** Per-component **Grab Mode Override** *(ProceduralGrabComponent)*  
  - `bOverrideGrabMode`  
  - `GrabMode (EGrabHandMode)`  
  Allows overriding Data Asset grab behavior, including multi-hand grab control.

- **Added:** **Custom Animation Pose Override** *(ProceduralGrabComponent)*  
  - `bOverrideAnimPose`  
  - `OverrideAnimPoseSequence (UAnimSequenceBase*)`  
  Custom poses can be applied on grab or dynamically during overlap events.

- **Improved:** Trigger finger tracing — reduced trace length for better collision accuracy.

- **Added:** **Custom Pose Editor Mode** *(ProceduralGrabComponent)*  
  Hand poses can now be manually edited and saved as Anim Sequences.

- **Added:** `FistFormingAlphaMultiplier` *(B_HandMeshComponent)*  
  Limits finger curl strength (useful for thick or restrictive gloves).

- **Added:** `bSkipTwoHandedGrabLogic` *(ProceduralGrabComponent)*  
  Allows secondary hand grips without applying two-handed constraints  
  (e.g. off-hand weapon grips).


## 🆕 Version 1.2.4 
(Alyx Gravity Pull Update)
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
