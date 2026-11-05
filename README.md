# Unreal to Godot Export Guide
### Tools
* [Unreal to Godot Exporter](https://www.fab.com/listings/61983625-664c-4308-9b26-edfd58d41002) ⭐ Recommended
* [UnrealToGodot](https://github.com/vortechU/UnrealToGodot) 🟢 Free 🔴 Cannot export full scenes- individual meshes only.
### Troubleshooting
* My lighting is way overlit or looks bad.
  * Unreal uses physical light units by default, godot does not: [Follow this guide](https://docs.godotengine.org/en/stable/tutorials/3d/physical_light_and_camera_units.html) 
### Project Settings
* Project Settings ➡️ Rendering ➡️  Lights And Shadows ➡️ Use Physical Light Units
* Camera ➡️  Attributes ➡️ CameraAttributesPhysical (or CameraAttributesPractical)
* WorldEnvironment ➡️  Attributes ➡️ CameraAttributesPhysical (or CameraAttributesPractical)
