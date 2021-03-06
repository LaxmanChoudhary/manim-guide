## Basics
### Imports
Start with the imports, as manim is not a heavy consuming library we can just import all the functionalities available.  
1. Create a new .py file that contains all the required imported to it.<br>
`touch all-imports.py`<br>
*example [file](all-imports.py) is present in the same folder*

2. Then, we can use this file for directly importing all functionalities.<br>
`from all-import import *`<br>

### Common functionalities
#### Main Class
- `class SCENE-FUNCTION(Scene):`<br>
Every manim program is contained in a python class. <br>
**Render order is Top -> Bottom**

#### Config
- `CONFIG = { }`<br>
A dictionary containing the declaration of objects.<br>
It let's us create a base class and reuse it in different scenes by changing the objects in ***CONFIG*** itself.<br>

#### Functions
- `def construct(self):`<br>
A class should contain a contruct function defined, where whatever is to be rendered is mentioned.

- **Built-in functions**<br>
	- `self.add(object)`<br>
	Simply add the object to the scene without any animations.
	- `self.play(object)` | `.play(Transition(object))`<br>
	Render the objects with animations.Transformations functions can be passed to change animations for entry, exit and so.
	- `self.remove(object)`<br>
	remove object from the scene.
	- `self.wait(time)`<br>
	Adds pause to the animation
		- time- in sec

*Here `self` refers to the current scene displayed*

**eg**
```python
class WriteText(Scene): 
    def construct(self): 
        text = TextMobject("This is a regular text")
        self.play(Write(text))
        self.wait(3)
```

## Index
- [Text Formats](./Text/text_formats.md)