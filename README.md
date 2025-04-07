1 ამოცანა 

ფანქარს დააჭირე და მერე დააკოპირე

using System;

class Program
{
    static void Main()
    {
        // ცვლადების ინიციალიზაცია
        int quantity = 10;
        string itemName = "ყავა";

        // ციკლი 1-დან 5-მდე
        for (int i = 1; i <= 5; i++)
        {
            Console.WriteLine($"პროდუქტი: {itemName}, იტერაცია: {i}");
        }
    }
}

