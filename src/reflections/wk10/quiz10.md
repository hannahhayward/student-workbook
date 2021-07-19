# C# Fundamentals


**1.** What is the purpose of a `namespace`?
<!-- enter you answer in the space below -->
```
it provides a scope of what is inside of the document
```
**2.** What is the difference between a `class` and a `struct`?
<!-- enter you answer in the space below -->
```
a struct is a value type and a class is reference type
```
**3.** What is the method that returns an instance of a class, yet it has no return type?
<!-- enter you answer in the space below -->
```
a return void
```
## Example 1
```c#
abstract class Car
{
  ...
  public virtual string Start()
  {
    return "Vroooom";
  }
}
```
**5.** In the example what is the access modifier of the `Start()` method?
<!-- enter you answer in the space below -->
```
public
```
**6.** In the example what is `string` an indication of?
<!-- enter you answer in the space below -->
```
the data type that will be returned
```
**7.** In the example what is `abstract` preventing?
<!-- enter you answer in the space below -->
```
creating objects
```
**8.** In the example what is the purpose of `virtual`?
<!-- enter you answer in the space below -->
```
allows the class to be overridden by the class it inherents
```
**9.** Name four access modifiers:
<!-- enter you answer in the space below -->
```
private, public, protected, internal
```
**10.** If you set a class or method to private, what can access it?
<!-- enter you answer in the space below -->
```
the member functions inside the class
```