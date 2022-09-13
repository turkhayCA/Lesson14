# Lesson14
Project review and Delegates first part

For reading : <br>
1 - https://www.completecsharptutorial.com/basic/c-delegate-tutorial-with-easy-example.php <br>
2 - https://www.geeksforgeeks.org/c-sharp-delegates/ <br>
3 - https://www.infoworld.com/article/2996770/how-to-work-with-delegates-in-csharp.html <br>


Tasks: <br>
1 - We have User (Name, Surname, Age, Country) class and list of User objects  <br>
a) Write a method to generate about 10 user objects and return them as list. <br>
b) Find all users that age is greater than 20 and print them as "Name Surname Age Country" format. ex: "Parviz Parvizzada 21 Azerbaijan" <br>
c) Remove all users that belongs to Turkey and Age is lower than 10  <br>

2 - 

using System;
 
namespace DelegatesAndEvents
{
 
  public class DelegateExercises
  {
    public delegate int MyDelegate(int intValue);
 
    public int Method1(int intMethod1)
    {
      return intMethod1*2;
    }
 
    public int Method2(int intMethod2)
    {
      return intMethod2*10;
    }
 
    public void Method3()
    {
      MyDelegate myDelegate = new MyDelegate(Method1);
      int result1 = myDelegate(10);
      System.Console.WriteLine(result1);
      myDelegate = new MyDelegate(Method2);
      int result2 = myDelegate(10);
      System.Console.WriteLine(result2);
    }
  }
 
  public class Program
  {
    public static void Main()
    {
      DelegateExercises delegateExercises = new DelegateExercises();
      delegateExercises.Method3();
      Console.ReadLine();
 
    }
  }
}

---  Find Output for me and explain why
