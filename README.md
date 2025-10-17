// Question 1
// Imagine you are developing a basic calculator for a financial application.
// You need to calculate the total sum of all the transactions recorded in a day.
// Write a C# program to find the sum of all elements in an integer array using a loop.

using System;

class FinancialCalculator
{
    static void Main()
    {
        int[] transactions = { 200, -150, 340, 500, -100 };
        int totalSum = 0;
        for (int i = 0; i < transactions.Length; i++)
        {
            totalSum += transactions[i];
        }
        Console.WriteLine("Total sum of transactions: " + totalSum);
    }
}

// Question 2
// You are working on an analytics tool that needs to find the average score of a class from a list of floating-point numbers.
// Create a C# program that calculates the average of values in a floating-point array using a loop.

using System;

class AverageCalculator
{
    static void Main()
    {
        float[] scores = { 85.5f, 90.3f, 78.4f, 88.9f, 92.1f };
        float total = 0f;
        for (int i = 0; i < scores.Length; i++)
        {
            total += scores[i];
        }
        float average = total / scores.Length;
        Console.WriteLine("Average score of the class: " + average);
    }
}

// Question 3
// You are tasked with developing a feature for an inventory management system that finds the most expensive item in stock.

using System;

class InventoryManagement
{
    static void Main()
    {
        int[] prices = { 1500, 2300, 999, 3200, 1750 };
        int maxPrice = prices[0];
        for (int i = 1; i < prices.Length; i++)
        {
            if (prices[i] > maxPrice)
            {
                maxPrice = prices[i];
            }
        }
        Console.WriteLine("Most expensive item price: " + maxPrice);
    }
}

// Question 4
// You need to generate a report for a survey that counts the number of male and female participants
// based on their unique codes (even for males, odd for females).

using System;

class SurveyReport
{
    static void Main()
    {
        int[] participantCodes = { 102, 215, 324, 453, 536 };
        int maleCount = 0;
        int femaleCount = 0;
        for (int i = 0; i < participantCodes.Length; i++)
        {
            if (participantCodes[i] % 2 == 0)
            {
                maleCount++;
            }
            else
            {
                femaleCount++;
            }
        }
        Console.WriteLine("Number of male participants: " + maleCount);
        Console.WriteLine("Number of female participants: " + femaleCount);
    }
}

// Question 5
// You are building a feature for an app that displays the recent search history in reverse order.

using System;

class SearchHistoryApp
{
    static void Main()
    {
        int[] searchHistory = { 101, 202, 303, 404, 505 };
        Console.WriteLine("Original search history:");
        for (int i = 0; i < searchHistory.Length; i++)
        {
            Console.Write(searchHistory[i] + " ");
        }
        Console.WriteLine("\n\nReversed search history:");
        for (int i = searchHistory.Length - 1; i >= 0; i--)
        {
            Console.Write(searchHistory[i] + " ");
        }
        Console.WriteLine();
    }
}

// Question 6
// You are developing a simulation tool where you need to adjust the measurements by a certain factor.

using System;

class MeasurementScaler
{
    static void Main()
    {
        int[] measurements = { 2, 4, 6, 8 };
        int factor = 3;
        Console.WriteLine("Original measurements:");
        for (int i = 0; i < measurements.Length; i++)
        {
            Console.Write(measurements[i] + " ");
        }
        for (int i = 0; i < measurements.Length; i++)
        {
            measurements[i] = measurements[i] * factor;
        }
        Console.WriteLine("\n\nScaled measurements (factor " + factor + "):");
        for (int i = 0; i < measurements.Length; i++)
        {
            Console.Write(measurements[i] + " ");
        }
        Console.WriteLine();
    }
}

// Question 7
// You are tasked with creating a search function for a library system that finds a specific book by its code.

using System;

class LibrarySearch
{
    static void Main()
    {
        int[] bookCodes = { 101, 203, 304, 405, 506 };
        int searchCode = 304;
        int foundIndex = -1;
        for (int i = 0; i < bookCodes.Length; i++)
        {
            if (bookCodes[i] == searchCode)
            {
                foundIndex = i;
                break;
            }
        }
        if (foundIndex != -1)
        {
            Console.WriteLine("Book code " + searchCode + " found at index: " + foundIndex);
        }
        else
        {
            Console.WriteLine("Book code " + searchCode + " not found in the list.");
        }
    }
}

// Question 8
// In an academic project, you need to identify the second smallest grade in a list of student grades.

using System;
using System.Collections.Generic;

class GradeAnalyzer
{
    static void Main()
    {
        int[] grades = { 56, 78, 89, 45, 67 };
        for (int i = 0; i < grades.Length - 1; i++)
        {
            for (int j = i + 1; j < grades.Length; j++)
            {
                if (grades[i] > grades[j])
                {
                    int temp = grades[i];
                    grades[i] = grades[j];
                    grades[j] = temp;
                }
            }
        }
        int smallest = grades[0];
        int secondSmallest = -1;
        for (int i = 1; i < grades.Length; i++)
        {
            if (grades[i] != smallest)
            {
                secondSmallest = grades[i];
                break;
            }
        }
        if (secondSmallest != -1)
        {
            Console.WriteLine("Second smallest grade: " + secondSmallest);
        }
        else
        {
            Console.WriteLine("All grades are the same. No second smallest grade found.");
        }
    }
}

// Question 9
// You are improving a system where you need to clean up duplicate entries from a list of IDs.

using System;
using System.Collections.Generic;

class DuplicateRemover
{
    static void Main()
    {
        int[] ids = { 102, 215, 102, 324, 215 };
        List<int> uniqueIds = new List<int>();
        for (int i = 0; i < ids.Length; i++)
        {
            if (!uniqueIds.Contains(ids[i]))
            {
                uniqueIds.Add(ids[i]);
            }
        }
        Console.WriteLine("Unique IDs after removing duplicates:");
        foreach (int id in uniqueIds)
        {
            Console.Write(id + " ");
        }
        Console.WriteLine();
    }
}

// Question 10
// You are developing a function that finds common elements in two different datasets for an analytics application.

using System;
using System.Collections.Generic;

class CommonElementsFinder
{
    static void Main()
    {
        int[] dataset1 = { 1, 2, 3, 4, 5 };
        int[] dataset2 = { 3, 4, 5, 6, 7 };
        List<int> common = new List<int>();
        for (int i = 0; i < dataset1.Length; i++)
        {
            for (int j = 0; j < dataset2.Length; j++)
            {
                if (dataset1[i] == dataset2[j])
                {
                    if (!common.Contains(dataset1[i]))
                    {
                        common.Add(dataset1[i]);
                    }
                    break;
                }
            }
        }
        Console.WriteLine("Common elements:");
        foreach (int value in common)
        {
            Console.Write(value + " ");
        }
        Console.WriteLine();
    }
}
