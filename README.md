class Program
{
    static void Main()
    {
        List<int> numbers = Console.ReadLine()
            .Split(' ')
            .Select(int.Parse)
            .ToList();

        int addNumber = int.Parse(Console.ReadLine());
        int removeNumber = int.Parse(Console.ReadLine());
        int index = int.Parse(Console.ReadLine());

        Console.WriteLine("Начален списък: " + string.Join(" ", numbers));

        numbers.Add(addNumber);
        Console.WriteLine("След Add: " + string.Join(" ", numbers));

        numbers.Insert(0, addNumber);
        Console.WriteLine("След Insert: " + string.Join(" ", numbers));

        if (numbers.Remove(removeNumber))
        {
            Console.WriteLine("След Remove: " + string.Join(" ", numbers));
        }
        else
        {
            Console.WriteLine("Числото не съществува в списъка.");
        }

        if (index >= 0 && index < numbers.Count)
        {
            numbers.RemoveAt(index);
            Console.WriteLine("След RemoveAt: " + string.Join(" ", numbers));
        }
        else
        {
            Console.WriteLine("Невалиден индекс.");
        }

        Console.WriteLine("Краен брой елементи: " + numbers.Count);

        for (int i = 0; i < numbers.Count; i++)
        {
            Console.WriteLine(i + ". " + numbers[i]);
        }
    }
}

# Homework2
