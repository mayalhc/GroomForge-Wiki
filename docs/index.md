# Welcome to GroomForge

For full documentation visit [superhivemarket.com](https://superhivemarket.com/products/groomforge).
<div align="center">
  <iframe width="640" height="360" src="https://www.youtube.com/embed/GdUoXGK6g4E" title="[ Professional Hair Physics for Blender &amp; UE5 | Groomforge Addon Showcase ]" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>


---
## Update News
## 🚀 GroomForge PRO v1.3 Release Notes

### [Bug Fix] Fixed 'Fix & Output Connect' Automation and Clump ID Issues
* **Issue:** Previously, when using the 'Fix' function to automatically generate the node setup, the `clumpid` attribute failed to calculate or apply correctly to the strands.
* **Fix:** Improved the internal logic of the `Fix & Output Connect` feature. The automatically generated `Store Named Attribute (clumpid)` node now properly fetches the `Random Value` data across the Spline domain and maintains a stable connection directly to the `Group Output`. Hair clumping effects will now display accurately per strand.
!(v1.3.0 Update)](assets/clumpid01.png)
---

### 💡 Advanced Styling Tips & Use Cases

#### Procedural Clumping via Voronoi Texture Masking
For advanced styling, explore creative setups beyond the default node setup—such as layering multiple clump attributes for complex braids, realistic flyaways, or stylized layering.
* **Procedural Clumping:** Instead of simple random values, try using a `Voronoi Texture` mapped to the strand positions to generate spatially clustered clump IDs.
* **Realistic Clustering:** By passing the texture color through a `Separate Color` node and scaling it with a `Multiply` math node, you can procedurally group hair strands based on their physical proximity. This creates much more realistic, natural-looking hair clumps and partings.

!(v1.3.0 Update)](assets/clumpid02.png)
---

### 🎬 Showcase: Procedural Clumping in Action
*Procedural Clumping via Voronoi Texture allows you to easily achieve realistic, engine-ready hair clustering.*
!(v1.3.0 Update)](assets/clumpid03.png)
* **Advanced Spatial Clustering:** By driving the `clumpid` attribute with a procedural `Voronoi Texture`, hair strands are automatically clustered based on their 3D proximity rather than simple random generation.
* **Flawless Engine Integration:** As shown in the Unreal Engine viewport debug mode, each distinct color seamlessly visualizes a procedural clump unit. This data-driven approach yields incredibly natural hair breaks, realistic partings, and high-fidelity clumping behavior without any manual grooming overhead.
* **Production-Ready Efficiency:** This setup bridges the gap between Blender's procedural generation and real-time engine shading, giving you complete pipeline control over complex hairstyles.

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
