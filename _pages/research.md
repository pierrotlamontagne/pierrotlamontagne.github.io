---
title: "Research"
permalink: /research/
author_profile: true
---

Welcome! This page gives a quick tour of how we find exoplanets with radial velocities and how stellar activity can confuse us. I use animations I created with the open-source package [manim](https://www.manim.community/). 

When a planet orbits a star, **both** move around their common center of mass. The star wobbles toward and away from us, making its spectral lines shift due to the **Doppler effect**.

<figure style="max-width: 900px; margin: 1.5em auto;">
  <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px; display: block;">
    <source src="/images/RadialVelocityOutreach.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <figcaption style="margin-top: 0.5em; font-size: 0.95em;">
    - <strong>Left:</strong> the star and its planet orbit their <strong>barycenter</strong>.
    - <strong>Top-right:</strong> spectral lines shift <strong>left/right</strong> as the star moves <strong>toward/away</strong> from us.
    - <strong>Bottom-right:</strong> from many spectra taken at different times, we measure a <strong>radial-velocity (RV) curve</strong>.
  </figcaption>
</figure>

From the shape and amplitude of this RV curve, we can infer the planet's **mass**, **period** and **eccentricity**. 

---

Stars are not perfect spheres of light. **Dark spots** rotating across the surface change how much light we receive from the approaching vs. receding side. This distorts the spectral line shape and can create RV signals, even with no planet.


<div style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: center; align-items: flex-start; margin: 1.5em 0;">
  <figure style="flex: 1 1 280px; max-width: 500px; margin: 0;">
    <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
      <source src="/images/StellarActivity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="margin-top: 0.5em; font-size: 0.95em;">
      <strong>Single spot:</strong> one dark region crosses the star. It removes light from one rotational “side”, distorting the spectral line and affecting the RV curve.
    </figcaption>
  </figure>

  <figure style="flex: 1 1 280px; max-width: 500px; margin: 0;">
    <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
      <source src="/images/StellarActivityMultiSpot.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="margin-top: 0.5em; font-size: 0.95em;">
      <strong>Many spots:</strong> several spots of different sizes and latitudes rotate together, creating a more irregular, quasi-periodic RV signal that can imitate a planet's signal. 
    </figcaption>
  </figure>
</div>

---

In real data, we often see **both** a planet and stellar activity at the same time.

<video autoplay loop muted playsinline style="width: 100%; max-width: 900px; margin: 1.5em auto; display: block; border-radius: 8px;">
  <source src="/images/PlanetPlusActivity.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


The observed RV curve is a sum:

$$v_{\text{obs}}(t) = v_{\text{planet}}(t) + v_{\text{activity}}(t) + \text{noise}$$

My research focuses on building models that can **separate these pieces** on real high-resolution spectral data, so we can characterize exoplanet as cleanly and precisely as possible, without biases. 

*You can find the animations [here](https://drive.google.com/drive/folders/1E4OUYQf_Xw-Weefa2b0YH3HMtRwvhtdn?usp=sharing)*

