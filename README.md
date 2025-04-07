using System;

// Abstract class
public abstract class Bird
{
    // Abstract method
    public abstract string MakeSound();
}

// Sparrow class inheriting from Bird
public class Sparrow : Bird
{
    public override string MakeSound()
    {
        return "Chirp.";
    }
}

// Pigeon class inheriting from Bird
public class Pigeon : Bird
{
    public override string MakeSound()
    {
        return "Coo.";
    }
}

// Main Program
class Program
{
    static void Main()
    {
        // Sparrow object
        Bird sparrow = new Sparrow();
        Console.WriteLine("Sparrow says: " + sparrow.MakeSound());

        // Pigeon object
        Bird pigeon = new Pigeon();
        Console.WriteLine("Pigeon says: " + pigeon.MakeSound());
    }
}
