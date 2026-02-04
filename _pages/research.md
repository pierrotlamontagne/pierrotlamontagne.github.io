---
title: "Research"
permalink: /research/
author_profile: true
---

Welcome! This page gives a **high-school-level tour** of how we find exoplanets with radial velocities and how **stellar activity** can confuse us. Each short animation is paired with a simple idea and a key equation.

### 1. Detecting exoplanets with radial velocity

When a planet orbits a star, **both** move around their common center of mass. The star wobbles toward and away from us, making its spectral lines shift due to the **Doppler effect**.

<video autoplay loop muted playsinline style="width: 100%; max-width: 900px; margin: 1.5em auto; display: block; border-radius: 8px;">
  <source src="/images/RadialVelocityOutreach.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

In the animation:
- Left: the star and its planet orbit a common center.
- Top-right: spectral lines shift left/right as the star moves toward/away from us.
- Bottom-right: from many spectra, we measure a **radial-velocity curve**.

If the orbit is nearly circular, the star’s radial velocity can be approximated as

$$v_\star(t) \approx K \sin\!\left(\frac{2\pi t}{P}\right)$$
where:
- $P$ is the orbital period,
- $K$ is the velocity amplitude (how strong the wobble is).

The Doppler shift of a spectral line with rest wavelength $\lambda_0$ is

$$\frac{\Delta \lambda}{\lambda_0} \approx \frac{v_\star}{c}$$
so by measuring tiny shifts $\Delta \lambda$, we infer $v_\star$ and thus the **planet’s mass**.

---

### 2. Stellar activity: when starspots fake planets

Stars are not perfect spheres of light. **Dark spots** rotating across the surface change how much light we receive from the approaching vs. receding side. This distorts the spectral line shape and can create a **fake RV signal**, even with no planet.

Below, the two animations show the same idea with different spot patterns:

<div style="display: flex; flex-wrap: wrap; gap: 1.5rem; justify-content: center; align-items: flex-start; margin: 1.5em 0;">
  <figure style="flex: 1 1 280px; max-width: 500px; margin: 0;">
    <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
      <source src="/images/StellarActivity.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="margin-top: 0.5em; font-size: 0.95em;">
      <strong>Single spot:</strong> one dark region crosses the star. It removes light from one rotational “side”, distorting the spectral line and producing a smooth, planet-like RV curve.
    </figcaption>
  </figure>

  <figure style="flex: 1 1 280px; max-width: 500px; margin: 0;">
    <video autoplay loop muted playsinline style="width: 100%; border-radius: 8px;">
      <source src="/images/StellarActivityMultiSpot.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <figcaption style="margin-top: 0.5em; font-size: 0.95em;">
      <strong>Many spots:</strong> several spots of different sizes and latitudes rotate together, creating a more irregular, quasi-periodic RV signal.
    </figcaption>
  </figure>
</div>

In both cases, the apparent radial velocity comes from changes in the **centroid** of the distorted spectral line:

$$v_{\text{activity}}(t) \propto
\frac{\displaystyle\int \lambda\,[1 - F(\lambda,t)]\,\mathrm{d}\lambda}
     {\displaystyle\int [1 - F(\lambda,t)]\,\mathrm{d}\lambda}
 \;-\; \lambda_0$$

where $F(\lambda,t)$ is the line profile at time $t$. Even without a planet, this can look like a planet-induced RV curve.

---

### 3. Planet + activity: the real-life challenge

In real data, we often see **both** a planet and stellar activity at the same time. The animation below combines the two:

<video autoplay loop muted playsinline style="width: 100%; max-width: 900px; margin: 1.5em auto; display: block; border-radius: 8px;">
  <source src="/images/PlanetPlusActivity.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

- Left: the star wobbles from a planet and has rotating spots.
- Top-right: the spectral line shifts (planet) and is distorted (spots).
- Bottom-right: we see the **total RV signal**, then split it into:
  - a smooth **Keplerian** planet curve,
  - a more irregular **activity** curve.

Mathematically, the observed RV is a sum:

$$v_{\text{obs}}(t) = v_{\text{planet}}(t) + v_{\text{activity}}(t) + \text{noise}$$

My research focuses on building models that can **separate these pieces**, so we can measure exoplanet masses as cleanly and precisely as possible.

