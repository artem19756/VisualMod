# VisualMod — Minecraft Java 1.21.4 / Fabric

Initial source prototype for a lightweight client-side visual mod.

## Current prototype features
- Right Shift opens the VisualMod settings screen.
- Minimal custom HUD with an FPS counter.
- Optional lightweight custom crosshair.
- Toggle placeholders for extra particles and compact hotbar (these are not implemented yet).

## Build
Requires JDK 21 and internet access for Gradle dependencies.

```bash
gradle build
```

The jar should appear in `build/libs/`. Use the regular Gradle wrapper if you add one locally.

## Install
1. Install Fabric Loader for Minecraft Java 1.21.4.
2. Put the built `visualmod-1.0.0.jar` in the instance's `mods` folder.
3. Launch using a compatible Java 21 runtime.

## Performance design
The prototype avoids per-frame allocations in its HUD path and uses small GUI draw calls. It does not replace Sodium and does not guarantee a specific FPS increase. Test separately on desktop and Android/FCL.

## Important
This is a starter source project, not a prebuilt or tested jar. Some planned options are labelled reserved and do not yet change Minecraft rendering. Verify dependency versions and compile against your chosen Fabric/FCL environment.
