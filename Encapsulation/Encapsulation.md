<h1 align="center">Encapsulation</h1>
<table>
  <th width="500">
<table width="100%" align="center">
  <th>Data Hiding</th>
  <th>Reusiblity</th>
  <tr>
    <td align="center" width="500">Restricting access to a class's attributes ensures that there is no unwanted access or data corruption; and makes for a more usable and intuitive class design by not revealing unneccessary details to the user of a class.</td>
    <td align="center" width="500">Encapsulating classes makes it so the class can easily be adapted to the potential input data types without having to rewrite code. </td>
  </tr>
</table>

    
<h3 align="center">A Basic Encapsulated class structure: </h3>


```
public class Pet 
{
	private int Id;
	private String name;
	private String description;
	private double price;
	private int categoryId;
	
	@Override
	public String toString() 
	{
		return "Pet [Id= " + Id + ", name= " + name + ", description= " + description + 
				", price= " + price + ", categoryId= " + categoryId + "]";
	} 
	
	// Getters and Setters
```


---
All class members are to be made private which would call for getters and if neccessary setters as well.
---
