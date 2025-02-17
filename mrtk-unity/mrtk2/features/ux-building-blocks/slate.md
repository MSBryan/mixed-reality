---
title: Slate -- MRTK2
description: Documentation on Slate in MRTK
author: CDiaz-MS
ms.author: cadia 
ms.date: 01/12/2021
keywords: Unity,HoloLens, HoloLens 2, Mixed Reality, development, MRTK, Slate,
---

# Slate -- MRTK2

![Slate](../images/slate/MRTK_Slate_Main.png)

The Slate prefab offers a thin window style control for displaying 2D content, for example plain text or articles including media. It offers a grabbable title bar as well as *Follow Me* and *Close* functionality. The content window can be scrolled via articulated hand input.

## How to use a slate control

A slate control is composed of the following elements:

* **TitleBar**: The entire title bar on top of the slate.
* **Title**: The title area on the left side of the title bar.
* **Buttons**: The button area on the right side of the title bar.
* **BackPlate**: The back side of the slate.
* **ContentQuad**: Content is assigned as material. The example uses a sample material 'PanContent'.

<img src="../images/slate/MRTK_SlateStructure.jpg" width="650" alt="Slate Structure in the Unity editor">

## Bounds control

A slate control contains a bounds control script for scaling and rotating. For more information on bounds control, please see the [bounds control](bounds-control.md) page.

<img src="../images/slate/MRTK_Slate_BB.jpg" width="650" alt="Slate BB">

## Buttons

A standard slate offers two buttons as default on the top right of the title bar:

* **Follow Me**: Toggles an orbital solver components to make the slate object follow the user.
* **Close**: Disables the slate object.

<img src="../images/slate/MRTK_Slate_Buttons.jpg" width="650" alt="Slate Button">

## Scripts

In general, the `NearInteractionTouchable.cs` script must be attached to any object that is intended to receive touch events from the `IMixedRealityTouchHandler`.

<img src="../images/slate/MRTK_Slate_Scripts.png" alt="Slate Structure">

* `HandInteractionPan.cs` This script handles articulated hand input for touching and moving the content on the slate's *ContentQuad*.

* `HandInteractionPanZoom.cs`: In addition to the panning interaction, this script supports two-handed zooming.

<img src="../images/slate/MRTK_Slate_PanZoom.png" width="500" alt="Slate Pan Zooming">
