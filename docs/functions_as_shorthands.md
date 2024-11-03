# Functions as Shorthands

## Introduction
Functions are a fundamental concept in programming that allow you to group a set of statements into a single unit. This unit can then be called and executed whenever needed. Functions help in avoiding repetition and making the code more modular and readable.

## Avoiding Repetition
One of the main advantages of using functions is to avoid repeating the same code multiple times. By defining a function once and calling it whenever needed, you can reduce redundancy and make your code more maintainable.

## Example: Annotated Code
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

## Example: Using Functions
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

## Conclusion
Using functions as shorthands is a powerful technique to avoid repetition and improve the maintainability of your code. By grouping related statements into functions, you can make your code more modular, readable, and easier to maintain.

## Reference
For more details on the allowed and disallowed constructs at this phase, refer to the [Functions as Shorthands](teaching_order.md#functions-as-shorthands) section in the `docs/teaching_order.md` file.
