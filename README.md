# Cup Swapper
Code to emulate a cup swapping game using 3blue1brown's animation engine [Manim](https://www.github.com/3b1b/manim/).

The [init](__init__.py) file contains raw code to find the last cup, which is not used in the animation code.

The [scene.py](scene.py) file, when ran with [Manim](https://www.github.com/3b1b/manim/), will generate a video in /media/videos/scene/[resolution]/ that contains the animation of the cups being moved, and a folder containing videos for each individual animation in the sequence.

Both pieces of code run by giving them  a list of paths, which could look like this:

    ["AB","BC","AC","BA"]
    ["CA","BA","BA","BC","AB","CA"]

   where each "path" in the list contains two letters referring to the cups to be swapped. In the [init](__init__.py) file, it takes it as an argument to the `swapper()` function, and in the [scene.py](scene.py) file, it takes it as the `PATHS` variable defined near the top if the file.

To run the scene.py file so that it generates the video, you will first need to clone the repository to your local computer and install [Manim](https://www.github.com/3b1b/manim/) (instructions for installing [Manim](https://www.github.com/3b1b/manim/) can be found [here](https://docs.manim.community/en/stable/installation.html)). After this, open cmd, navigate to the directory containing [scene.py](scene.py), and run this command: `python -m manim scene.py CupSwapperScene -q h` (can also be found commented at the bottom of [scene.py](scene.py),). The code will then generate the video.

If you want the resolution to change, the syntax is `-q [l|m|h|p|k]`. To see the respective values of these letters, run the command `python -m manim render --help` and navigate down to `Render Options:` where you will find `-q, --quality`. There it will say which resolution and framerate the letters refer to.
