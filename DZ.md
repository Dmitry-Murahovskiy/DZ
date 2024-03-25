
bool IsSumEven(int number)
{
    int sum = 0;
    while (number != 0)
    {
        sum += number % 10;
        number /= 10;
    }
    return sum % 2 == 0;
}

while (true)
{
    Console.WriteLine("Введите целое число или 'q' для выхода:");
    string input = Console.ReadLine();

    if (input == "q")
    {
        break;
    }

    int number;
    if (int.TryParse(input, out number))
    {
        if (IsSumEven(number))
        {
            break;
        }
    }
    else
    {
        Console.WriteLine("Введено некорректное значение. Повторите попытку.");
    }
}


