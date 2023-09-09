I love Voronoi tesselations, and have done some procedural rendering projects making heavy use of them, such as a stained-glass rendering process in Unreal. Something I had never done, however,
was program a tesselation into a single shader, since I never really knew a computationally efficient way to do so. As such when I was exploring Shadertoy and happened upon a few demos by Inigo
Quilez--one of the site’s creators--going in-depth on tesselations, I decided I wanted to play around with his work, and rewrote the Voronoi and noise functions he used in
[this shader](https://www.shadertoy.com/view/ldl3W8) in order to understand them.

I love the way Voronoi tesselations create such a distinctive mosaic look while being incredibly adaptive, customizable, and mathematically significant, and since this demo involved not only
creating a tesselation, but also calculating a large amount of useful coordinate and distance data per tile, I saw the opportunity to demonstrate how that data could be used to make a mosaic of
very interestingly styled tesselations; for some reason, what immediately came to mind was making a net of strangely-shaped “coins” with a restricted metallic palette and gradients, consistent
space between each, a simple bezel, and the viewer’s face inscribed on each one. My code is the same throughout my demo, so the visual is driven only by webcam, audio, and resolution/tile
offsets that automatically change with the time (using ``seconds()``).

My feedback from Milo on my video was very positive; he thought it was very cool, and seemed to enjoy how the full nature of the effect gradually became more clear over time as the tile
resolution increased. He enjoyed the palette and went from first questioning why certain blobs of color were in certain places to gradually recognizing features and finally realizing that the
entire field of tiles was displaying the webcam footage using tints. He did not comment on the engraving effect or gradients used, but were curious about why the tiles where my eyes were
appeared so blue; it was likely a combination of the blue light from my camera on my glasses, as well as the blue light filter on my lenses producing a blue-violet glare (I had also noticed this
effect in the footage and had been surprised by how prominent it was). No negative feedback was provided, though for my own part (based on my own critique) I had been anticipating some feedback
about the audio responsivity being somewhat inconsistent or the noise on each tile not “sticking” properly to each tile as it moved in space (or more generally the noise was constantly in motion,
like a “no signal” screen rather than a texture). He also didn’t seem to recognize the “coins” as coins, which I had anticipated given that I visually ended up moving more towards stylized coins
than real ones.
