# Синтаксис написания кода

Команды для программы, которые она должна выполнять:
+ Console.Write(); - вывод в одну строку
+ Console.WriteLine(); - в конце перейти на новую строку
+ Console.ReadLine(); - прочесть строку из терминала
+ new Random().Next(min, max); - случайное число
+ switch () case ; — это удобная замена длинной if-else конструкции, которая сравнивает переменную с несколькими константными
+ while (УСЛОВИЕ ПРОДОЛЖЕНИЯ); - цикл.
+ if (УСЛОВИЕ ПРОДОЛЖЕНИЯ); - условие
+ else - еще
+ username.Tolover - толерантность к шрифту
+ string - строка с данными от 0 до много
+ object - класс , базовый для всех типов (CTS)
+ switch - переключатель
+ int - целые числа
+ double - вещественные числа (с запятой)
+ bool - хранит в себе только 2 значения: правда (true) и ложь (false)

Математический синтаксис:
 +(плюс) - сложение
 -(минус) - вычетание
 / - деление
 *(звездочка) - умножение
 %(процент) - нахождение остатка
 () - скобки
 
## Оператор выбора (условный оператор IF)

Оператор выбора используется для последующего выполнения или не выполнения некоторого оператора или группы операторов, в зависимости от условия. Если предлагаемое условие истинно, то вложенный оператор или блок кода выполняется. Альтернативная ветвь, которая может присутствовать (а может и нет) выполнится, если условие ложно.

Пример:
    if (resault == 777){ 
    System.Console.WriteLine('Congratulations, you win!!!!');  
    } 
    else 
    { 
    System.Console.WriteLine('please, try again ');
    System.Console.WriteLine('we are confident - you will be lucky');    
    }
    else if(resault != 777){
    System.Console.WriteLine('game over');
    }

Также можно использовать упрощенный синтаксис, подобно используя условная операции: (resault == 777) ? true : false;

## Оператор ветвления

Оператор ветвления может иметь большое количество ветвей, выбор которых осуществляется с помощью значения управляющего выражения. Это очень удобный способ реализации кода, когда существует некий параметр, в зависимости от которого должны выполняться те или иные ветви кода. В C# он реализуется следующим образом:

switch(value) 
{ 
    default: 
    { 
        System.Console.WriteLine('для этого варианта действие не определено'); 
        break; 
    } 
        case 1 : 
    { 
        System.Console.WriteLine('Цифра 1'); 
        break; 
    }
    case 2 : 
    {
        System.Console.WriteLine('Цифра 2'); 
        break;
    }
    case 3 : 
    { 
        System.Console.WriteLine('Цифра 3'); 
        break; 
    } 
       }

## Оператор цикла while

Пример: значение переменной "a" инициируется равным 100, затем, пока "а" больше 5, выполняется тело цикла - вывод "а", затем уменьшение его значения на 1.

int a = 100; 
while(a > 5){ 
    System.Console.WriteLine(a); 
    a--; 
    }

## Оператор цикла do-while

Тело цикла выполняется до проверки условия:
    int a = 100; 
    do{ 
    System.Console.WriteLine(a); 
    a--; 
    } while(a > 5)

## Оператор цикла for

Цикл for используют, как правило, когда число повторений известно заранее, т.е. в задачах связанных с перебором. Мы устанавливаем начало отсчета, условие остановки и тип изменения параметра.

Пример: перебор значения для "a" = 100 изначально, до тех пор пока "a" больше 5. После каждого выполнения тела цикла, "a" уменьшается на 1.

    for (int a = 100; a > 5; a--){ 
    System.Console.WriteLine(a);
    }

## Оператор цикла foreach

Этот цикл полезен, когда необходимо перебрать все элементы массива, не вдаваясь в подробности. 
Пример: массив a состоит из 3 элементов. Цикл foreach переберет все значения, имеющиеся в массиве, приравнивая их к переменной **x**. В теле цикла мы производим вывод этих значений.

    int[] a = new int[]{1,2,3}; // наш массив 
    foreach (int x in a){ 
    System.Console.WriteLine(x); 
    }

## Методы и функции
Схема написания метода:
**ВозвращаемыйТипДанных ИмяМетода([ТипДанных1 ИмяАргумента1, ... ])
{
 Тело Метода
 return ЗначениеСоответствующееВозвращаемомуТипуДанных;
}

Пример:
double f(double x)
{
 double result = x * x + 1;
 return result
}


## Одномерные массивы

Данный тип массива включает в себя информацию о базовом типе элементов, которые может содержать массив, а также о количестве элементов в массиве (так называемая размерность массива). Нумерация элементов массивов начинается с нуля.

    uint[] arr_name = new uint[100];

Здесь arr_name - имя массива, 100 - количество элементов в массиве. Так как нумерация начинается с нуля, первый элемент доступен через следующее обращение: arr_name[0], последний: arr_name[99].

Способы заполнения массивов:

    1. int arr_name = new int[2]; 
    
    2. arr_name[0] = 1; 
       arr_name[1] = 2; 
       
    3. int[] arr_name = new int[] {1,2}; 
       int[] arr_name = {1,2};

## Прямоугольные массивы

Прямоугольный массив - это не что иное, как двумерный массив, например, размерностью 4x2:

    int[,] arr_name_1 = new int[4,2]; 
    int[,] arr_name_2 = {{0, 1, 2, 3}, {0, 1, 2}}; 
    for(i = 0; i < arr_name_1.GetLength(0); 
    i++){ 
        for (j = 0; j < arr_name_1.GetLength(1); j++){ 
            System.Console.WriteLine(arr_name_1[i,j]); 
            } 
        }

## Классы

Ключевое слово class, затем имя класса и перечисление его членов, заключенное в фигурные скобки, - на первый взгляд, мало что изменилось. 

Рассмотрим пример:

    public class MyTestClass 
    { 
        public string SomeStringInformation; 
    }

Модификатор доступа к классами:

+ public - член класса доступен вне определения класса и иерархии производных классов. + protected - член класса невидим за пределами класса, и обращаться к нему могут только производные классы. 
+ private - член класса недоступен за пределами области видимости определяющего его класса. Поэтому доступа к этим членам нет даже у производных классов. 
+ internal - член видим только в пределах текущей единицы компиляции. Модификатор доступа internals в плане ограничения доступа является гибридом public и protected, который зависит от местоположения кода.

