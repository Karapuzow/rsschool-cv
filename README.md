# rsschool-cv
# Yauheni Karapuzow
## Junior Backend Developer
## Contact information:

### **Phone**: +375336453090
### **E-mail**: karapuz01k@gmail.com
### **Telegram**: @Men_0f_mayhem
### **linkedln**: Евгений Карапузов

## Information about me:
### My name is Evgeny, I live in Belarus, I work in the energy sector. A few months ago, I decided to try my hand at IT, chose the direction of game and application development for myself. I successfully completed courses in C#, but it was not enough and in order to turn my ideas into reality, I decided to learn JavaScript, CSS & HTML.

# **Skills and Proficiency**:
### C#, .Net
### Git,GitHub

## **
Example of a task and code**:
### В этом задании я находил минимальное количество купюр, которыми можно разменять заданную сумму. В процессе решения я использовал циклы, работал с массивом и выводом информации на экран.
### using System;

namespace Task
{
    internal class Program
    {
        public static void Main(string[] args)
        {
            // Считываем сумму, которую мы должны разменять
            int amount = Convert.ToInt32(Console.ReadLine());

            // Создаем массив, в котором будем считать промежуточные значения.
            // В этом массиве amounts[СУММА_ДЕНЕГ] лежит минимальное количество купюр для размена этой суммы денег
            int[] amounts = new int[amount + 1];
            // Чтобы поменять ноль денег, надо ноль купюр
            amounts[0] = 0;

            // Считываем количество банкнот 
            int banknotesCount = Convert.ToInt32(Console.ReadLine());
            // Создаем массив, который будет хранить номиналы купюр
            int[] banknotes = new int[banknotesCount];

            // Считываем с консоли номиналы купюр
            for (int i = 0; i < banknotesCount; i++)
            {
                banknotes[i] = Convert.ToInt32(Console.ReadLine());
            }

            // Создаем цикл для всех сумм денег от 1 до amount
            for (int j = 1; j <= amount; j++)
            {
                // Задаем, максимально возможное значение для типа int в ячейки (это будет означать, что данную сумму денег нельзя разменять заданными купюрами)
                // Отнимаем 1, т.к. в коде ниже мы прибавляем единицу и тогда мы будем переполнять это число
                amounts[j] = Int32.MaxValue - 1;
                // Создаем цикл для всех номиналов купюр
                for (int i = 0; i < banknotesCount; i++)
                {
                    // Проверяем, чтобы купюра была меньше, чем сумма денег, которую мы хотим разменять
                    if (j >= banknotes[i])
                    {
                        // Если количество разменов получилось меньше, чем было, то изменяем это значение на новое
                        amounts[j] = Math.Min(amounts[j - banknotes[i]] + 1, amounts[j]);
                    }
                }
            }

            // Выводим ответ на консоль
            Console.WriteLine(amounts[amount]);
        }
    }
}
## Courses:
### 
basics of c# programming from Game Dev Academy
## Languages:
### English - A2(A1 in processing)
### Russian - Native
### Deutch - Basic
