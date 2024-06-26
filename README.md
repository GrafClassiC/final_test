# Контрольная работа по первому блоку (final test)
______

:white_check_mark::one: 
## Создать репозиторий на GitHub 

![подтверждение созданного репа](https://github.com/GrafClassiC/final_test/blob/main/PNG/1.png)

:white_check_mark::two: 
### Нарисовать блок-схему алгоритма (можно обойтись блок-схемой основной содержательной части, если вы выделяете её в отдельный метод)

![Скринн блок-схемы](https://github.com/GrafClassiC/final_test/blob/main/PNG/scheme.png)

[Ссылка на блок-схему формата .draiwio](https://github.com/GrafClassiC/final_test/blob/main/PNG/diagramm.drawio)

:white_check_mark::three: 

#### Снабдить репозиторий оформленным текстовым описанием решения (файл README.md)
```C#
using System;
class Programm

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
            if (item.Length <= 3)
            {
                resultArray[index] = item;
                index++;
            }
        }

        return resultArray;
    }
```
 __Подробное описание работы программы__:
1. Начинаем с метода `Main()`, который выводит - "Введите элементы массива через запятую:" и ждет ввода.
2. Вводим данные в строку, содержащую элементы массива, разделенные запятой. Эта строка разбивается на подстроки, используя метод `Split(',')`, и сохраняется в массиве `inputArray`.
3. Далее программа вызывает метод `FilterArray(inputArray)`, передавая ему в качестве аргумента массив `inputArray`.
4. Метод `FilterArray` проходит по каждому элементу в массиве `inputArray` и проверяет длину каждой строки. Если длина строки меньше или равна 3 символам, увеличивается счетчик `count`.
5. Затем создается новый массив `resultArray` длиной `count`, в который будут сохранены только строки из `inputArray` с длиной меньше или равной 3 символам.
6. Далее программа проходит снова по каждому элементу в массиве `inputArray` и, если длина строки меньше или равна 3 символам, копирует эту строку в `resultArray`.
7. Наконец, метод `FilterArray` возвращает новый массив `resultArray`.
8. В методе `Main()` результат, содержащий только отфильтрованные строки, выводится на экран с помощью цикла `foreach`.

___Следовательно программа фильтрует введенные элементы массива по длине и выводит только те, которые содержат не более 3 символов.___

:white_check_mark::four:

##### Написать программу, решающую поставленную задачу:
> Задача: Написать программу, которая из имеющегося массива строк формирует новый массив из строк, длина которых меньше, либо равна 3 символам. Первоначальный массив можно ввести с клавиатуры, либо задать на старте выполнения алгоритма. При решении не рекомендуется пользоваться коллекциями, лучше обойтись исключительно массивами.

>> Примеры:
[“Hello”, “2”, “world”] → [“2”]
[“1234”, “1567”, “-2”, “computer science”] → [“-2”]
[“Russia”, “Denmark”, “Kazan”] → []

__Первая часть кода в VSC__
![printscreen VSC1](https://github.com/GrafClassiC/final_test/blob/main/PNG/1project.png)

__Вторая часть кода в VSC__
![printscreen VSC2](https://github.com/GrafClassiC/final_test/blob/main/PNG/2project.png)

__Ввод данных/вывод решения в VSC__
![printscreen VSC3](https://github.com/GrafClassiC/final_test/blob/main/PNG/3project.png)