## About

[Manim](https://github.com/3b1b/manim) is an animation engine for explanatory math videos. It was written by Grant Sanderson and popularized by his YouTube channel, [3Blue1Brown](https://www.youtube.com/3blue1brown).

Animating technical concepts is traditionally pretty tedious since it can be difficult to make the animations precise enough to convey them accurately. Manim uses Python to generate animations programmatically, which makes it possible to specify exactly how each one should look.

## Installation

### Requirements

what we need to work with Manim,<br>
<ul>
	<li>LaTex- by MikTex</li>
	<p>for processing mathematical formulas</p>
	<li>FFmpeg</li>
	<p>for rendering purpose</p>
	<li>Cairo</li>
	<p>python graphics library</p>
	<li>Sox *(optional)*</li>
	<p>for sound</p>
</ul>

#### Steps

`pip must be installed along with Python`

<strong>1. MikTex</strong>
<ol>
	<li>Download installer from [MikTex.org](https://miktex.org)<br>
	<em>MikTex.org > Downloads > (Your OS)  > Installer(64bit | 32bit)</em>
	</li>
	<li><em>After downloading the installer,</em> Installation through 2 steps:<br>
	**1. Downloading MikTex**<br>
	Setup:<br>
		- Run setup as administrator <br>
		- Download recommended in root directory <br>
	**2. Installing the downloaded**<br>
		- Run setup again <br>
		- Choose install and follow the default.<br>
	</li>
</ol>

<strong>2. FFmpeg</strong>
<ol>
	<li>Download build from https://ffmpeg.org/download.html</li>
	<li>Unzip file to a folder at root(For non-modification of data in that folder)</li>
	<li>Add `/bin` address to system `PATH`<br>
	*check by typin `$ ffmpeg` at command line.*
	</li>
</ol>

<strong>3. Sox</strong>
<ol>
	<li>Download link: https://sourceforge.net/projects/sox/</li>
	<li>Download to the root as well</li>
	<li>Add *sox.exe* address to `PATH`</li>
	*check by `$ sox`*
</ol>

<strong>4. Cairo / pycairo</strong>
<ol>
	<li>Download link to binaries: https://www.lfd.uci.edu/~gohlke/pythonlibs/#pycairo</li>
	<li><em>check for specific version for your 32/64 bit operating system & cpXX where XX for your python version. <br> i.e for python3.7 and 64bit os => consider **cp37** and **win_amd64.whl** </em></li>
	<li>The downloaded file is of .whl extension. Open cmd prompt in the same terminal of the downladed file, **run** `python -m pip install <file_name>`.</li>
	<em>check by trying import in python shell `import cairo`.</em>
</ol>

*once downloaded all the above, we have met the requirements to use manim. Now download the original github Manim by [3b1b](https://github.com/3b1b)*

<strong>5. Download Python plugins & manim</strong>
<ol>
	<li>Download link: https://github.com/3b1b/manim/tree/3b088b12843b7a4459fe71eba96b70edafb7aa78 <br>
		<em>this one is a old commit link but it works well enough, we can definitely go for new one [here](https://github.com/3b1b/manim).</em></li>
		<li>Download repo as zip</li>
		<li>Extract the zip</li>
		<strong>Plugins:</strong>
		<li>Remove pycairo from the requirements.txt > open cmd terminal here > **run** `python -m pip install -r requirements.txt`</li>
		<li>`python -m pip install pydub`<br>
		`python -m pip install pyreadline`</li>
		<li><strong>Running manim:</strong><br>
			Goto **cmd** terminal > **run** `python -m manim example_scenes.py SquareToCircle -pl`<br>
		The `-p` flag in the command above is for previewing, meaning the video file will automatically open when it is done rendering. The `-l` flag is for a faster rendering at a lower quality.</li>
</ol>


### References:
<li>Windows download guide: https://youtu.be/ZltiKHFWmv8</li>
<li>Official documentation in progress [https://eulertour.com/docs/](https://eulertour.com/docs/){:target="_blank"}</li>
