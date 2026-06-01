# Puddles VRC Unity Tools

This repository contains a Unity Package Manager package for VRChat avatar creation tools.

## Add to VRC Creator Companion

Click Settings, Click Packages, Click +Add Repositor(on the right hand side of the screen) Then Paste this link and hit submit.

https://raw.githubusercontent.com/Austin-M-Thomas/p-j-e/main/index.json

Now the package should be available for instal in your VRChat creator companion under Managed Packages. 

## Package

Package folder:

`Packages/com.puddles.vrc-unity-tools`

Package manifest:

`Packages/com.puddles.vrc-unity-tools/package.json`

## Install In A Unity Project

### Option A: Embedded Package

Copy this folder into your Unity project's `Packages` folder:

`com.puddles.vrc-unity-tools`

The final path should look like:

`YourUnityProject/Packages/com.puddles.vrc-unity-tools/package.json`

Unity should detect it after recompiling.

### Option B: Add Package From Disk

1. Open Unity Package Manager.
2. Click `+`.
3. Choose `Add package from disk...`.
4. Select:

`Packages/com.puddles.vrc-unity-tools/package.json`

## Current Tool

Open the current tools from:

- `Tools > Puddles > Poiyomi Lighting Menu Builder`
- `Tools > Puddles > Avatar Action Builder`

The Poiyomi tool builds VRC radial puppet expression menus for Poiyomi material float/range shader properties.

The Avatar Action Builder creates editable profile-based controls for toggles, radials, and selector submenus that can mix object states, blendshapes, material swaps, and shader float changes.

More detailed usage notes live inside the package README:

`Packages/com.puddles.vrc-unity-tools/README.md`

The package has an editor-only assembly definition that references `VRC.SDK3A` and `VRC.SDKBase`, so install it into a VRChat avatar project with the SDK already present.

Current version: `0.6.1`

## Planned Upgrades

- Add post-generation renaming for generated radial dials and menus.
- Add a viewer for existing generated controls already attached to the avatar.
- Revisit these before a public release pass.

## Exporting A `.unitypackage`

A classic `.unitypackage` export has to be created from inside Unity:

1. Import or embed the package in a Unity project.
2. In the Project window, select the package folder or copied `Assets` version.
3. Use `Assets > Export Package...`.
4. Include dependencies only if you intentionally want Unity to pull extra assets into the export.

For this tool, the UPM package is the cleaner install path because it keeps editor code separate from avatar assets.
