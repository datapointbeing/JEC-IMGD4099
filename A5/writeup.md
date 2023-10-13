I added a color scheme and general visual theme inspired by Brian Moriarty's [Perlenspiel](https://ps3.perlenspiel.net/) engine and branding because I felt like it. This included applying a mask that 1. would make them slightly smaller than the respective spaces on the grid that they occupied, 2. round their corners slightly, and 3. inscribe a unique "glyph" on each of the five types of ants.

In addition to keeping the two types of ants that came with the simulation (the two that mirrored one another's behavior) as orange and yellow, I added:

- Green ants which turn _very_ slowly when not touching a pheromone -- and so trace broad, polygonal paths -- and upon hitting one turn abruptly and teleport to a pseudo-random space on the board, determined via white noise seeded with the current ant location and direction.
- Blue ants which are indecisive and jittery, constantly backtracking to where they've just been (0.5 increment turn). When they hit a pheromone, they turn a pseudorandom amount determined via white noise seeded with the current ant location.
- Violet ants which trace smooth curves over open space, using a turn increment of 0.33 to make medium-sized ellipse forms. When they hit a pheromone, they turn only a tenth of this amount, often causing them to "bounce" slightly back off the surface in question before continuing to curve. This forms an interesting path almost like the absolute value of a sine wave.

There's a small issue where a phantom ant (or possibly multiple) not included in the agent count are locked at the top left corner constantly adding/removing pheromone. At counts of 136 or higher this does not happen.
