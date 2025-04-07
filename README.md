using System;

public class Item
{
    // Protected property
    protected double Price { get; set; }

    // Constructor
    public Item()
    {
        Price = 0;
    }
}

public class Fruit : Item
{
    // Private fields
    private double _weightInKg;
    private double _priceOfOneKg;

    // Properties
    public double WeightInKg
    {
        get { return _weightInKg; }
        set { _weightInKg = value; }
    }

    public double PriceOfOneKg
    {
        get { return _priceOfOneKg; }
        set { _priceOfOneKg = value; }
    }

    // Overloaded method
    public double CalculateTotalPrice(double weightInKg, double priceOfOneKg)
    {
        _weightInKg = weightInKg;
        _priceOfOneKg = priceOfOneKg;
        Price = _weightInKg * _priceOfOneKg;
        return Price;
    }
}

public class Electronics : Item
{
    // Private fields
    private int _quantity;
    private double _oneUnitPrice;

    // Properties
    public int Quantity
    {
        get { return _quantity; }
        set { _quantity = value; }
    }

    public double OneUnitPrice
    {
        get { return _oneUnitPrice; }
        set { _oneUnitPrice = value; }
    }

    // Overloaded method
    public double CalculateTotalPrice(int quantity, double oneUnitPrice)
    {
        _quantity = quantity;
        _oneUnitPrice = oneUnitPrice;
        Price = _quantity * _oneUnitPrice;
        return Price;
    }
}

class Program
{
    static void Main()
    {
        // Fruit object
        Fruit banana = new Fruit();
        double fruitTotal = banana.CalculateTotalPrice(3.5, 2.0); // 3.5 კგ * 2 ლარი

        // Electronics object
        Electronics laptop = new Electronics();
        double electronicsTotal = laptop.CalculateTotalPrice(1, 1200.0); // 1 ცალი * 1200 ლარი

        // Print results
        Console.WriteLine($"ხილის ჯამური ფასი: {fruitTotal} ლარი");
        Console.WriteLine($"ელექტრონიკის ჯამური ფასი: {electronicsTotal} ლარი");
    }
}
