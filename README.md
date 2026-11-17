```
using System;
using System.Data;

class Program
{
    static void Main()
    {
        Console.OutputEncoding = System.Text.Encoding.UTF8;
        Console.WriteLine("Введіть математичний вираз");
        string expression = Console.ReadLine();

        try
        {
            
            DataTable table = new DataTable();
            var result = table.Compute(expression, "");
            
            Console.WriteLine($"Відповідь програми: {result}");
        }
        catch (Exception)
        {
            Console.WriteLine("Помилка: некоректний математичний вираз.");
        }
    }
}
