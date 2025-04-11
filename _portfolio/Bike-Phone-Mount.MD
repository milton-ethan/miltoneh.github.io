---
title: "Bike Phone Mount"
excerpt: "Rotating Phone Mount for Bicycle Handlebars from Vanderbilt Additive and Polymer-based Manufacturing Class (CHBE 4200)"
header:
  image: /assets/img/phoneHolderRendering1.png
  teaser: /assets/img/phoneHolderRendering2.png
gallery:
  - url: /assets/img/phoneHolder1.jpg
    image_path: /assets/img/phoneHolder.jpg
    alt: "Full Phone Holder 1"
  - url: /assets/img/phoneHolder2.jpg
    image_path: /assets/img/phoneHolder2.jpg
    alt: "Full Phone Holder 2"
  - url: /miltoneh.github.io/assets/img/phoneHolderTest4.jpg
    image_path: /assets/img/phoneHolderTest4.jpg
    alt: "Full Phone Holder Test Third Image"
  - url: /assets/img/phoneHolderTest5.jpg
    image_path: /assets/img/phoneHolderTest5.jpg
    alt: "Full Phone Holder Test Fourth Image"
---

## Introduction
The task for this project was to design a phone holder that could mount onto a bike handlebars, complete with a rotating locking mechanism allowing the phone to 'click' into place in the vertical and horizontal modes. For a project such as this, with multiple components, whose positions are all defined relative to each other, it is almost a necessity to use a method of modeling known as [Top-Down Modeling](https://www.youtube.com/watch?v=HHL8xvC3W1c&ab_channel=AutodeskFusion). In this method, components are not created in separate files. Rather, new components are added to the larger assembly bit by bit, so that the features and positions of the existing parts can provide the needed context while modeling. 

For example, it would be difficult to design a piece that clamps onto bike handlebars without first knowing the geometry of the handlebars, and where in space the piece would be clamped. With top down modeling, the clamp can be designed directly around the handlebars without needing to switch back and forth between separate files. 

Components, once created, can also be moved around the assembly, and joined with other components via "joints" or "mates" (depending which software you may be using). For example, if you were designing a door in CAD, Top-Down Modeling would allow you create a hinge of the exact size and in the exact place you needed, say the top of the door, copy it to drag to the bottom of the door, then use joints/mates to add revolute constraints to the hinges so the door opened and closed naturally in the CAD model. Ultimately, top-down modeling also streamlines workflow, leading to a better idea of an entire assembly, with less time and fewer mistakes.


## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a413b34a84c0f1fcba?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Design & Iteration
I wanted my design to have the following features:
- A spring-loaded detent mechanism that was easy to assemble.
- A convenient press fit for my phone to keep my over all design simple.
- A sturdy and tight fixture with minimal assembly to fix the rotating holder to the bike mechanism.

To achieve the simple spring-loaded detent mechanism, I created a pocket a spring and ball bearing could be easily dropped into. The ball bearing interfaces with a rotating disk with indentations allowing the phone holder to "snap" into place. In my first design, however, I failed to account for the detent mechanism pushing the entire phone holder out of place, as I was planning to slide it in from the top. (In other words, I had nothing ensuring the ball bearing wouldn't pop out and roll away.) In order to keep the easy assembly, but also keep the entire detent mechanism together, I decided to slot in the phone holder sideways instead of vertically, and retain it with a backing disk that could screw into a heat set insert.

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/phoneHolderSection.jpg" width="60%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderSection2.jpg" width="60%" style="display: inline-block; margin: 0 2%;" />
</div>

Counterboring the hole in the backing disk allowed an M5 bolt to keep the assembly together without any awkward protrusions. In the section analyses above, you can also look at my clamping mechanism for the bike handlebars. For ease of assembly, I used a simple top piece that screwed to two arms to clamp over the handlebars, which could be tightened to satisfaction. I used two arms instead of one so an Allen key could be used between them to fasten the retaining disk without interference.

To ensure my detent mechanism would function as anticipated, and that I had the right tolerance to press-fit my phone into the holder, I printed some test pieces out of PLA. This also let me test how effective my idea of using a heat set insert to screw in a retaining disk to hold the detent mechanism was.


<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/phoneHolderTest1.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderTest2.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
</div>
<br>
The detent and the retaining disk worked like a charm, but my press fit was a little loose, leading me to tighten the tolerance ever so slightly. Since PLA will tend to warp a bit (much more than with SLS printing), I used calipers to make sure I was getting real measurements off my test print instead of relying off the dimensions in CAD.

The result of these test prints and caution was a rigid stable phone mount with full functionality on the first print! 

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/phoneHolderFinal.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderFinal2.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderFinal3.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
</div>
<br>
Since SLS printing is more costly and labor intensive than standard FFF printing, it's important to be sure you have a good idea of how your part is going to turn out before pressing print. This, to me, illustrates why having a diverse range of rapid prototyping technologies is so beneficial.

Check out the print in action!

<div style="text-align: center;">
  <video width="360" height="640" controls style="display: inline-block; margin: 0 2%;">
    <source src="/miltoneh.github.io/assets/img/phoneHolderVid1.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>

  <video width="360" height="640" controls style="display: inline-block; margin: 0 2%;">
    <source src="/miltoneh.github.io/assets/img/phoneHolderVid2.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
</div>

Here's a few images of my final product from other angles.


## Gallery
{% include gallery caption="Renderings, final product, dissasembly, and pliers in action" %}
