using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        List<int> numbers = new List<int>();

      
        for (int i = 0; i < 10; i++)
        {
            Console.Write("Enter number " + (i + 1) + ": ");
            int number = Convert.ToInt32(Console.ReadLine());

            numbers.Add(number);
        }

        int largest = numbers[0];
        int smallest = numbers[0];

        int evenCount = 0;
        int oddCount = 0;

        foreach (int number in numbers)
        {
            
            if (number > largest)
            {
                largest = number;
            }

            // Find the smallest number
            if (number < smallest)
            {
                smallest = number;
            }

          
            if (number % 2 == 0)
            {
                evenCount++;
            }
            else
            {
                oddCount++;
            }
        }

        Console.WriteLine("\n--- Results ---");
        Console.WriteLine("Largest number: " + largest);
        Console.WriteLine("Smallest number: " + smallest);
        Console.WriteLine("Even numbers: " + evenCount);
        Console.WriteLine("Odd numbers: " + oddCount);
    }
}
