---
layout: default
title: Slicing
nav_order: 3
---

# Slicing:
Slicing a model is the process of running it through a type of program called, you guessed it, a slicer. There are various programs that do this, but the most popular is Cura. Running your model through a slicer turns the 3d model into a list of commands that the printer can execute, these commands are called gcode. I will be showing the process of slicing this example model of a cube using our Ultimaker 3 printer. This is a more advanced printer that has 2 extruders, but we will ignore that for the purpose of this simple overview.

For the sake of simplicity I will go over the basic features of cura that you need to know here. If you are interesed in learning more, check out the advanced slicing tutorial under the advanced section.

## Basic settings:
At the top of your screen you should have the options shown below. You may need to click on the right most box to open the full print settings view.

![image](https://user-images.githubusercontent.com/61284764/224892159-9a7c81ad-d86e-45f7-be5b-31a58c483047.png)
*figure 2a*

<br>

### Resolution:
The first setting "Resolution" is how thin the layers of your print will be. The lower the number, the thinner the layer, the higher quality the print is. However, the smaller the layer, the slower the print takes and the more material it uses. The comparison below demonstrates what this cube will look like with different layer heights.

For example, with a resolution of 0.06mm, this 25x25mm cube takes just over 2 hours to print! However since this model does not have any small details or any pieces that need to fit inside one another, we can raise our resolution to 0.2mm. This reduces our print time to just 27 minutes!

![image](https://user-images.githubusercontent.com/61284764/224893119-ba09d1f9-83bc-4e55-8c93-7a890566806f.png)

*figure 2b*

It's up to you to pick your layer height depending on what you're printing, but I reccomend 0.15-0.2mm for the best print speeds.

<br>

### Infill:

Infill is the material that is generated inside of your object to support the roof, walls and any overhanging parts where it would otherwise be floating! 3D printers are not magic and cannot print in the middle of the air, so too little infill will mean your model's quality will suffer as it cannot bridge far enough.

The default value of 20% will work just fine for a majority of prints, as it is the optimal balance between speed and strength. If your part needs to hold weight or needs to withstand large amounts of stress, consider raising this as your part will be much stronger. The inverse of this is also true, if your part is a simple cube like mine, and does not need to be very strong we can lower this value to 10%, to save time and materials. Below is an image of my cube with 20% infill, with the top layers hidden so you can see inside.

![image](https://user-images.githubusercontent.com/61284764/224894227-ffca10e0-a4c0-44ac-a328-43b3d98d2326.png)

*figure 2c*

<br>

### Support:

Sometimes your model has large overhangs, tall parts or just a part where it has more than a 65 degree angle. To make sure the printer has something to put the material on, we use what we call support strucutres. These are quite simple(for now) and should be enabled if your print needs has an angle over 65 degrees from vertical. For example, we have this dog model that has a very long stretch between the legs that would otherwise not print!

![image](https://user-images.githubusercontent.com/61284764/224895544-bfe05dac-7f15-4f24-b959-61df0f553efd.png)

*figure 2d*

<br>

## Adhesion: 

This setting is probably the easiest of them all. If your print is small, or does not have a lot of contact area on the print bed, you should enable it. My cube has a large flat surface on the bottom, so I would not need to enable this. However, if you are making a part with little contact on the bed, enabling this setting tells the program to generate a few 1 layer thick rings that attach to the bottom layer of the print. This increases the surface area on the bed, making it stick better! Don't worry though, these can easily be pulled or cut off after the print is done! Heres what it looks like(orange lines)!

![image](https://user-images.githubusercontent.com/61284764/224896293-b79770fa-543d-43ca-ba27-bfc3554b11f6.png)

*figure 2e*  

<br>
