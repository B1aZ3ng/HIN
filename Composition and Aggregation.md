ceeebbs
### Aggregation
- A weaker "has-a" relationship where a class (whole) contains references to other classes (parts), but the parts can exist independently of the whole.​
- Design: The containing class references component objects, which may be created or destroyed independently.​
- Example: A Library class contains a list of Book objects; books can exist outside the library (e.g., in another library or on their own).
- Purpose: Models loose coupling, allowing flexible and reusable object relationships.
asdf
- Parts have an independent lifecycle and can exist outside the whole.​
- Loose coupling; parts can be shared across multiple wholes or reused elsewhere.​
- Typically implemented by passing or referencing pre-existing component objects to the containing class​
- Example: Employee objects exist independently and are aggregated into the Department, which references them without controlling their lifecycle​
```python
class Engine:
	def __init__ (self,horsepower):
		self.horsepower = horsepower
	def start():
		return "Engine Started"

class Car:
	def __init__(model)
		self.model = model
		self.engine = Engine(6767)
	...
```
### Composition
- A strong "has-a" relationship where a class (whole) contains one or more instances of other classes (parts), and the parts are dependent on the whole for their lifecycle.​
- Design: The containing class creates and manages the component objects, which are typically destroyed when the containing object is destroyed.​
- Example: A Car class contains an Engine object; the engine is created when the car is instantiated and destroyed when the car is destroyed.​
- Purpose: Models tight coupling where parts are integral to the whole, ensuring cohesive object design.
asdf
- Parts are created and destroyed with the whole; they have no independent lifecycle.​
- Strong ownership; parts cannot belong to multiple wholes simultaneously.​
- Typically implemented by instantiating component objects within the containing class's constructor.​
- Example: The Car owns an Engine, which is tightly coupled and exists only as part of the Car.
