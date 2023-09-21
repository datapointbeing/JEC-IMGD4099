My interest with A2 was exploring a paper "topography" look comprised of a number of cutout layers approximating the contents of the video feed. I had one of my first art class final projects in mind when I created this: it was a piece based on one selected from the Worcester Art Museum, a woodblock print that created the impression of cascading layers of solid color getting farther and farther from the viewer. For my rendition, I wanted to really accentuate the sense of distance between layers, and also wanted to allow control over visual qualities of the paper (brightness, contrast) while establishing default values that would give the layers a gentle, earthy, construction paper-esque appearance on first load. To double down on this appearance I added a subtle texture of white noise to each "sheet".

To this end I decided to posterize the input field into fewer colors and used a simple Sobel-like hard drop shadow on all layers of color; to ensure a realistic and consistent hierarchy, drop shadows would be cast from blocks with higher channel totals (post-posterization) onto ones with lower totals. In essence, the highest-value colors appear at the highest altitude, with ties broken by higher R channel *and then failing that* higher G channel. I ultimately settled on posterization steps, shadow depth (how far away to sample for shadow casting), light direction (for shadow casting), paper brightness, and paper contrast as adjustables for the interaction method requirement. I had originally intended to also add an adjustable "rougness" to the edges of each layer that would make them appear more torn using large noise interference in the posterization process, but my camera caused so much static on its own that I decided it wasn't worth adding more (lest the image become unrecognizable).

My feedback was positive, with the predominant phrase being that I had created an "album cover generator" due to the posterization and noise effects especially when using low steps and very low depth; however, it seems that the original intent of the effect didn't make sense to him until I recommended using fewer steps and explained some of how it worked. In particular, I recieved the feedback that I probably should have kept the depth slider max far smaller, as using a higher number of steps ends up making the effect more of an engraving or very visually busy. Camera interference also causes the image to not "sit still" or have as neat layers as would have been desirable, resulting in an unfortunately prominent static-y tearing. Despite these issues, the sentiment overall seemed to be that the colors and overall cutout effect were fun and engaging to play with and try on different objects.