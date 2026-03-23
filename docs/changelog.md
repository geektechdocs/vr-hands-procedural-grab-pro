## VR Hands Procedural Grab Pro

# 🧾 Version History

### 🔧 Version 1.3.0
For compatibility with [climbing addon](climbingAddon.md) (physics will not be enabled for static mesh actors on grab)

### 🔧 Version 1.2.10

- Fixed input turn issue on Vive controllers

- Fixed HandMeshOnGrabbed delegate not firing correctly

    Delegate is now properly broadcast with valid references (HandMeshComponent, MotionController, GrabbedItem)

Delegate fix in this update is crucial for proper functionality of the upcoming [VRHPG Pro Climbing add-on](climbingAddon.md)

### 🔧 Version 1.2.9
- Fixed: Now Hand Physics is enabled on begin play by default

- Fixed: In Grab Component details bOverwriteBoneAttachment is now displayed correctly. Before it was hidden due the incorrect Category specified

### 🔧 Version 1.2.8

- Fixed: Now Hand Physics is enabled on begin play by default

- Fixed: In Grab Component details bOverwriteBoneAttachment is now displayed correctly. Before it was hidden due the incorrect Category specified

### 🔧 Version 1.2.7

<iframe width="560" height="315" src="https://www.youtube.com/embed/AJoeABHaitQ?si=vvJGSHLzXkzHRdNu" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
  
- **Improved:** Physics substepping tuned for better performance (runtime-only).  
  Defaults are applied in `VRHandsProceduralGrab.cpp`:
  ```cpp
  PS->bSubstepping        = true;
  PS->MaxSubstepDeltaTime = 0.0083f;
  PS->MaxSubsteps         = 6;
  ```


  

---

### 🔧 Version 1.2.6

**Added:**

- **Collision Safety Fallback**  
  Added an extra safety check to ensure fallback to blocking collision when an item is released.  
  Fixes rare cases where quickly grabbing and releasing an item could temporarily remove hand–world collision.

- **Attachment Bone Rule Flexibility** *(ProceduralGrabComponent)*  
  Added `bOverwriteBoneAttachment` and `SKAttachmentBone`.  
  When enabled, the specified bone overrides the attachment bone defined in the Data Asset.

- **Added:** Snap Turn support.

---

### 🔧 Version 1.2.4 
(Alyx Gravity Pull Update)
- **Improved:**  
  Disabled the speed-drop slow-motion effect when the item gets close to the hand, resulting in a more natural pull finish.  
  *(Toggle via `EnableSlowMo` on `ASC_RemoteGrabComponent`.)*

- **Added:**  
  **New Catch Mode selection enum:**
  - **Requires Second Trigger Press** — classic Alyx-style catch  
  - **Auto Catch When Near Hand** — automatically catches when item reaches the hand *(default)*

---

### 🔧 Version 1.2.0

- Half-Life Alyx–style Gravity Pull mechanic (remote object grab)
- Remote Grab Filter Priority enum (procedural grab components)
- Updated `VRHandsProceduralGrab.uplugin`:  
  **`"PlatformAllowList": ["Win64", "Android"]`**  
  *(Fixes instant crash on Android standalone devices — Quest 2/3)*

---

### 🔧 Version 1.1.0

- Removed unused Input Context
- Reparented main Player Pawn → Character
- Added extra constraint option for `AttachHandToObject`
- Added locomotion movement (walk forward, left/right)

---

### 🔧 Version 1.0.0

- Improved finger trace accuracy
- Added VRPrintString system for in-headset debugging
- Optimized physics defaults
