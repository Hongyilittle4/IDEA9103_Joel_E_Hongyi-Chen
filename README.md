# IDEA9103_Joel_E_Hongyi-Chen
#  Emotional Breakdown in the Sky – A Perlin Noise Interpretation of *The Scream*

##  How to Interact
- **Load the page**: Once the page is loaded, the animated Perlin noise starts immediately.
- **Click one of the four level buttons**: Each level reflects a different degree of emotional breakdown through increasingly distorted and thicker Perlin noise lines.
- **Resize the window**: The canvas and elements will adapt dynamically to fit the screen.

##  Individual Approach
My individual contribution primarily utilizes **Perlin noise** to animate the sky, with **user input** (via buttons ranging from Level 1 to Level 4) used to guide the animation’s emotional intensity.

##  Driven By: Perlin Noise
I chose **Perlin noise** as the core driver of my animation. I use it for both the **direction** and **color variation** of sky lines, with additional noise-based logic for dynamic movement and texture layering.

##  Animated Properties
- **Line distortion and direction** change across levels, becoming more chaotic with higher levels.
- **Stroke thickness** increases with each emotional stage.
- **Color palette** is randomized but constrained to hues (blue, yellow, brown) matching the mood of *The Scream*.
- **Lines animate over time**, simulating emotional instability.
- Uniqueness: My work exclusively animates the **sky layer**, while other group members focused on figures, geometry, or land texture.

##  Visual Inspiration
Inspired by:
- The sky in Edvard Munch’s *The Scream*
- This generative art reference using Perlin noise and color mapping: [Steve’s Makerspace – Flow Field](https://editor.p5js.org/StevesMakerspace/sketches/4zn-XY-FH)
These influenced my color control and the way I structured flowing animated lines.

##  Technical Explanation
- The sky is drawn in a separate `noiseGraphics` layer using `createGraphics()` and `colorMode(HSB)`.
- Perlin noise is used to generate angles for curved strokes and to vary colors based on spatial position and time (`t`).
- Four animation levels are triggered by buttons; each adjusts `noiseSpeed`, `noiseScale`, and `strokeFactor`.
- `drawAnimatedNoise()` generates time-based motion, and `drawNoiseLines()` handles the initial static rendering.
- The final output mimics oil painting via `applyPaperTexture()`, which samples colors and overlays short curved strokes.

##  Group Code Modifications
I added `drawAnimatedNoise()`, level-based noise variation arrays, and modified button logic to dynamically change the noise behavior. These changes integrate seamlessly with the existing group structure and rendering pipeline.

##  External Tools & Techniques
- **Perlin noise flow field concept** adapted from open tutorials.
- **Paper texture layering** was implemented to simulate an oil-painting effect.
- **SVG-to-p5.js path conversion** was done using [svg2p5.com](https://svg2p5.com).

##  References
- Steve’s Makerspace. “Flow Field.” *p5.js Editor*, https://editor.p5js.org/StevesMakerspace/sketches/4zn-XY-FH  
- Munch, Edvard. *The Scream* (1893)  
- svg2p5.com – for SVG shape-to-code conversion
