# Welcome to GroomForge

For full documentation visit [superhivemarket.com](https://superhivemarket.com/products/groomforge).
<div align="center">
  <iframe width="640" height="360" src="https://www.youtube.com/embed/GdUoXGK6g4E" title="[ Professional Hair Physics for Blender &amp; UE5 | Groomforge Addon Showcase ]" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


---
## Update News

## 🚀 Version 1.4.0 Update

### New Features & Improvements
*   **🆕 Send to Unreal Engine (Beta)**  
    A brand-new one-click bridge between Blender and a running Unreal Engine Editor. Instead of manually exporting an Alembic file and importing it in UE by hand, just click **Send to Unreal Engine** — GroomForge exports your hair and automatically creates the Groom asset inside UE for you, no file dialogs or manual import steps required.
    - Works when Blender and Unreal Engine are running on the **same computer**.
    - Requires a one-time setup in UE: enable the **Python Editor Script Plugin** and turn on **Enable Remote Execution** in Editor Preferences (see the User Guide for the exact steps).
    - You can choose the **UE Folder** and **Asset Name** directly from the Blender panel, so the imported Groom asset lands exactly where — and named however — you want.
    - After the first successful send, repeated sends to the same UE session are much faster, since GroomForge remembers the connection for the rest of your Blender session.

*   **🆕 Smarter, More Natural Clump Grouping**  
    The auto-generated “clumpid” attribute (created by **Fix & Output Connect**) now groups strands by their actual 3D position instead of just their internal list order, so strands that are physically close together now share the same clump ID — giving a much more natural, bundled look. A new **Clump Scale** slider next to the **Fix & Output Connect** button lets you control how large or small the clumps are.

*   **🆕 Richer Unreal Groom Data on Export**  
    Groom Export now includes extra guide-interpolation data (`groom_closest_guides` / `groom_guide_weights`) and standard Groom version info, giving Unreal Engine more information to interpolate your strands from the guides more accurately.

*   **🆕 Force UE Scale Option**  
    A new **Force UE Scale (100x)** checkbox in Hair Rig Prop Creator lets you manually force the correct scale compensation for Unreal-style (centimeter) armatures, in case it isn't detected automatically.

### Bug Fixes
*   **Fixed:** Hair bones could be generated in the reversed direction when using Guide Curves in Hair Rig Prop Creator.
*   **Fixed:** Generated hair meshes/tubes could come out **100x too large** when targeting an Unreal-scaled (centimeter) Armature.
*   **Fixed:** The auto-generated “roughness” attribute could end up as a single identical value across the whole hair system instead of varying naturally per strand.
*   **Fixed:** Groom Export could fail unexpectedly in certain setups — export is now more robust and reliable.
*   Cleaned up a couple of unused leftover buttons in the UV Color Packer panel for a tidier UI.
*   General performance improvement for the Wiggle Hair Sync bridge in scenes with many objects.

---

## 🚀 Version 1.2.0 Update

### New Features & Improvements
*   **🆕 Edge-to-Rig Generation**  
    You can now generate professional rig structures directly from **selected edges** in Object Edit Mode. This allows for more flexible and custom skeleton layouts beyond standard curves.

*   **⚡ Enhanced Color UV Packing**  
    The Color UV Pack engine has been overhauled for **better precision and faster processing**. It ensures UV islands are snapped to color blocks more accurately with significantly reduced calculation time.
    
*   **🎮 Unreal Engine Pipeline Optimization**  
    Automatically generates UE-compatible attributes (UV Maps, Color Attributes, and Vertex Data) during hair card creation. This ensures a seamless transition to Unreal's hair shaders with pre-configured data such as Flow maps, Gradient groups, and Occlusion variations.

### Bug Fixes & Optimization
*   Improved internal logic for UV tile group distribution.
*   Minor UI/UX refinements for the property panels.

### 🔄 Advanced Binding System
*   **🆕 Hair Curve-to-Mesh Bind**  
    A specialized solution to bind Hair Curves to mesh data. This ensures hair follows complex character movements perfectly, overcoming the native limitation where curves cannot be directly influenced by an Armature.

*   **🆕 Mesh-to-Rig Bind**  
    Streamlined workflow to bind meshes to rigs (armatures). This feature optimizes the connection between your generated props and the skeletal system for stable animation.
