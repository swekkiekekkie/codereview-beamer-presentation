# Object-Oriented Programming in C#

## Advantages of Using Classes, Objects, and Encapsulation

Object-oriented programming (OOP) is a programming paradigm that uses classes and objects to create models based on the real world environment. OOP offers several advantages:

1. **Modularity**: The source code for a class can be written and maintained independently of the source code for other classes. Once created, an object can be easily passed around inside the system.
2. **Reusability**: Once a class is written, it can be used to create multiple objects. This is called instantiation.
3. **Pluggability and Debugging Ease**: If a particular object turns out to be problematic, it can be removed and replaced with a different object. This makes it easier to debug and maintain the code.

## Classes and Objects

Classes are blueprints for creating objects. Objects are instances of classes. Here is an example in C#:

```csharp
class Person {
    public string Name;
    public int Age;

    public void Greet() {
        Console.WriteLine("Hello, my name is " + Name);
    }
}

Person person = new Person();
person.Name = "Bob";
person.Age = 25;
person.Greet(); // Output: Hello, my name is Bob
```

In this example, `Person` is a class with two fields (`Name` and `Age`) and one method (`Greet`). An object of the `Person` class is created and its fields are set. The `Greet` method is then called on the object.

## Encapsulation

Encapsulation is the concept of hiding the internal state and requiring all interaction to be performed through an object's methods. This is done to protect the internal state of the object from unintended or harmful changes. Here is an example in C#:

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

In this example, the `BankAccount` class encapsulates the `balance` field by making it private. The `Deposit` and `GetBalance` methods provide controlled access to the `balance` field.

## Computational Thinking

Computational thinking is a problem-solving process that involves breaking down complex problems into smaller, more manageable subproblems. This approach allows us to tackle each subproblem individually, making it easier to find solutions and implement them in a programming language.

### Example: Managing a Bank Account

The `BankAccount` class encapsulates the problem of managing a bank account balance into subproblems by providing methods for depositing money and retrieving the balance.

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
