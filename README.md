
using System;

namespace SampleCalculator;


	class Calculator
{
    static void Main(string[] args)
    {
        int num1; 
        int num2;
        float answer;
        string operation;


        Console.WriteLine("-----------------");
        Console.WriteLine("SIMPLE CALCULATOR");
        Console.WriteLine("-----------------");

        Console.WriteLine("ENTER YOUR FIRST NUMBER:- ");
        num1 = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("ENTER YOUR SECOND NUMBER:- ");
        num2 = Convert.ToInt32(Console.ReadLine());
        Console.WriteLine("CHOOSE AN OPERATION(+, -, /, *):- ");
        operation = Console.ReadLine();


        switch (operation)
        {
            case "+":
                answer = num1 + num2;
                Console.WriteLine("THE ANSWER IS :  " + answer);
                break;
            case "-":
                answer = num1 - num2;
                Console.WriteLine("THE ANSWER IS :  " + answer);
                break;
            case "*":
                answer = num1 * num2;
                Console.WriteLine("THE ANSWER IS :  " + answer);
                break;
            case "/":
                answer = num1 / num2;
                Console.WriteLine("THE ANSWER IS :  " + answer);
                break;
           default:
                answer = 0;
                break;
           
        }
        Console.WriteLine(num1.ToString() + " " + operation + " " + num2.ToString() + " = " + answer.ToString());
        while(true)
        {
            Console.WriteLine("DO YOU WANT TO CONTINUE [Y/N]? ");
            string choice = Console.ReadLine().ToUpper();
            if (choice == "Y")
                break;
            if (choice == "N")
                return;
        }
        


        Console.ReadLine();
    }
}
