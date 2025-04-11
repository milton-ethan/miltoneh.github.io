---
title: "Bike Phone Mount"
excerpt: "Rotating Phone Mount for Bicycle Handlebars from Vanderbilt Additive and Polymer-based Manufacturing Class (CHBE 4200)"
header:
  image: /assets/img/phoneHolderRendering1.png
  teaser: /assets/img/phoneHolderRendering2.png
gallery:
  - url: /assets/img/phoneHolder1.jpg
    image_path: assets/img/phoneHolder.jpg
    alt: "Full Phone Holder 1"
  - url: /assets/img/phoneHolder2.jpg
    image_path: assets/img/phoneHolder2.jpg
    alt: "Full Phone Holder 2"
  - url: /assets/img/phoneHolderTest3.jpg
    image_path: assets/img/phoneHolderTest3.jpg
    alt: "Full Phone Holder Test Third Image"
  - url: /assets/img/phoneHolderTest4.jpg
    image_path: assets/img/phoneHolderTest4.jpg
    alt: "Full Phone Holder Test Fourth Image"
  - url: /assets/img/phoneHolderTest5.jpg
    image_path: assets/img/phoneHolderTest5.jpg
    alt: "Full Phone Holder Test Fifth Image"
---

## Introduction
Top down modeling...
Blah [PolyJet](https://www.stratasys.com/en/industries-and-applications/3d-printing-applications/rapid-prototyping/) blah blah

I wanted to focus on a few key elements in my design:
- Bullet Point


## CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a413b34a84c0f1fcba?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Design & Iteration
I wanted my design to have the following features:
- A spring-loaded detent mechanism that was easy to assemble.
- A convenient press fit for my phone to keep my over all design simple.
- A sturdy and tight fixture with minimal assembly to fix the rotating holder to the bike mechanism.

To achieve the simple spring-loaded detent mechanism, I created a pocket a spring and ball bearing could be easily dropped into. The ball bearing interfaces with a rotating disk with indentations allowing the phone holder to "snap" into place. In my first design, however, I failed to account for the detent mechanism pushing the entire phone holder out of place, as I was planning to slide it in from the top. (In other words, I had nothing ensuring the ball bearing wouldn't pop out and roll away.) In order to keep the easy assembly, but also keep the entire detent mechanism together, I decided to slot in the phone holder sideways instead of vertically, and retain it with a backing disk that could screw into a heat set insert.

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/phoneHolderSection.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderSection2.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
</div>

Counterboring the hole in the backing disk allowed an M5 bolt to keep the assembly together without any awkward protrusions. In the section analyses above, you can also look at my clamping mechanism for the bike handlebars. For ease of assembly, I used a simple top piece that screwed to two arms to clamp over the handlebars, which could be tightened to satisfaction. I used two arms instead of one so an Allen key could be used between them to fasten the retaining disk without interference.

To ensure my detent mechanism would function as anticipated, and that I had the right tolerance to press-fit my phone into the holder, I printed some test pieces out of PLA. This also let me test how effective my idea of using a heat set insert to screw in a retaining disk to hold the detent mechanism was.


<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/phoneHolderTest1.jpg" width="60%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderTest2.jpg" width="60%" style="display: inline-block; margin: 0 2%;" />
</div>


The detent and the retaining disk worked like a charm, but my press fit was a little loose, leading me to tighten the tolerance ever so slightly. Since PLA will tend to warp a bit (much more than with SLS printing), I used calipers to make sure I was getting real measurements off my test print instead of relying off the dimensions in CAD.

The result of these test prints and caution was a rigid stable phone mount with full functionality on the first print! 

<div style="text-align: center;">
  <img src="/miltoneh.github.io/assets/img/phoneHolderFinal.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderFinal2.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
  <img src="/miltoneh.github.io/assets/img/phoneHolderFinal3.jpg" width="45%" style="display: inline-block; margin: 0 2%;" />
</div>


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

Blah Blah...


## Gallery
{% include gallery caption="Renderings, final product, dissasembly, and pliers in action" %}
