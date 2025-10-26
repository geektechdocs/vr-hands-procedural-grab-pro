<!-- index.md - VR Hands Procedural Grab Pro Documentation -->

<h1 style="text-align:center;">VR Hands Procedural Grab Pro Documentation</h1>

<p align="center">
  <a href="ScreenShots/VRHandsProceduralGrabPro.jpg" class="glightbox">
    <img src="ScreenShots/VRHandsProceduralGrabPro.jpg" alt="VR Hands Procedural Grab Pro" style="width:90%; max-width:1100px; display:block; margin:12px auto;">
  </a>
</p>

<p align="center">
  <a href="https://www.youtube.com/watch?v=QFCV_MboX9w" target="_blank" rel="noopener">
    <img src="https://img.shields.io/badge/Watch%20Demo-YouTube-red?logo=youtube&style=for-the-badge" alt="Watch on YouTube">
  </a>
  &nbsp;
  <a href="https://www.fab.com/listings/0d7009c6-ad1b-41d0-96d0-56ae95e59653" target="_blank" rel="noopener">
    <img src="https://img.shields.io/badge/Get%20on%20Fab-VR_Hands_Procedural_Grab_Pro-009688?logo=unrealengine&style=for-the-badge" alt="Get on Fab">
  </a>

</p>

---

## :material-rocket-launch: Quick Start Guide

### :material-cog-outline: Step 1 — Enable Plugin
> :material-arrow-right-bold-outline: **Plugins → Enable Plugin**  
> <a href="ScreenShots/EnablePlugin.jpg" class="glightbox">
>   <img src="ScreenShots/EnablePlugin.jpg" alt="Enable Plugin screenshot" style="display:block; margin:8px auto; width:90%; max-width:900px;">
> </a>

---

### :material-cog-outline: Step 2 — Input Setup

1. Move plugin's Input Folder **`Plugins/VRHands:ProceduralGrabProContent/Input`** → into your **game project's `Content`** folder.  

!!! warning "This step is required"
    Any input context used by the **Enhanced Input** system **must** be placed inside your game's **Content** folder.  
    Plugin content is not packaged the same way and will not be discovered in packaged builds, which will cause inputs to stop working after packaging.

<a href="ScreenShots/MoveInputToContent.jpg" class="glightbox">
  <img src="ScreenShots/MoveInputToContent.jpg"
       alt="Move Input to Content"
       style="display:block; margin:8px auto; width:90%; max-width:900px;">
</a>


---

### :material-cog-outline: Step 2.1 — For UE 5.2
1. Search for **PMI** in Project Settings.  
2. Set **Mappable Input Config For XR** to `PMI_VRTemplateProcedural`.

<a href="ScreenShots/InputUE5.2PMI.jpg" class="glightbox">
  <img src="ScreenShots/InputUE5.2PMI.jpg" alt="UE5.2 PMI" style="display:block; margin:8px auto; width:80%; max-width:800px;">
</a>

---

### :material-cog-outline: Step 2.1 — For UE 5.3–5.6
1. Search Project Settings for **Input** → **Default Mapping Contexts**.  
2. Add 3 array items and set:
   - `IMC_ProcGrab_Hand`
   - `IMC_ProcGrab_Weapon_Left`
   - `IMC_ProcGrab_Weapon_Right`

<a href="ScreenShots/InputforUE5.3-5.6.jpg" class="glightbox">
  <img src="ScreenShots/InputforUE5.3-5.6.jpg" alt="Input contexts" style="display:block; margin:8px auto; width:80%; max-width:800px;">
</a>

---

### :material-dock-window: Step 3 — Open Example Map
Open: **Plugins/VRHands:ProceduralGrabProContent/Example_Map**

<a href="ScreenShots/OpenLevel.jpg" class="glightbox">
  <img src="ScreenShots/OpenLevel.jpg" alt="Open Example Map" style="display:block; margin:8px auto; width:90%; max-width:900px;">
</a>

---

## :material-cog-outline: Setting Custom Hands Mesh

1. Open **BP_VRPawnProcedural**.  
2. Select **B_HandMesh_r** component.  
3. Set enum **Hand Mesh Visual Settings** → **Show Custom Hand** and choose your right-hand skeletal mesh.  
4. Repeat for **B_HandMesh_l** to set the left hand.

<a href="ScreenShots/SettingCustomHands.jpg" class="glightbox">
  <img src="ScreenShots/SettingCustomHands.jpg" alt="Settings Custom Hands" style="display:block; margin:8px auto; width:90%; max-width:900px;">
</a>

---

## :material-gift: Get Human Hands — FREE (How to claim)

<a href="ScreenShots/HandsPromo.gif" class="glightbox">
  <img src="ScreenShots/HandsPromo.gif" alt="Human Hands animation" style="width:90%; max-width:900px; display:block; margin:8px auto;">
</a>

You can receive the **Human Hands** mesh pack for free by following these steps:

1. **Rate the product on** [**Fab**](https://www.fab.com/listings/0d7009c6-ad1b-41d0-96d0-56ae95e59653)

2. **Write a few words (feedback) on the** [**Fab Forum**](https://forums.unrealengine.com/t/geektech-vr-hands-procedural-grab-pro/2668162)

3. **Contact me to confirm:** [geektechcg@gmail.com](mailto:geektechcg@gmail.com)  
   or send a [direct message](https://forums.unrealengine.com/u/iD.P/summary) on the forum.  
   Don’t forget to include your **forum username**.

> **After confirmation**, I’ll provide the download link for the Human Hands pack.  

---

### Troubleshooting & Tips

??? tip "Input not detected in packaged game?"
    - Make sure the **Input** folder was moved into your **game project's `Content`** folder (not left inside the plugin).
    - Check Project Settings → Input to ensure the mapping contexts are listed.
    - Review [Step 2 — Input Setup](#step-2-input-setup)

---

## :material-email-outline: Need Help?

Contact: [GeekTech](mailto:geektechcg@gmail.com)  
Plugin listing / updates: <https://www.fab.com/listings/0d7009c6-ad1b-41d0-96d0-56ae95e59653>

---

<small>
Plugin is developed and maintained by GeekTech. Compatible with Unreal Engine **5.2 – 5.6**.
</small>

---

*Ready to supercharge your VR Project? Get [**VR Hands Procedural Grab Pro**](https://www.fab.com/listings/0d7009c6-ad1b-41d0-96d0-56ae95e59653) now!*
