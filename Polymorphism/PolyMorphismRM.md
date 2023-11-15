<h1 align="center">Polymorphism</h1>

---
The ability of an object to take on multiple forms at runtime. The objects that it may 'morph' into must have an "IS-A" relationship with the base class it inherits from, as seen from this UML design where the electric and petrol car classes "IS-A" type of Car.
---

<img src="https://github.com/phollenback/Skills-Overview/assets/145724342/1374373b-6601-4c2c-9d4d-06294aa2eefe" width="1000">


<table>
  <th>The car base class is what would be defined when the object is being referenced if say for example the user of this class hierarchy was printing a overridden toString format of one of each instance of the petrol car and electric car classes. At runtime, the "Car" reference would morph into whatever object is being printed and outprint the correct data that goes along with the car type.</th>
</table>


```
private static void displayArea(ShapeBase shape)
	{
		// Show polymorphism action by getting the Shapes name and area
		System.out.println("This is a shape of type " + shape.getClass());
		System.out.println("This is a shape named " + shape.getName() + " with an area of " + shape.calculateArea());
	}
```
<table>
  <th>
    In this example each type of the "ShapeBase" class has a different definition for the calculateArea method inherited from the "ShapeBase" interface. This allows the method parameter to morph at runtime and correctly print the correct area for each type of shape defined in an array being iterated over calling displayArea.
  </th>
</table>
<br>
<table>
<tr>
	<th width="500">Overridding</th>
	<th width="500">Overloading</th>
</tr>
<tr>
	<td width="500" align="center">Method overriding allows the types of a base class to create a type-specific implementation of the bahavior that goes with a certain group of objects, and will be ran when the object morphs at runtime.</td>
 	<td width="500" align="center">When overloading methods, it enhances polymorphic behavior even futher. By implementing multiple methods with different arguements and return types it allows for any parameter to be passed in order to produce a desireable result.</td>
</tr>
  
</table>
