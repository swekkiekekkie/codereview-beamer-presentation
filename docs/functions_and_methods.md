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
