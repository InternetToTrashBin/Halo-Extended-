Bring back the classic Android 4.4 KitKat look with this custom mod of the iconic Holo Spiral live wallpaper, updated with new color changes and tweaked to run smoothly on modern phones and tablets.
This project was built and modified with the help of Claude AI, which assisted with updating the legacy code, adjusting the color palette, and repackaging the APK so it installs without hassle on newer Android versions.
What's inside:
• Custom color changes: Freshly tweaked colors layered over the classic glowing 3D spiral animation.
• Built with Claude AI: Legacy Android 4.4 compatibility fixes, manifest updates, and packaging assisted by Claude.
• Clean & lightweight: Just the live wallpaper—no ads, no tracking, and no extra permissions.
Version: 1.0
How to set it:
1. Install the .apk file on your device.
2. Open your phone's Wallpaper settings and go to Live Wallpapers.
3. Pick the Holo Spiral wallpaper and tap Set Wallpaper.
 read this too: # Holo Extended Plus - Full Source Code & Preservation Archive

*Collaboratively reconstructed via Claude and Gemini AI assistance.*

## Project Overview
This project contains the complete, clean source code and asset bundle for **Holo Extended Plus**, the classic RenderScript live wallpaper. 

*Note on Architecture & Compatibility:* 
* **Scrapped Container Architecture:** Initial explorations involving a custom `.haloext` file-importing container system were **scrapped**. Inspection of the APK's internal structure (`classes.dex`, `AndroidManifest.xml`, and `META-INF/`) revealed that the engine relies strictly on standard Android live wallpaper service bindings, native RenderScript bytecode (`holo_spiral.bc`), and compiled GLSL shader pipelines[span_0](start_span)[span_0](end_span). 
* **Broken Original APK:** On modern Android versions (Android 12+), the original live wallpaper APK fails and appears completely broken because Google officially deprecated and removed the **RenderScript** runtime from the OS. This repository preserves the source for historical and educational analysis.

## Project Structure
* **`app/src/main/java/com/android/wallpaper/holospiral/`**
  * `HE.java`: Token replacement engine (`@H@`, `@S@`, `@B@`, `@Z@`, `@G@`, `@R@`, `@K@`, `@C@`), `SharedPreferences` configuration handler, and preset manager (featuring all 8 built-in presets: *Original*, *Ocean*, *Forest*, *Neon rainbow*, *Mono*, *Dusk*, *Big glow*, and *Bright background*).
  * `HoloSettings.java`: Settings activity hosting the 8 parameter sliders (*Hue*, *Saturation*, *Brightness*, *Point size*, *Glow*, *Rainbow*, *Background*, and *Gamma*) and preset triggers.
  * `HoloSpiralRS.java`: RenderScript initialization, GLSL program compilation, background gradient mesh, and inner/outer spiral geometry generation.
  * `HoloSpiralWallpaper.java`, `HoloSpiralView.java`, & `HoloSpiralTestActivity.java`: Live wallpaper service bindings, `RSSurfaceView` renderer wrapper, and touch-drag preview activity.
  * `ScriptC_holo_spiral.java`, `ScriptField_VertexColor_s.java`, & `ScriptField_VertexShaderConstants_s.java`: RenderScript bitcode bindings and vertex data structures.

* **`app/src/main/res/`**
  * `raw/`: Compiled RenderScript bitcode (`holo_spiral.bc`) and exact GLSL vertex/fragment shaders (`fragment_background.glslf`, `fragment_geometry.glslf`, `vertex_background.glslv`, `vertex_geometry.glslv`)[span_1](start_span)[span_1](end_span).
  * `drawable/`: Particle point texture (`points_red_green.png`) and wallpaper picker thumbnail (`wallpaper_thumb.png`)[span_2](start_span)[span_2](end_span).

## Requirements
* **Android Studio / Gradle** (Compile SDK 33, Min SDK 14)
* Support for legacy RenderScript runtime
# Holo Extended Plus - Full Source Code & Preservation Archive

*Collaboratively reconstructed via Claude and Gemini AI assistance.*

## Project Overview
This project contains the complete, clean source code and asset bundle for **Holo Extended Plus**, the classic RenderScript live wallpaper. 

*Note on Architecture & Compatibility:* 
* **Scrapped Container Architecture:** Initial explorations involving a custom `.haloext` file-importing container system were **scrapped**. Inspection of the APK's internal structure (`classes.dex`, `AndroidManifest.xml`, and `META-INF/`) revealed that the engine relies strictly on standard Android live wallpaper service bindings, native RenderScript bytecode (`holo_spiral.bc`), and compiled GLSL shader pipelines[span_0](start_span)[span_0](end_span). 
* **Broken Original APK:** On modern Android versions (Android 12+), the original live wallpaper APK fails and appears completely broken because Google officially deprecated and removed the **RenderScript** runtime from the OS. This repository preserves the source for historical and educational analysis.

## Project Structure
* **`app/src/main/java/com/android/wallpaper/holospiral/`**
  * `HE.java`: Token replacement engine (`@H@`, `@S@`, `@B@`, `@Z@`, `@G@`, `@R@`, `@K@`, `@C@`), `SharedPreferences` configuration handler, and preset manager (featuring all 8 built-in presets: *Original*, *Ocean*, *Forest*, *Neon rainbow*, *Mono*, *Dusk*, *Big glow*, and *Bright background*).
  * `HoloSettings.java`: Settings activity hosting the 8 parameter sliders (*Hue*, *Saturation*, *Brightness*, *Point size*, *Glow*, *Rainbow*, *Background*, and *Gamma*) and preset triggers.
  * `HoloSpiralRS.java`: RenderScript initialization, GLSL program compilation, background gradient mesh, and inner/outer spiral geometry generation.
  * `HoloSpiralWallpaper.java`, `HoloSpiralView.java`, & `HoloSpiralTestActivity.java`: Live wallpaper service bindings, `RSSurfaceView` renderer wrapper, and touch-drag preview activity.
  * `ScriptC_holo_spiral.java`, `ScriptField_VertexColor_s.java`, & `ScriptField_VertexShaderConstants_s.java`: RenderScript bitcode bindings and vertex data structures.

* **`app/src/main/res/`**
  * `raw/`: Compiled RenderScript bitcode (`holo_spiral.bc`) and exact GLSL vertex/fragment shaders (`fragment_background.glslf`, `fragment_geometry.glslf`, `vertex_background.glslv`, `vertex_geometry.glslv`)[span_1](start_span)[span_1](end_span).
  * `drawable/`: Particle point texture (`points_red_green.png`) and wallpaper picker thumbnail (`wallpaper_thumb.png`)[span_2](start_span)[span_2](end_span).

## Requirements
* **Android Studio / Gradle** (Compile SDK 33, Min SDK 14)
* Support for legacy RenderScript runtime
