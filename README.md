## About

[Manim](https://github.com/3b1b/manim) is an animation engine for explanatory math videos. It was written by Grant Sanderson and popularized by his YouTube channel, [3Blue1Brown](https://www.youtube.com/3blue1brown).

Animating technical concepts is traditionally pretty tedious since it can be difficult to make the animations precise enough to convey them accurately. Manim uses Python to generate animations programmatically, which makes it possible to specify exactly how each one should look.

## Installation

### Requirements

what we need to work with Manim,<br>

- LaTex- by MikTex  
	*for processing mathematical formulas*
- FFmpeg  
	*for rendering purpose*
- Cairo  
	*python graphics library*
- Sox *(optional)*  
	*for sound*

#### Steps
`pip must be installed along with Python`

<strong>1. MikTex</strong>

- Download installer from [MikTex.org](https://miktex.org)<br>
<em>MikTex.org > Downloads > (Your OS) > Installer(64bit | 32bit)</em>
- <em>After downloading the installer,</em> Installation through 2 steps:<br>
	<strong>1. Downloading MikTex</strong><br>
  Setup:<br> - Run setup as administrator <br> - Download recommended in root directory <br>
  <strong>2. Installing the downloaded</strong><br> - Run setup again <br> - Choose install and follow the default.<br>

<strong>2. FFmpeg</strong>

- Download build from https://ffmpeg.org/download.html
- Unzip file to a folder at root(For non-modification of data in that folder)
- Add `/bin` address to system `PATH`<br>
  *check by `$ ffmpeg` at command line.*

<strong>3. Sox</strong>

- Download link: https://sourceforge.net/projects/sox/
- Download to the root as well
- Add *sox.exe* address to `PATH`<br>
  *check by `$ sox`*

<strong>4. Cairo / pycairo</strong>

- Download link to binaries: https://www.lfd.uci.edu/~gohlke/pythonlibs/#pycairo
- <em>check for specific version for your 32/64 bit operating system & cpXX where XX for your python version. <br>
	i.e for python3.7 and 64bit os => consider **cp37** and **win_amd64.whl** </em>
- The downloaded file is of .whl extension. Open cmd prompt in the same terminal of the downladed file, **run** `python -m pip install <file_name>`.
<em>check by trying import in python shell `import cairo`.</em>

*once downloaded all the above, we have met the requirements to use manim. Now download the original github Manim by [3b1b](https://github.com/3b1b)*

<strong>5. Download Python plugins & manim</strong>

- Download link: https://github.com/3b1b/manim/tree/3b088b12843b7a4459fe71eba96b70edafb7aa78 <br>
  <em>this one is a old commit link but it works well enough, we can definitely go for new one [here](https://github.com/3b1b/manim).</em>
- Download repo as zip.
- Extract the zip
  <strong>Plugins:</strong>
- Remove pycairo from the requirements.txt > open cmd terminal here > <strong>run</strong> `python -m pip install -r requirements.txt`
- `python -m pip install pydub`<br>
  `python -m pip install pyreadline`
- <strong>Running manim:</strong><br>
  Goto <b>cmd</b> terminal > <b>run</b> `python -m manim example_scenes.py SquareToCircle -pl`<br>
  The `-p` flag in the command above is for previewing, meaning the video file will automatically open when it is done rendering. The `-l` flag is for a faster rendering at a lower quality.

### References:

Windows download guide: https://youtu.be/ZltiKHFWmv8v  
Official documentation in progress https://eulertour.com/docs/