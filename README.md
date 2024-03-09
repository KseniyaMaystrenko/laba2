# laba2

## задание 1

условие

Андрей составляет 6-буквенные коды из букв А, Н, Д, Р, Е, Й. Буква Й может использоваться в коде не более одного раза, при этом она не может стоять на первом месте, на последнем месте и рядом с буквой Е. Все остальные буквы могут встречаться произвольное количество раз или не встречаться совсем. Сколько различных кодов может составить Андрей?

объяснение решения

В коде определена функция Andrey(), принимающая в качестве аргумента строку s. Далее идет инициализация переменных n и k значениями 0. Затем идут вложенные циклы с именами (x1, x2, x3, x4, x5, x6), которые пробегают все возможные комбинации из символов 'АНДРЕЙ'. Для каждой комбинации формируется строка x, в которую эти символы объединяются. Далее проверяется, содержит ли строка x подстроки 'ЙЕ', 'ЕЙ' и Й в нужном количестве. Если это so, к счетчику k добавляется 1.

На выходе функция возвращает значение счетчика k, которое и является количеством правильных комбинаций. После определения функции вызывается print функция, которая выводит сообщение о количестве возможных комбинаций с поиском слова 'АНДРЕЙ' в них.


## задание 2

условие

Сколько единиц содержится в двоичной записи значения выражения 8**2020+4**2017+26-1

объяснение решения

В этом коде определяется функция `dva()`, которая выполняет следующие операции:

1. Создается переменная `bun`, которой присваивается значение выражения `8**2020 + 4*2017 + 26 - 1`.
2. Создается переменная `ces`, которой присваивается значение строки, полученной путем преобразования числа `bun` в двоичную систему счисления с помощью функции `bin()`. Так как `bin()` возвращает строку с приставкой '0b', используется срез `[2:]`, чтобы получить только двоичное представление числа без приставки.
3. Функция `dva()` возвращает количество единиц в двоичном представлении числа `bun`, с помощью метода `count('1')`.
4. Выводится результат вызова функции `dva()`.

ответ:

11

## задание 3

условие

Найдите среди целых чисел, принадлежащих числовому отрезку [245 690; 245 756]  простые числа. Выведите на экран все найденные простые числа в порядке возрастания, слева от каждого числа выведите его порядковый номер в последовательности. Каждая пара чисел должна быть выведена в отдельной строке. Например, в диапазоне [5; 9]  ровно два различных натуральных простых числа  — это числа 5 и 7, поэтому для этого диапазона вывод на экран должен содержать следующие значения:   

  1   5
  3   7

объяснение решения

  Данный код на языке Python представляет собой функцию f(x), которая принимает на вход число x и находит все его делители (кроме 1 и самого числа). Затем задаются начальное (start) и конечное (end) значения для диапазона чисел. Далее в цикле перебираются все числа от начального до конечного (включительно) и проверяется, имеются ли делители у этих чисел (используется функция f). Если у числа нет делителей, то выводится его номер в последовательности (n) и само число.

ответ:

22 245711
30 245719
34 245723
52 245741
58 245747
64 245753
