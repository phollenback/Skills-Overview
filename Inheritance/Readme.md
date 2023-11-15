<h1 align="center">Inheritence</h1>
<h3 align="center">How can inheritence be modeled in a UML Diagram?</h3>
<table>
  <th width="500">
    <img src="https://github.com/phollenback/Skills-Overview/assets/145724342/c2fc46dd-a616-4d22-bf1c-3c459ab78339" width="1000" height="300">
  </th>
  <th width="500">
    
   - The 'base' of any inheritence relationship starts with the "Base" or "Parent" class. In this example, the 'salable'
    class is the bass of the three classes beneath it.


--------------------------

   -   Because the bottom three classes have an 'extends' line realationship to there base class, this means that all three inherit each       property and method its parent class contains.
   
  </th>
</table>
<table>
  <th width="500">

    
-  Inheritence is an important principle because it helps to model real world relationships between objects. In this example the UML illustrates that the "Oval", "Circle" and "Triangle" class are types of "Shape".


--------------------


-  Inheritence is also a powerful tool when combined with the concepts of 'overriding' and 'overloading' methods alongside the implementation of interfaces. This allows the child classes to provide unique behaviors as well as handle specific data types when developing derived classes.
  </th>
  <th width="565">
    <img src="https://github.com/phollenback/Skills-Overview/assets/145724342/d54f9078-ae26-4980-a560-3b1d7709fb01)" width="1000" height="375">
  </th>
</table>

<h3 align="center">Implementation within a project</h3>

```
public class Circle extends ShapeBase {

	private double radius;

	public Circle(String name, int width, int height, double radius) 
	{
		super(name, width, height);
		this.radius = radius;
	}
	@Override
	public double calculateArea() 
	{
		
		return 3.14 * this.radius;
	}

}
```
This code exemplifies the significance of inherited classes. Because the circle class inherits from the base "Shape" class, it has some, but not all of the correct properties to implement the method within the "ShapeInterface" class. Since the name, width, and height properties can be defined using the "super" keyword to access its base class constructor, as well as add a property (in this case radius) in order to correctly calculate the area of the circle.
