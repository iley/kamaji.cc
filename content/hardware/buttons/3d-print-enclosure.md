---
title: "3D-print Enclosure"
date: 2023-01-14T17:43:26Z
lastmod: 2023-05-06
weight: 4
---

For this part you will need access to an FDM 3D-printer. If you don't have one, you can find an on-demand print service online.

You will also need filament to print with. We use PETG because it's a little more durable, but PLA would work too.

### Download and slice the parts

The button enclosure consists of two parts. Start by downloading the STL files:

 * [button_v1_bottom.stl](https://github.com/iley/kamaji/blob/master/3d/button_v1/button_v1_bottom.stl)
 * [button_v1_top.stl](https://github.com/iley/kamaji/blob/master/3d/button_v1/button_v1_top.stl)

Next you need to use a slicer software such as [PrusaSlicer](https://github.com/prusa3d/PrusaSlicer) or [Cura](https://ultimaker.com/software/ultimaker-cura/). We recommend PrusaSlicer.

Import the STL files into the slicer. Place both parts with the flat outer part facing downwards. This helps minimize supports and gives the outer surface nice finish.

You might want to do the first test print with just single part. Once you're confident in your print settings, feel free to pack multiple parts onto the print surface.

Here is what it might look like in the slicer:

<img src="/images/button-slicer-layout.png">

The default print settings of your slicer might work just fine. However, there are a few settings worth tweaking.

### Enable supports

Supports are needed for the mounting holes only, see the picture below (supports are shown in green).

<img src="/images/button-slicer-supports.png">

Notice that the chamfers on the edges of the parts do not need supports. To prevent the slicer from generating the unnecessary supports, you can adjust the overhang threshold to a value below 45. This is how it's done in PrusaSlicer:

<img src="/images/button-slicer-settings-supports.png">

### Tweak infill settings

Here are infill settings that worked well for us:


<img src="/images/button-slicer-settings-infill.png">

### Increase the number of perimeters

It is also worth increasing the number of perimeters to 3 so that the vertical walls are a little thicker.

<img src="/images/button-slicer-settings-perimiters.png">


### Print

Before printing, double check that you're using the correct printer profile and filament settings (especially the print temperature).

Once printing is done, you'll need to remove the supports. They should come off easily. Poking a screwdriver through the hole from the other side usually does the trick.
