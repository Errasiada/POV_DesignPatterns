# POV_DesignPatterns

Practice - Design Patterns

In this practice the objective is developing a design pattern by using the previous activities from WebGL.

In my case, I decided to implement a Prototype Design Pattern. The Prototype pattern is a creational design pattern that allows you to copy existing objects without making your code dependent on their classes. The class Coordinates2D has implemented a copy constructor and operator overloads for + and - that create new objects by copying the properties of existing objects. This allows for efficient object creation without the need for constructors with multiple arguments or a large number of constructors.

![image](https://user-images.githubusercontent.com/114673717/212970488-d3ee24ac-9d67-4cb4-9276-5b265930f922.png)

Sample (1). Here is the portion of code I took from Controller.razor.cs

One of the possible ways to improve the code snippet while maintaining the Prototype design pattern was adding an ICloneable interface to the class to make it more cloneable, and added the Clone method which returns the new object with the same properties as the original object.

![image](https://user-images.githubusercontent.com/114673717/212972347-c7663e1a-c592-4b51-9a33-d1b31eca6924.png)

Sample (2). Here is the ICloneable method implemented.

This way client can create a new object by calling the Clone() method on an existing Coordinates2D object. Also, made the class properties as read-write to make it more flexible for the client code. Also, you can validate the input values in constructors to make sure it's in the correct format.

To verify this pattern I applied the same structure to the class Angles2D. The class Angles2D has implemented a copy constructor and a constructor with two arguments, which set the Yaw and Pitch properties and validate the input values.

![image](https://user-images.githubusercontent.com/114673717/212973254-1b0527b3-cae8-497f-91de-090a2c73eafc.png)

Sample (3). Here is the public Angles2D

![image](https://user-images.githubusercontent.com/114673717/212973440-4669384c-2f95-4330-a19f-5b02c9367a0f.png)

Sample (4) Here is the Angles2D ICloneable.

To sum up, it took me a lot of time to figure out which pattern could fix better using the WebGL's pratices, as it was not easy to figure out in specially those projects. If we could at least apply the patterns in our personal projects or any other idea we wanted to implement giving us the chance to be a bit more creative in the resolution, would have been pretty much easier, understandable and even enjoyable. Which in this case, wasn't at all.

