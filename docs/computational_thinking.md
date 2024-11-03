# Computational Thinking

## Introduction
Computational thinking is a problem-solving process that involves breaking down complex problems into smaller, more manageable subproblems. This approach allows us to tackle each subproblem individually, making it easier to find solutions and implement them in a programming language.

## Breaking Problems into Subproblems
One of the key principles of computational thinking is breaking problems into subproblems. This can be done recursively until you arrive at primitives that your programming language or libraries have implemented. Here are some examples:

### Example 1: Control Flow
In the `docs/basic_programming_concepts.md` file, the concept of control flow is broken down into subproblems using if-else statements to handle different conditions.
```csharp
if (age > 18) {
    Console.WriteLine("Adult");
} else {
    Console.WriteLine("Minor");
}
```

### Example 2: Swapping Variables
In the `docs/functions_and_methods.md` file, the `Swap` function is an example of breaking down the problem of swapping two variables into smaller steps: storing one value in a temporary variable, assigning the second value to the first variable, and then assigning the temporary value to the second variable.
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

### Example 3: Managing a Bank Account
In the `docs/object_oriented_programming.md` file, the `BankAccount` class encapsulates the problem of managing a bank account balance into subproblems by providing methods for depositing money and retrieving the balance.
```csharp
class BankAccount {
    private double balance;

    public void Deposit(double amount) {
        if (amount > 0) {
            balance += amount;
        }
    }

    public double GetBalance() {
        return balance;
    }
}

BankAccount account = new BankAccount();
account.Deposit(100);
Console.WriteLine(account.GetBalance()); // Output: 100
```

### Example 4: Everyday Tasks
In the `presentation/sections/programs_no_control_flow_or_variables.tex` file, everyday tasks like brushing your teeth, cooking, making a cup of coffee, and getting dressed are broken down into smaller steps, each represented as a function call. For example, brushing your teeth is broken down into steps like `wetToothbrush()`, `applyToothpaste()`, `brushTeeth()`, `rinseMouth()`, and `rinseToothbrush()`.
```csharp
wetToothbrush();
applyToothpaste();
brushTeeth();
rinseMouth();
rinseToothbrush();
```

## Recursion
Recursion is a powerful technique in computational thinking where a function calls itself to solve a problem. This is particularly useful for problems that can be broken down into smaller, similar subproblems. Here is an example of a recursive function in C# that calculates the factorial of a number:
```csharp
int Factorial(int n) {
    if (n <= 1) {
        return 1;
    } else {
        return n * Factorial(n - 1);
    }
}

int result = Factorial(5);
Console.WriteLine(result); // Output: 120
```
