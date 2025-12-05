# Interface

## Aim:
To Develop a small bank application by declaring deposit() and withdrawal() as abstract methods in the interface. Get the choice from the user whether to perform withdrawal or deposit operation. After the operation completes, display the balance amount.

## Algorithm:
Step 1:
Create an interface.

Step 2:
Create a child class.

Step 3:
Declare 2 functions deposit() and withdrawal() as abstract methods in the interface.

Step 4:
Create those 2 functions in the child class and perform respective operation.

Step 4:
Use if-else conditional statement to get the choice from the user whether to perform withdrawal or deposit operation.

Step 5:
After performing the functions display the remaining balance of the user.

## Program:
```python
using System;
public interface Bank
{
    void deposit();
    void withdrawal();
}

public class Example : Bank
{
    int amount, ch, balance = 5000;
    public Example()
    {
        Console.WriteLine("Press 1 to Deposit\nPress 2 to Withdraw");
        ch = Convert.ToInt32(Console.ReadLine());
        if (ch == 1)
        {
            deposit();
        }
        else
        {
            withdrawal();
        }
    }
    public void withdrawal()
    {
        Console.WriteLine("Enter the amount to be withdrawn");
        int amount = Convert.ToInt32(Console.ReadLine());
        balance -= amount;
        Console.WriteLine("Balance Amount : " +balance);
    }

    public void deposit()
    {
        Console.WriteLine("Enter the amount to be deposited");
        int amount = Convert.ToInt32(Console.ReadLine());
        balance += amount;
        Console.WriteLine("Balance Amount : "+balance);
    }
}

public class Hello
{
    public static void Main()
    {
        Example c = new Example();
        
    }
}
```

## Output:
<img width="677" alt="image" src="https://user-images.githubusercontent.com/75235554/172896984-e48f0f86-5711-45db-94c3-1a989c947e98.png">


## Result:
Thus, a C# program was developed for a bank application using interface.
