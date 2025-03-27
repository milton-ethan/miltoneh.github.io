---
title: "Multi-Material Pliers"
excerpt: "Multi-Material Pliers from Vanderbilt Additive and Polymer-based Manufacturing Class (CHBE 4200)"
header:
  image: /assets/img/pliers3.jpg
  teaser: /assets/img/pliers1.jpg
gallery:
  - url: /assets/img/pliers1.jpg
    image_path: assets/img/pliers1.jpg
    alt: "Pliers Rendering 1"
  - url: /assets/img/pliers2.jpg
    image_path: assets/img/pliers2.jpg
    alt: "Pliers Rendering 2"
  - url: /assets/img/pliers3.jpg
    image_path: assets/img/pliers3.jpg
    alt: "Pliers Rendering 3"
  - url: /assets/img/pliersGif1.gif
    image_path: assets/img/pliersGif1.gif
    alt: "Quick dissasembly demonstration."
  - url: /assets/img/pliersGif2.gif
    image_path: assets/img/pliersGif2.gif
    alt: "The pliers in action."
---

## Introduction
Print-in-place is a method of 3D-Printing design that allows for fully functional assemblies or products to be fabricated in a single print without requiring post-assembly. When done properly, this can save time and money, and allow for rapid iteration. The idea is to print assemblies with multiple materials on one print bed so the part is ready to go straight out of the 3D printer. 

The technology is limited by typical 3D-printing barriers such as support and resolution, however faces the additional challenge of printing with multiple materials. This is typically achieved in one of two ways: using multiple extruders, or using a more advanced extruder that can swap filaments. 

Despite these challenges, the print-in-place technique has been used in a variety of commercial applications. Some examples would be hinged parts such as phone stands or small tools, or fidget toys which often use simple inexpensive designs with few materials. More advanced printing techniques such as [PolyJet](https://www.stratasys.com/en/industries-and-applications/3d-printing-applications/rapid-prototyping/) printing has been used to create small scale models of parts for commercial prototyping, and even bioprinting scaffolding for biomedical purposes.

Typical materials for print-in-place assembles might be:
- PLA for cheap, biodegradable, easy-to-print plastic.
- TPU for flexible "rubbery" parts, useful for hinges, springs, and grip.
- PETG for a more robust, chemical resistant plastic safe.
- Nylon for flexibility and resistance to wear and tear.


## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a48ae82478546fcef0?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Design & Iteration
The main idea behind my design was a set of pliers that used press-fit or sliding parts that could be printed once, and adjusted to meet a specific application. My desire to make the pliers have an adjustable stiffness led me to sacrifice the true print-in-place methodology, and instead print a set of TPU strips that acted as compression springs that could be press-fit into the dovetailed slots in the plier handles. 
The dovetailed slot and strip design allowed the TPU strips to be slotted in from the side without falling out during actuation. Multiple slots and corresponding strips were implemented so that the strips could be rearranged into larger or smaller slots to create variable stiffness.
The result of this design was a robust set of functional pliers with a high grip strength, (tested by picking up many small resistors of a flat surface at a quick pace.)

I knew the pliers would never need to bend more than, say, 20 degrees, and I designed my hinge joint accordingly. The pliers implement a T shaped slot that allows the two plier handle halves to slot into each other at 90 degrees from their intended orientation. This allows the pliers to be assembled with no extra tools or components in the print-in-place spirit, provides the mechanical advantage of creating two crossed levers, and makes for a smooth sliding joint with the correct tolerances. 

One design flaw I didn’t initially catch until assembly was that my pliers had no gap between the jaws when the TPU strips were in their corresponding initial slots. (I designed the pliers to be fully closed, even when the “springs” had no compression). The adjustable design easily accounted for this issue – all I had to do was put a longer TPU strip into a shorter slot to give the jaws a small initial gap. However, if I were to reprint the pliers a second time, I’d leave a few-millimeter gap between the jaws in their resting state.


The final model features a reinforced handle, optimized jaw shape for gripping, and a resilient spring structure that retains elasticity after multiple uses.

## Specifications
- **Jaw Length:** 40mm
- **Jaw Capacity:** Variable, but generally [INSERT]
- **Material Combination:** PLA body with flexible, adjustable TPU "spring" strips.

## TPU Print Settings
- **Nozzle Diameter:** 0.6mm
- **Extruder Temperature:** 240C
- **Bed Temperature:** 60C
- **Layer Height:** 0.16-0.4mm
- **Infill:** 25%
- **Supports:** None needed

## PLA Print Settings
- **Nozzle Diameter:** 0.4mm
- **Extruder Temperature:** 210 C (First layer 215 C)
- **Bed Temperature:** 65C
- **Layer Height:** 0.1-0.3mm
- **Infill:** 20%
- **Supports:** Grid style, minor support needed.

## Gallery
{% include gallery caption="Renderings, final product, dissasembly, and pliers in action" %}
