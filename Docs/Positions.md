## Positions
1. Absolute <br>
	- `.to_edge(option, buff)`<br>
	for edge of screens <br>
	moves **with respect to the current positions** i.e if corrently the object is at the TOP and told to move LEFT, it will get placed to TOP-LEFT corner<br>
	**option**
		- UP
		- DOWN
		- LEFT
		- RIGHT

	- `.to_corner(option)`
	**option**
		- UR
		- UL
		- DR
		- DL

> **buff**- float that measures the distance of object, here **lesser the value, the closer to the edge**.

2. Relative <br>
	- `.move_to(option)`<br>
	does overlap two objects
		- option = `vector`<br>
		following format can be used <br>
		`vector = np.array([x, y, z])` **OR**<br>
		`vector = x*LEFT/RIGHT + y*UP/DOWN`<br>
		- option = `ref_object.get_center()+ vector`

	- `.next_to(ref_object, Edge_of_ref, buff)`<br>
	don't overlap two objects <br>
	measures the distance from the side of reference_object and not center of it like .move_to().
	
	- `.shift(option)`<br>
	shifts the object from it's current position. <br>
	**option**
		- RIGHT
		- LEFT
		- UP
		- DOWN

## Rotations
- `.rotate(radian/degrees, about_point)`
radian like `PI/4`, where `PI` is a constant. <br>
degrees like `45*DEGREES` <br>
when using any point as a reference to rotate, `about_point` parameter is passed. <br>
- `.flip(DIRECTION)`<br>
takes direction of reflection of the mirror object. <br>

