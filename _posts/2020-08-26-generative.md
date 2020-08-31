---
layout: single
title:  "Generative Art: Greater than the Sum of its Parts"
published: true
---

> Generative art refers to any art practice where the artist uses a system, such
as a set of natural language rules, a computer program, a machine, or other
procedural invention, which is set into motion with some degree of autonomy
contributing to or resulting in a completed work of art.
>
> <cite>[Philip Galanter](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.90.2634)</cite>

Since first learning about the concept of generative art, I have been intrigued by what it has to offer. The idea of creating art with computer programs in particular caught my interest, since this is a medium that is both familiar and accessible to me. Experimenting with it myself, with the help of a variety of online resources, revealed the rich possibilities of creating visually satisfying artworks from foundations of algorithms and mathematics.

The process of generating art programmatically incorporates randomness and tuneable parameters, making it highly dynamic and iterative. As I experimented I found I was often surprised by the results that came from changing parameters in my code, leading me to ideas that were not part of my original vision. Equally fun is looking at other peoples' generated artworks, and trying to deduce what algorithms or mathematical concepts might have been used to create them.

There are plenty of resources online that explain in more detail what generative art really is, and the many different tools and techniques that are used to create it, so these aspects won't be discussed here. The aim of this post is to demonstrate how an extremely simple base element or idea can be iterated upon to generate patterns that are (in my opinion, at least) surprisingly complex and pleasing to the eye.

---

Our starting point will be the two squares shown below, each with two opposing quarter-circles drawn on them. These are really the same image, with a 90 degree rotational offset between them.

<p align="middle">
  <img src="/assets/2020-08-26-generative/tile-1.png" width="25%" />
  <img src="/assets/2020-08-26-generative/tile-2.png" width="25%" />
</p>

On its own, there's nothing very exciting about this... but now, look what happens when we randomly tile the two squares in a grid pattern:

<p align="middle">
  <img src="/assets/2020-08-26-generative/basic.png" width="80%"/>
</p>

When I first saw this pattern, which is an example of something called a *Truchet pattern*, I was pretty amazed to find out how simple it was to create. Looking only at the tiled pattern, it is not entirely obvious how one would go about creating it programmatically, yet the answer is extremely simple.

So where can we take it from here? One way to extend our design is by layering the pattern at multiple scales, using different shades and line thicknesses to create aesthetic variation.

<p align="middle">
    <div id="carouselTruchetBW" class="carousel slide carousel-fade" data-ride="carousel" data-interval="1500">

      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="/assets/2020-08-26-generative/bw-2.png" alt="Base pattern">
        </div>
        <div class="carousel-item">
          <img src="/assets/2020-08-26-generative/bw-3.png" alt="Second layer">
        </div>
        <div class="carousel-item">
          <img src="/assets/2020-08-26-generative/bw-4.png" alt="Third layer">
        </div>
      </div>

      <a class="carousel-control-prev" href="#carouselTruchetBW" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselTruchetBW" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>

    </div>
</p>

Part of the beauty of generating art from code is that once the base program is written, modifications of this type (scaling, layering, etc.) are quick and easy. This is part of why the genre lends itself so well to experimentation, either manually or through randomisation.

Finally, let's add some colour. Shown below are a few more layered Truchet patterns, created with somewhat randomised sizes and scales.  

<p align="middle">
    <div id="carouselTruchetColored" class="carousel slide carousel-fade" data-ride="carousel" data-interval="2500">

      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="/assets/2020-08-26-generative/colored-1.png" alt="Pattern 1">
        </div>
        <div class="carousel-item">
          <img src="/assets/2020-08-26-generative/colored-2.png" alt="Pattern 2">
        </div>
        <div class="carousel-item">
          <img src="/assets/2020-08-26-generative/colored-3.png" alt="Pattern 3">
        </div>
        <div class="carousel-item">
          <img src="/assets/2020-08-26-generative/colored-4.png" alt="Pattern 4">
        </div>
      </div>

      <a class="carousel-control-prev" href="#carouselTruchetColored" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselTruchetColored" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
</p>

The addition of colour not only makes the patterns much more interesting to look at, but differentiates them even further from each other. The beauty and complexity of the final artwork disguises the simplicity of the building blocks - a statement that is true of the simple patterns seen in this post, and also of generative art as a whole.
