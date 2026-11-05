# Unreal to Godot Export Guide
### Tools
* [Unreal to Godot Exporter](https://www.fab.com/listings/61983625-664c-4308-9b26-edfd58d41002) ⭐ Recommended
* [UnrealToGodot](https://github.com/vortechU/UnrealToGodot) 🟢 Free 🔴 Cannot export full scenes- individual meshes only.
### Godot Project Settings
* Project Settings ➡️ Rendering ➡️  Lights And Shadows ➡️ Use Physical Light Units
* WorldEnvironment ➡️ Camera Attributes ➡️ CameraAttributesPhysical (or CameraAttributesPractical)
* Camera ➡️ Camera Attributes ➡️ CameraAttributesPhysical (or CameraAttributesPractical)
### Troubleshooting / Solutions
* My lighting is way overlit or looks bad.
  * Unreal uses physical light units by default, godot does not. Follow the Project Settings above and [use this guide](https://docs.godotengine.org/en/stable/tutorials/3d/physical_light_and_camera_units.html)
* Some assets are missing!
  * Unreal to Godot Exporter sometimes has trouble exporting combined Actors.
  * [Unpack Blueprints on Fab](https://www.fab.com/listings/8491266d-c03b-4333-9675-cc8c73c83227) can extract these into their primitives (Actor ➡️ to individual meshes, lights). 
    *  Remember to add `Actor` to `EUBP_UnpackBlueprints` ➡️ `Supported Classes`
    *  Content Browser ➡️ `EUBP_UnpackBlueprints` ➡️ RMB ➡️ Run Editor Utility Blueprint
    *  In Outliner, sort by Type, select all Actors ➡️ RMB ➡️ Scripted Actor Actions ➡️ Unpack Blueprint
* Some polygons are missing!
  * Choose the "Export Original Mesh" option in Godot To Unreal when exporting.
