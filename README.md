# Контрольная работа по первому блоку (final test)
______

:white_check_mark::one: Создать репозиторий на GitHub
![подтверждение созданного репа](https://github.com/GrafClassiC/final_test/blob/main/1.png)

:white_check_mark::two: Нарисовать блок-схему алгоритма (можно обойтись блок-схемой основной содержательной части, если вы выделяете её в отдельный метод)

:white_check_mark::three: Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)

:white_check_mark::four: Написать программу, решающую поставленную задачу:
 >Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.
>>Примеры:
[“Hello”, “2”, “world”, “:-)”] → [“2”, “:-)”]
[“1234”, “1567”, “-2”, “computer science”] → [“-2”]
[“Russia”, “Denmark”, “Kazan”] → []
```C#
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Введите элементы массива через запятую:");
        string input = Console.ReadLine();
        string[] inputArray = input.Split(',');

        string[] resultArray = FilterArray(inputArray);

        Console.WriteLine("Результат:");
        foreach (string item in resultArray)
        {
            Console.Write(item + " ");
        }
    }

    static string[] FilterArray(string[] inputArray)
    {
        int count = 0;

        foreach (string item in inputArray)
        {
            if (item.Length <= 3)
            {
                count++;
            }
        }

        string[] resultArray = new string[count];
        int index = 0;

        foreach (string item in inputArray)
        {
            if (.Length <= 3)
            {
                resultArray[index] = item;
                index++;
            }
        }

        return resultArray;
    }
}
```