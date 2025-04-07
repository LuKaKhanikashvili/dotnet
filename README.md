2ამოცანა


using System;

public class Employee
{
    // private field
    private string _employeeName;

    // public property
    public string Salary { get; set; }

    // constructor
    public Employee(string name, string salary)
    {
        _employeeName = name;
        Salary = salary;
    }

    // public method
    public string DisplayInfo()
    {
        return $"Hi, I'm {_employeeName} and I earn {Salary} per year.";
    }
}

class Program
{
    static void Main()
    {
        // create object of Employee class
        Employee employee = new Employee("Nino", "$50,000");

        // call DisplayInfo method
        string info = employee.DisplayInfo();
        Console.WriteLine(info);
    }
}
