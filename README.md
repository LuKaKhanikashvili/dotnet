using System;
using System.Collections.Generic;

public class MyCollection<T>
{
    private List<T> items = new List<T>();

    // ელემენტის დამატება
    public void AddItem(T item)
    {
        items.Add(item);
    }

    // ელემენტის ამოღება ინდექსით
    public T GetItem(int index)
    {
        if (index >= 0 && index < items.Count)
        {
            return items[index];
        }
        else
        {
            throw new IndexOutOfRangeException("მოცემული ინდექსი არასწორია.");
        }
    }
}

class Program
{
    static void Main()
    {
        // MyCollection<string> ობიექტის შექმნა
        MyCollection<string> names = new MyCollection<string>();

        // ელემენტების დამატება
        names.AddItem("Ana");
        names.AddItem("Giorgi");
        names.AddItem("Luka");

        // ელემენტის ამოღება ინდექსით და დაბეჭ
