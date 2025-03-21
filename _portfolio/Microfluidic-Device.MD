---
title: "Microfluidic Device"
excerpt: "Microfluidic particle seperator from Vanderbilt Additive and Polymer-based Manufacturing Class (CHBE 4200)"
header:
  image: /assets/img/microfluidicBanner.jpg
  teaser: /assets/img/microfluidic2.jpg
gallery:
  - url: /assets/img/microfluidic1.png
    image_path: assets/img/microfluidic1.png
    alt: "Rendering 1"
  - url: /assets/img/microfluidic2.png
    image_path: assets/img/microfluidic2.png
    alt: "Rendering 2"
  - url: /assets/img/microfluidic3.png
    image_path: assets/img/microfluidic3.png
    alt: "Rendering 3"
  - url: /assets/img/microfluidic1.jpg
    image_path: assets/img/microfluidic1.jpg
    alt: "Microfluidic Device Image 1"
  - url: /assets/img/microfluidic2.jpg
    image_path: assets/img/microfluidic2.jpg
    alt: "Microfluidic Device Image 2"
  - url: /assets/img/microfluidic3.jpg
    image_path: assets/img/microfluidic3.jpg
    alt: "Microfluidic Device Image 3"
  - url: /assets/img/microfluidic4.jpg
    image_path: assets/img/microfluidic4.jpg
    alt: "Microfluidic Mold Image 1"
  - url: /assets/img/microfluidic5.jpg
    image_path: assets/img/microfluidic5.jpg
    alt: "Microfluidic Mold Image 2"
  - url: /assets/img/microfluidicSetup.jpg
    image_path: assets/img/microfluidicSetup.jpg
    alt: "Microfluidic Device Setup"
  - url: /assets/img/microfluidicParticles.jpg
    image_path: assets/img/microfluidicParticles.jpg
    alt: "Microfluidic Particles Image 1"
---

## Introduction
Microfluidic devices are small-scale systems designed to control and process tiny fluid volumes, usually in the microliter or nanoliter range, through microscale channels. They are commonly used in biomedical research, diagnostics, and chemical analysis but can also be used in environmental monitoring, drug development, and food safety testing.

Pinched flow fractionation (PFF) is a passive microfluidic technique used for continuously sorting particles by size within a channel. It relies on laminar flow properties, where a particle-free fluid focuses the particle-containing fluid as they pass through a narrow "pinched segment." In this region, the particles are pushed against one of the channel’s sidewalls, and align based on their size, with smaller particles positioned closer to the wall and larger particles closer to the channel center. As the flow exits the pinched segment into a broader section, particles separate along their streamlines. Their final position can be calculated as a function of the pinched and broad section widths as well as the particle diameters.

This method enables precise particle sorting without requiring external forces, making it useful for applications involving droplet or cell separation. One potential use case could be separating circulating tumor cells (CTC's) from white blood cells in a blood sample.


# CAD MODEL
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4df359f54eff9d9d4?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
---

## Instructions

How to go from the 3D printed mold to the final device (Lab on a Chip paper). Include the following steps but with additional detail:

- **CAD Model**
The process for creating the microfluidic device began with a provided template CAD file in Fusion 360. The template included the main housing the PDMS would be poured into, as well as the locations of the two inlets and three outlets. It is important to ensure that your inlets and outlets are spaced such that the barbs connecting the lines to the device can all fit next to each other. The positive mold was  then designed parametrically using the pinched flow fractionation formula included in the discussion section.
- **Print and Cure Mold**
The positive mold was then printed using a Formlabs SLA resin printer. SLA printing ensures the high resolution necessary to achieve the small geometry required in microfluidic testing. Once the mold finish printing, it was washed with isopropyl alcohol and UV cured at 60°C for 60 seconds, as specified by the Lab on a Chip paper used as a basis for this project. Since only the surface needs to cure, further curing is not necessary and can in fact negatively impact the microfluidic device.
- **Parylene Device**
The molds are the coated with a nanometer thick layer of parylene-C using a machine such as a Labcoter PDS 2010 parylene deposition machine. This parylene layer, depending on the application, can be used to prevent the cytotoxicity that any uncured resin may present. In our case, since the microfluidic devices were not actually being used on biological substances, the parylene was primarily to create a hydrophobic barrier so that the PDMS can be easily demolded after it finishes curing and does not get stuck to the resin mold. 

- **Cast PDMS**
After the parylene layer is deposited, PDMS is mixed in a 10:1 elastomer to curing-agent ratio and the mold is placed in a vacuum chamber for 10 minutes to remove any gas bubbles present in the PDMS. Once de-gassed, the PDMS is cured at 80°C for 3 hours, after which it is ready to be bonded to glass microscope slide.

- **Plasma Bond Glass Slide**
In the final step of the microfluidic device creation process, the PDMS is demolded and bonded to a glass slide using a device such as a PlasmaFlo PDC FMG plasma cleaner (as specified by the Lab on a Chip paper, creating strong adhesion between the PDMS and the slide. After this, the microfluidic device is ready for use.


## Discussion
My microfluidic device has a variety of features making it optimal for particle sorting, (which, as mentioned, can be used for such cases as separating circulating tumor cells (CTC's) from white blood cells in a blood sample, or removing impurities from an industrial powder, for example). The device is designed parametrically based on the following formula, which relates the particle outlet position to the pinched flow fractionation geometry:

  - url: /assets/img/microfluidic1.png
    image_path: assets/img/microfluidic1.png
    alt: "Rendering 1"

The parametric geometry in CAD makes it easy to adjust the device for different size particles. By determining the range of positions the particles should end up based on their theoretical streamlines, dividers can be placed to properly sort the particles. 
There are various important geometries to consider in this model. The height of the mold should be large enough to let both particles through. However, if it is too tall then particles can stack on top of each other, potentially clogging or failing to sort correctly. Choosing a size of around 1.5x the large particle diameter should suffice. 
Similarly, examining the above formula reveals that the larger the ratio between the pinched and broad sections of our device creates larger separation at the outlet. Our broad section is limited by the size of the microscope slide and the walls of the mold, so our pinched section should be made as small as possible. (Again, around 1.5x the large particle diameter)

In an attempt to keep the flow rate between the different channels, my design includes a few particular design choices attempting to combat the backflow issue that was observed in previous iterations of this project. For starters, my three channels were quite long, in the hope that any back pressure might “equalize” slightly by the time it backed up to the channel entrance. More importantly, I was careful to adjust the height of the third channel such that all three channels had an identical cross sectional area (including the area that the channel walls consumed). The channel outlet positions mandated that more width was given to the bottom channel, (which should only contain water, theoretically.) 
By shrinking the height of this channel, I equalized the areas in attempt to get exactly 1/3 of the water to go through each channel. Since flow rate is directly proportional to area and pressure, my hope was the equal cross sectional area would cause equal pressures at each inlet. (This was my attempt to tackle the challenge in the bonus, although I was more concerend with the geometry forcing equal flow rates and pressures, rather than what happened to the particles after they left my device.)

It is difficult to verify exactly how effective my design decisions were unfortunately. Gravity and the tilt of the device appeared to have an extremely strong affect on which outlet the water flowed. Even when this effect was counteracted by using extremely long outlet tubes suspended in the air, the particles appeared to vary quite a lot in their entrance velocity and streamline preference, indicating some part of the process was missing that prevented the device from working properly. This could have been caused by a few things such as air in the lines creating turbulence, or possible motor vibration, tilt, or some other factor. Further troubleshooting will be required before more informed design choices can be made.

{% include gallery caption="Some images of my microfluidic device and mold, the CAD files, the setup, and the particles." %}

---
