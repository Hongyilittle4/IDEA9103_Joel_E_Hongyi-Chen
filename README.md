# IDEA9103_Joel_E_Hongyi-Chen
#  Emotional Breakdown in the Sky – A Perlin Noise Interpretation of *The Scream*

##  How to Interact
- **Load the page**: Once the page is loaded, the animated Perlin noise starts immediately.
- **Click one of the four level buttons**: Each level reflects a different degree of emotional breakdown through increasingly distorted and thicker Perlin noise lines.
- **Resize the window**: The canvas and elements will adapt dynamically to fit the screen.

##  Individual Approach
My individual contribution primarily utilizes **Perlin noise** to animate the sky, with **user input** (via buttons ranging from Level 1 to Level 4) used to guide the animation’s emotional intensity.

##  Visual Inspiration
Inspired by:
- The animated version of [Vincent van Gogh’s *Starry Night* ](https://www.youtube.com/watch?v=pCHFAsXYHGA)
- This generative art reference using Perlin noise and color mapping: [Steve’s Makerspace – Flow Field](https://editor.p5js.org/StevesMakerspace/sketches/4zn-XY-FH)
These influenced my color control and the way I structured flowing animated lines.
![alt text](<Perlin Noise.png>)

##  Technical Explanation
- The sky is drawn in a separate `noiseGraphics` layer using `createGraphics()` and `colorMode(HSB)`.
- Perlin noise is used to generate angles for curved strokes and to vary colors based on spatial position and time (`t`).
- Four animation levels are triggered by buttons; each adjusts `noiseSpeed`, `noiseScale`, and `strokeFactor`.
- `drawAnimatedNoise()` generates time-based motion, and `drawNoiseLines()` handles the initial static rendering.
- The final output mimics oil painting via `applyPaperTexture()`, which samples colors and overlays short curved strokes.
###  How To Achieve The Ideal Visual Effect
- **Line distortion and direction** change across levels, becoming more chaotic with higher levels.
- **Stroke thickness** increases with each emotional stage.
- **Color palette** is randomized but constrained to hues (blue, yellow, brown) matching the mood of *The Scream*.
- **Lines animate over time**, simulating emotional instability.
- Uniqueness: My work exclusively animates the **sky layer**, while other group members focused on figures, geometry, or land texture.
###  How The Perlin Noise Sky Was Made Animated
I transformed the originally static sky into an animated one by:
- Introducing a time variable (`t`) and incorporating it into the noise function to simulate a continuously flowing sky.
- Replacing `noLoop()` with `draw()` to enable frame-by-frame canvas updates.
- Modifying noise coordinates over time, creating the illusion that the painterly background is alive and subtly shifting.

##  References

StevesMakerspace. (n.d.). *Flow fields for YT* [Computer software]. p5.js Web Editor. https://editor.p5js.org/StevesMakerspace/sketches/4zn-XY-FH

Author Media. (n.d.). *The ultimate guide to writing YouTube video descriptions and titles* [Video]. YouTube. https://www.youtube.com/watch?v=CSMcrKouQ3o

StevesMakerspace. (n.d.). *Perlin noise flow field colors* [Computer software]. p5.js Web Editor. https://editor.p5js.org/StevesMakerspace/sketches/qTjXhdC8t

