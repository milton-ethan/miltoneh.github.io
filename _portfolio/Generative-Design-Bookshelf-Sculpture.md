---
title: "Bike Phone Mount"
excerpt: "Rotating Phone Mount for Bicycle Handlebars from Vanderbilt Additive and Polymer-based Manufacturing Class (CHBE 4200)"
header:
  image: /assets/img/handBanner.jpg
  teaser: /assets/img/hand2.jpg
gallery:
  - url: /assets/img/hand1.jpg
    image_path: /assets/img/hand1.jpg
    alt: "Hand Holder Image 1"
  - url: /assets/img/hand5.jpg
    image_path: /assets/img/hand5.jpg
    alt: "Hand Holder Image 5"
  - url: /assets/img/hand6.jpg
    image_path: /assets/img/hand6.jpg
    alt: "Hand Holder Image 6"
  - url: /assets/img/hand7.jpg
    image_path: /assets/img/hand7.jpg
    alt: "Hand Holder Image 7"
  - url: /assets/img/handTop.jpg
    image_path: /assets/img/handTop.jpg
    alt: "Top View of Hand Holder"
---

## Introduction
This project gave students an open ended opportunity to create a generative design project using Fusion360. For my project, I decided to merge form and function to create a project I could take home with me after graduation and use, without it being an eyesore. In light of this, I decided to create a sculpture designed to sit on a shelf and hold up books and spark conversation, in the shape of a human hand. As a big reader, my room and house are filled with books, a fact that’s unlikely to change as I get older, so a book holder was an easily applicable load-bearing idea for a first generative design project. While not as practical or space efficient as a book-end, I’ve found through my 3D-printed phone case that people will jump at the opportunity to ask about a project that draws the eye or looks striking.

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/hand2.jpg" width="100%" style="display: inline-block; margin: 0 2%;" />
</div>

#Preserve and Obstacle Geometry
To create my model, I knew I needed a human hand as a starting shape and for preserve geometries. Finding one online on GrabCAD, I tweaked the finger placements to support a flat surface, then cut a flat plane through the fingertips to give them a bit more purchase. I knew the fingertips, at a bare minimum, would need to be preserve geometry, since they are where the load on the sculpture is applied, and where the books rest. I also knew that without a place to secure the sculpture to some sort of a base plate, the entire thing would fall over. To remedy this, I cut some countersunk holes into the wrist of the sculpture, which became my second preserve geometry.

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/handFasteners.jpg" width="100%" style="display: inline-block; margin: 0 2%;" />
</div>

With these preserves set, and the entire hand as my starting-shape, I started my first studies. To try to avoid any part growth between the fingertips or beneath the hand, I first encased the entire hand in a block of obstacle-geometry, with the hand cut out of it as a cavity. This proved an ineffective method for the Fusion360 solver to run efficiently. I decided instead to create slices of obstacle geometry between the fingers to keep them separated, which worked a charm.

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/handForces1.jpg" width="100%" style="display: inline-block; margin: 0 2%;" />
</div>

#Load Case Application and Structural Constraints
The first and most obvious load case for the project was that of the books on the fingertips. A typical hardcover book weighs from 1-3 lbs, and I wanted the sculpture to be able to hold up 4-5 books safely. In light of this, I divided a 12 lb force across the five fingertips. Since the entire wrist section where the sculpture fastened to a base plate was a preserve geometry, I didn’t feel the need to apply any forces on it. 

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/hand4.jpg" width="100%" style="display: inline-block; margin: 0 2%;" />
</div>

Aside from the downward weight of the books (and gravity of course), I didn’t want the fingers or sculpture to snap if someone were to bump into its side. To combat this, I made a number of forces parallel to the ground at various points across the sculpture. First, I wanted to account for the chance that books would be leaned against the fingertips sideways (rather than / as well as stacked vertically), so I made some forces against the front end up the fingertips directed towards the wrist end. I also wanted to account for any bumps created when placing books on the sculpture. To combat this possibility, I made some preserve sections along the side of the hand by intersecting small spheres with the hand body (so that they would blend into the existing contour), and applying forces at these points directed across the palm, as well as between the fingertips. I figured most horizontal forces wouldn’t exceed the force exerted by the weight of a single book, so I made all horizontal forces about 2 lbs.
<br><br>
Once the generative study solved, a little bit of tailoring was needed - namely removing the unwanted preserve geometries that were created for load applications only, and connecting any  now-disconnected parts. Ultimately, once printed, the sculpture held a sizable amount of weight (a hardcover textbook and a few paperbacks) without much flexion. While delicate in the horizontal direction, I felt comfortable carrying the sculpture around, and it can definitely handle some sideways bumps without issue. I felt the most worried while cleaning the part, as it probably experienced more sideways forces during cleaning then it ever will again, however I was cautious and thorough, and it turned out great. Since it passed all my tests (bumps and books), I feel no need to further refine the design, and I’m happy to have a cool and functional sculpture made with one of my favorite developing technologies in manufacturing today!

## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a492558adfd4f2f8e4?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

#Critique of Generative Design
While visually interesting, it is important to know when generative design is useful and when it is not. Depending on the aesthetic of your model, generative design may produce very unnatural and undesirable results, for starters. (Many people confessed finding my hand creepy, though that was rather intentional on my part, and I took no offense.) Additionally, while minimizing materials while maintaining load bearing capabilities can be fantastic in additive manufacturing, it can be quite impractical in a subtractive workflow. The complex geometries created by generative design will be difficult to manufacture, which will increase time and cost, while also “wasting” more material, unless the removed stock can be reused. If a block of steel works great for an application, it probably isn’t worth the risk or the cost of trying to improve it. Still, for 3D printing or molds, the technology provides an incredible opportunity to reduce cost, create a more natural or “organic” looking form, and gain a competitive edge. I wouldn’t be surprised to see more generative bridges in the future.
<br><br>
The generative design process for this project was extremely iterative. The technology is still developing, and for all its charms, the generative space on Fusion360 has just as many quirks. Fusion didn’t seem to like my using pressure instead of point loads, leading me to create sideways preserve geometries somewhat arbitrarily. I would have liked to see a type of load that told the software the farthest points of a model along a certain axis would experience a force, without needing to turn that force into a preserve geometry. (I don’t care what the side of the hand looks like, so long as it doesn’t snap when it’s bumped into.) Getting the look I needed consisted of repeatedly cloning the previous study, tweaking something about the preserve geometries or the loads until the solver decided to behave or I got the look I wanted. Still, I find the technology fascinating and with definite room for improvement, I’m already thinking of new projects to try in the name of keeping my skills sharp for the future.



Here's a few images of my final product from other angles, as well as some of the steps leading up to its creation.


## Gallery
{% include gallery caption="Renderings, final product, and different generative studies." %}
