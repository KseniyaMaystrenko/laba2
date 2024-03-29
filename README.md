# laba2

## задание 1

     условие

Андрей составляет 6-буквенные коды из букв А, Н, Д, Р, Е, Й. Буква Й может использоваться в коде не более одного раза, при этом она не может стоять на первом месте, на последнем месте и рядом с буквой Е. Все остальные буквы могут встречаться произвольное количество раз или не встречаться совсем. Сколько различных кодов может составить Андрей?

     объяснение решения

1. Импортируется функция product из модуля itertools, которая используется для создания всех возможных комбинаций элементов из заданного списка.
2. Определяется функция count_codes(), которая подсчитывает количество различных кодов, которые может составить имя "Андрей".
3. Задается список letters с буквами имени "Андрей" - ['А', 'Н', 'Д', 'Р', 'Е', 'Й'].
4. Инициализируется переменная count равная 0, которая будет использоваться для подсчета количества кодов.
5. В цикле for создаются все возможные комбинации из букв имени "Андрей" длиной 6 символов с помощью функции product(letters, repeat=6).
6. Для каждого полученного кода проверяются условия:
   - Количество буквы 'Й' в коде не превышает 1 (code.count('Й') <= 1).
   - Первая и последняя буквы не равны 'Й' (code[0] != 'Й' и code[-1] != 'Й').
   - Подстроки 'ЕЙ' и 'ЙЕ' отсутствуют в коде ('ЕЙ' not in ''.join(code) и 'ЙЕ' not in ''.join(code)).

7. Если код удовлетворяет всем условиям, увеличивается значение переменной count.
8. Функция возвращает общее количество удовлетворяющих условиям кодов.
9. Вызывается функция count_codes() и результат сохраняется в переменной total_codes.
10. Выводится сообщение о количестве различных кодов, которые может составить имя "Андрей", используя f-строку для форматирования строки вывода.
На выходе функция возвращает значение счетчика k, которое и является количеством правильных комбинаций. После определения функции вызывается print функция, которая выводит сообщение о количестве возможных комбинаций с поиском слова 'АНДРЕЙ' в них.

     ответ:

!![image](https://github.com/KseniyaMaystrenko/laba2/assets/152999073/6cc8b728-93c5-4fe1-91b0-6abdade2838d)


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

![image](https://github.com/KseniyaMaystrenko/laba2/assets/152999073/cf6616ef-4abc-4a72-8b19-b065e5acba0d)


## задание 3

      условие

Найдите среди целых чисел, принадлежащих числовому отрезку [245 690; 245 756]  простые числа. Выведите на экран все найденные простые числа в порядке возрастания, слева от каждого числа выведите его порядковый номер в последовательности. Каждая пара чисел должна быть выведена в отдельной строке. Например, в диапазоне [5; 9]  ровно два различных натуральных простых числа  — это числа 5 и 7, поэтому для этого диапазона вывод на экран должен содержать следующие значения:   

  1   5
  3   7

     объяснение решения

Код, который вы предоставили, выполняет следующие действия:

1. def f(x):: Определение функции f, которая принимает один аргумент x.
2. k=2: Инициализация переменной k равной 2.
3. deliteli=set(): Создание пустого множества deliteli, которое будет содержать делители числа x.
4. while k*k<=x:: Начало цикла while, который будет выполняться до тех пор, пока квадрат k меньше или равен x.
5. if x%k==0:: Проверка, делится ли число x нацело на k.
6. deliteli.add(k): Добавление делителя k в множество deliteli.
7. if x//k<x:: Проверка, является ли результат целочисленного деления x на k меньше самого x.
8. deliteli.add(x//k): Добавление делителя x//k в множество deliteli.
9. k=k+1: Увеличение значения переменной k для проверки следующего делителя.
10. return sorted(deliteli): Возврат отсортированного списка делителей числа x.
11. start=245690: Инициализация переменной start равной 245690.
12. end=245757: Инициализация переменной end равной 245757.
13. n=0: Инициализация переменной n равной 0.
14. for i in range(start,end+1):: Начало цикла for для перебора чисел от start до end.
15. n=n+1: Увеличение значения переменной n.
16. if len(f(i))==0:: Проверка, имеет ли число i нулевое количество делителей (то есть является ли оно простым).
17. print(n,i): Вывод номера числа и самого числа, если оно простое (имеет нулевое количество делителей).

1. Определяется функция f(x), которая находит все делители числа x и возвращает их в виде отсортированного списка.
2. Задаются начальное значение start и конечное значение end для интервала чисел, в котором будет производиться поиск простых чисел.
3. Инициализируется переменная n равная 0, которая будет использоваться для нумерации чисел.
4. В цикле for перебираются все числа от start до end.
5. Для каждого числа i увеличивается значение переменной n.
6. Проверяется количество делителей числа i, используя функцию f(i). Если число i является простым (имеет 0 делителей), то выводится его номер и значение.

Таким образом, программа находит и выводит все простые числа в заданном интервале от 245690 до 245757.

      ответ:

![image](https://github.com/KseniyaMaystrenko/laba2/assets/152999073/b0e6868a-c2cc-4fe8-9bf9-dfe293248879)


используемые источники: 

[Использование itertools](https://youtu.be/xIEVAm7BakE?feature=shared)

[Про простые чилса](https://youtu.be/R8oCK4W8px4?feature=shared)
