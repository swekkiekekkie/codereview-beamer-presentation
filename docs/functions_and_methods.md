# Functions and Methods in C#

## Defining and Calling Functions
Functions are blocks of code that perform a specific task. In C#, you can define and call functions as follows:
```csharp
int Add(int a, int b) {
    return a + b;
}

int result = Add(3, 4);
Console.WriteLine(result); // Output: 7
```

## Passing Arguments to Parameters
Arguments are values passed to a function when it is called. Parameters are variables that hold the values of the arguments. Here is an example in C#:
```csharp
void Greet(string name) {
    Console.WriteLine("Hello, " + name);
}

Greet("Alice"); // Output: Hello, Alice
```

## Common Confusions
One common confusion is understanding how arguments are passed to parameters. When a function is called, the arguments are loaded into the variables declared by the parameters in the function signature. Here is an example to illustrate this concept:
```csharp
void Swap(ref int a, ref int b) {
    int temp = a;
    a = b;
    b = temp;
}

int x = 5;
int y = 10;
Swap(ref x, ref y);
Console.WriteLine("x: " + x + ", y: " + y); // Output: x: 10, y: 5
```
In this example, the `Swap` function takes two parameters by reference using the `ref` keyword. This allows the function to modify the original variables passed as arguments.

## Functions as Shorthands
Functions can be used as shorthands to avoid repeating yourself. This can be demonstrated by first annotating code with comments, where statements are grouped, each group with its own comment. Then the statements are put into functions and the comments are replaced with function calls that are as descriptive as the comments.

### Example: Annotated Code
Let's consider an example where we have a piece of code that performs a series of operations. Initially, we will annotate the code with comments to group related statements together.

```csharp
// Calculate the area of a rectangle
double length = 5.0;
double width = 3.0;
double area = length * width;
Console.WriteLine("Area: " + area);

// Calculate the perimeter of a rectangle
double perimeter = 2 * (length + width);
Console.WriteLine("Perimeter: " + perimeter);
```

In the above code, we have two groups of statements: one for calculating the area of a rectangle and another for calculating the perimeter. Each group is annotated with a comment to describe its purpose.

### Example: Using Functions
Now, let's refactor the code by putting the statements into functions and replacing the comments with function calls.

```csharp
double CalculateArea(double length, double width) {
    return length * width;
}

double CalculatePerimeter(double length, double width) {
    return 2 * (length + width);
}

double length = 5.0;
double width = 3.0;

double area = CalculateArea(length, width);
Console.WriteLine("Area: " + area);

double perimeter = CalculatePerimeter(length, width);
Console.WriteLine("Perimeter: " + perimeter);
```

In the refactored code, we have defined two functions: `CalculateArea` and `CalculatePerimeter`. These functions encapsulate the logic for calculating the area and perimeter of a rectangle, respectively. By calling these functions, we avoid repeating the same code and make the program more modular and readable.

## Reference
For more details on the allowed and disallowed constructs at this phase, refer to the [Functions and Methods](teaching_order.md#functions-and-methods) section in the `docs/teaching_order.md` file.
