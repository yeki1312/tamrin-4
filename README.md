# tamrin-4using System;

class Program
{
    static void Main()
    {
        int[] numbers = new int[5];
        bool foundTwo = false;
        int position = -1;

        Console.WriteLine("لطفاً 5 عدد وارد کنید:");

        // دریافت 5 عدد از کاربر
        for (int i = 0; i < 5; i++)
        {
            Console.Write($"عدد {i + 1}: ");
            numbers[i] = Convert.ToInt32(Console.ReadLine());
        }

        // بررسی وجود عدد 2
        for (int i = 0; i < numbers.Length; i++)
        {
            if (numbers[i] == 2)
            {
                foundTwo = true;
                position = i + 1; // موقعیت را 1-indexed نمایش می‌دهیم
                break;
            }
        }

        // نمایش نتیجه
        if (foundTwo)
        {
            Console.WriteLine($"عدد 2 در موقعیت {position} وجود دارد.");
        }
        else
        {
            Console.WriteLine("عدد 2 در بین اعداد وجود ندارد.");
        }
    }
}
