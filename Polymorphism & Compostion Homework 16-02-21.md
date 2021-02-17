
# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?
```
    - Polymorphism is the state of existing in different, independent forms.
```
2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
```
    - A method can be defined once and used, in different ways, by any classes that inherit that method.
	//Method is defined in interface
	public interface IConnect {
		public String connect(String data);
	}

	//Method is invoked in another class
	public String connect(String data) {
	return "connecting to network: " + data;
	}
	//Method is invoked in a further class in a different way
	public String connect(String data) {
	return  "connecting to "  +  data  +  " network";
	}  
```
3. What can we use to implement polymorphism in Java?
```
    - We can use interfaces and abstract classes to define methods that can be invoked in different ways determined by the class inheriting the methods.
```
4. How many 'forms' can an object take when using polymorphism?
```
    - An object can exist in as many forms as are required.
```
5. Give an example of when you could use polymorphism.
```
    - The same method could be used by different classes to enforce entry requirements, that are different for each class.
```


# Composition and Aggregation

6. What do we mean by 'composition' in reference to object-oriented programming?
```
    - In terms of composition in OOP, and object can be seen a a component part of another object.
```
7. When would you use composition? Provide a simple example in Java.
```
    - The wings of an aircraft would be useless if the aircraft was disassembled:
    class Wing {
    private int wingSpan;
    private String crossSection;
    private String constructionMaterial;
    ...
}

class Plane {
    private Wing wing;
    
    public Plane() {
        this.wing = new Wing();
    }
}
```
8. Give a difference between composition and aggregation?
```
    - With aggregation component objects are independent of the object they comprise. If the aeroplane is destroyed, the wing can be removed and re-used on another aeroplane.
```
9. What is/are the advantage(s) of using composition/aggregation?
```
    - Composition/aggregation is more flexible than inheritance. Object components can be changed or 'swapped-out' without the requirement to code an new hierarchy of inherited objects.
```
10. When using composition, when an object is destroyed, what happens to all the objects it is composed of?
```
    - They are also destroyed. For example; the aeroplane has taken 'ownership' of the wing so when the aeroplane is destroyed, so is the wing.
```
11. When using aggregation, when an object is destroyed, what happens to all the objects it is composed of?
```
    - The component objects are not destroyed. They can still be used by any other objects that they are components of.
```