1_8

Цель
Напишите программу, которая считывает два целых числа из одной строки и выводит их сумму в стандартный вывод. Числа могут быть положительными, отрицательными или нулевыми.

Пример
В примере ниже показаны входные данные и соответствующие выходные данные. Ваша программа должна работать таким же образом. Не добавляйте лишние символы после вывода!

Символ «больше», за которым следует пробел ( > ), представляет ввод пользователя. Обратите внимание, что это не часть ввода.

> 5 8
13

2_8

Описание
Настало время улучшить предыдущую версию калькулятора. Что делать, если у нас есть много пар чисел, сумму которых нам нужно найти? Каждый раз запускать программу будет очень неудобно. Итак, давайте добавим цикл для непрерывного вычисления суммы двух чисел. Обязательно укажите безопасное слово, чтобы разорвать цикл. Также было бы неплохо продумать ситуации, когда пользователи вводят только одну цифру или вообще не вводят цифры.

Цели
Напишите программу, которая считывает два числа в цикле и выводит сумму в стандартный вывод.
Если пользователь вводит только одно число, программа должна напечатать тот же номер. Если пользователь вводит пустую строку, программа должна ее игнорировать.
/exitПри вводе команды программа должна напечатать "Bye!"(без кавычек), а затем остановиться.
Примеры
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> 17 9
26
> -2 5
3
>
> 7
7
> /exit
Bye!

3_8

Описание
В редких случаях нам нужно вычислить сумму всего двух чисел. Теперь пришло время научить калькулятор читать неограниченную последовательность чисел. Также давайте позаботимся о себе, если через некоторое время мы захотим вспомнить, что делает наша программа. Для этого введем /helpв наш калькулятор новую команду. Пользователи, которые впервые познакомились с этой программой, могут /helpтакже узнать о ней больше!

Цели
Добавьте в калькулятор возможность читать неограниченную последовательность чисел.
Добавьте /helpкоманду для вывода некоторой информации о программе.
Если вы встретите пустую строку, ничего не выводите.
Примеры
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> 4 5 -2 3
10
> 4 7
11
> 6
6
> /help
The program calculates the sum of numbers
> /exit
Bye!

4_8

Описание
Наконец мы добрались до следующей операции: вычитания. Это значит, что отныне программа должна получать на вход операторы сложения +и вычитания -, чтобы отличать операции друг от друга. Он должен поддерживать как унарные, так и бинарные операторы минус. Более того, если пользователь ввел несколько одинаковых операторов, следующих друг за другом, программа все равно должна работать (например, Java или Python REPL). А еще, как вы помните из школьной математики, два соседних знака минус превращаются в плюс. Следовательно, если пользователь вводит --, это следует читать как +; если они вводят ----, это следует читать как ++и так далее. У умного калькулятора должна быть такая функция.

Обратите внимание на /helpкоманду, важно сохранять ее актуальность в зависимости от изменений (в том числе и на следующих этапах). Вы можете написать информацию о своей программе в свободной форме, но главное, чтобы она была понятна вам и другим пользователям.

Цели
Программа должна вычислять такие выражения: 4 + 6 - 8, 2 - 3 - 4и т. д.
Измените результат команды /help, чтобы объяснить эти операции.
Декомпозируйте свою программу с помощью функций, чтобы облегчить ее понимание и редактирование в дальнейшем.
Программа не должна останавливаться, пока пользователь не введет /exitкоманду.
Если вы встретите пустую строку, ничего не выводите.
Примеры
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> 8
8
> -2 + 4 - 5 + 6
3
> 9 +++ 10 -- 8
27
> 3 --- 5
-2
> 14       -   12
2
> /exit
Bye!

5_8

Описание
Теперь нужно учесть реакцию калькулятора, когда пользователи вводят выражения в неправильном формате. Программа знает только числа, знак плюс, знак минус и две команды. Все остальные символы он принять не может и об этом необходимо предупредить пользователя.

Цели
Программа должна печатать Invalid expressionв тех случаях, когда данное выражение имеет недопустимый формат. Если пользователь вводит неверную команду, программа должна вывести Unknown command. Все сообщения должны быть напечатаны без кавычек. Программа никогда не должна генерировать исключение.
Чтобы справиться с неверным вводом, вы должны помнить, что пользовательский ввод, начинающийся с, /— это команда , в других ситуациях — выражение .

Как и раньше, /helpкоманда должна вывести информацию о вашей программе. При /exitвводе команды программа должна напечатать Bye!, а затем остановиться.
Примеры
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> 8 + 7 - 4
11
> abc
Invalid expression
> 123+
Invalid expression
> +15
15
> 18 22
Invalid expression
>
> -22
-22
> 22-
Invalid expression
> /go
Unknown command
> /exit
Bye!

6_8

Описание
Теперь калькулятор сможет сохранять результаты предыдущих расчетов. У вас есть идеи, как это сделать? Конечно! Этого можно добиться введением переменных. Сохранение результатов в переменных и последующая работа с ними в любой момент — очень удобная функция.

Цели
Итак, ваша программа должна поддерживать переменные.

Следуйте следующим правилам для переменных:

Мы предполагаем, что имя переменной (идентификатор) может содержать только латинские буквы.
Переменная может иметь имя, состоящее более чем из одной буквы.
Случай также важен; например, n — это не то же самое, что N.
Значение может быть целым числом или значением другой переменной.
Должна быть возможность установить новое значение для существующей переменной.
Чтобы напечатать значение переменной, вам нужно просто ввести ее имя.
В приведенном ниже примере показано, как можно объявлять и отображать переменные.

> n = 3
> m=4
> a  =   5
> b = a
> v=   7
> n =9
> count = 10
> a = 1
> a = 2
> a = 3
> a
3

Неправильное написание или объявление переменных также должно вызывать исключение с соответствующим сообщением пользователю:

Сначала переменная проверяется на корректность. Если пользователь вводит неверное имя переменной, то на выходе должно быть "Invalid identifier".
> a2a
Invalid identifier
> n22
Invalid identifier

Если переменная действительна, но еще не объявлена, программа должна вывести "Unknown variable".
> a = 8
> b = c
Unknown variable
> e
Unknown variable

Если идентификатор или значение переменной недопустимы во время объявления переменной, программа должна вывести сообщение, подобное показанному ниже.
> a1 = 8
Invalid identifier
> n1 = a2a
Invalid identifier
> n = a2a
Invalid assignment
> a = 7 = 8
Invalid assignment

Обратите внимание, что программа должна распечатать, "Invalid identifier"если левая часть задания неверна. Если часть после "="неверно, используйте "Invalid assignment". Сначала нам следует проверить левую сторону.

Обрабатывайте как можно больше неправильных входных данных. Программа никогда не должна генерировать какие-либо исключения.

Важно отметить, что все переменные должны сохранять свои значения между вычислениями разных выражений.

Не забываем о реализованных ранее командах: /helpи /exit.

Примеры
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> a  =  3
> b= 4
> c =5
> a + b - c
2
> b - c + 4 - a
0
> a = 800
> a + b + c
809
> BIG = 9000
> BIG
9000
> big
Unknown variable
> /exit
Bye!

7_8

Описание
На заключительном этапе осталось добавить операции: умножение *, целочисленное деление /и круглые скобки (...). Они имеют более высокий приоритет, чем сложение +и вычитание -.

Вот пример выражения, которое содержит все возможные операции:

3 + 8 * ((4 + 3) * 2 + 1) - 6 / (2 + 1)

Результат: 121.

Общее выражение может содержать множество круглых скобок и операций с разными приоритетами. Такие выражения сложно вычислить, если не использовать специальные методы. К счастью, существует достаточно эффективное и универсальное решение с использованием стека для вычисления самых общих выражений.

От инфикса к постфиксу

Ранее мы обрабатывали выражения, записанные в инфиксной записи. Такое обозначение не очень удобно, если в выражении есть операции с разными приоритетами, особенно при использовании скобок. Но мы можем использовать постфиксную нотацию , также известную как обратная польская нотация (RPN) . В этой записи операторы следуют за своими операндами. См. несколько примеров ниже.

Инфиксная запись 1:

3 + 2 * 4

Постфиксная запись 1:

3 2 4 * +

Инфиксная запись 2:

2 * (3 + 4) + 1

Постфиксная запись 2:

2 3 4 + * 1 +

Чтобы лучше понять постфиксную нотацию, можно поиграться с конвертером .

Как видите, в постфиксной записи операции располагаются по приоритету и круглые скобки вообще не используются. Таким образом, проще вычислять выражения, записанные в постфиксной записи.

Вы можете использовать стек ( LIFO ) для преобразования выражения из инфиксной записи в постфиксную. Стек используется для хранения операторов для изменения порядка. Вот несколько правил, описывающих, как создать алгоритм, преобразующий выражение из инфиксной записи в постфиксную.

Добавляйте операнды (числа и переменные) к результату (постфиксная запись) по мере их поступления.
Если стек пуст или содержит левую скобку сверху, поместите входящий оператор в стек.
Если входящий оператор имеет более высокий приоритет, чем верхняя часть стека, поместите его в стек.
Если приоритет входящего оператора ниже или равен приоритету вершины стека, извлеките стек и добавляйте операторы к результату, пока не увидите оператор с меньшим приоритетом или левую скобку на вершине стека; затем добавьте входящий оператор в стек.
Если входящий элемент представляет собой левую скобку, поместите его в стек.
Если входящий элемент представляет собой правую скобку, извлеките стек и добавляйте операторы к результату, пока не увидите левую скобку. Отбросьте пару скобок.
В конце выражения извлеките стек и добавьте к результату все операторы.
В стеке не должно оставаться скобок. В противном случае выражение содержит несбалансированные скобки. Это синтаксическая ошибка.

Расчет результата

Когда у нас есть выражение в постфиксной нотации, мы можем вычислить его, используя другой стек. Для этого просканируйте постфиксное выражение слева направо:

Если входящий элемент является числом, поместите его в стек (целое число, а не одну цифру!).
Если входящий элемент является именем переменной, поместите ее значение в стек.
Если входящий элемент является оператором, нажмите дважды, чтобы получить два числа и выполнить операцию; поместите результат в стек.
Когда выражение заканчивается, число на вершине стека является окончательным результатом.
Здесь вы можете найти пример и дополнительные пояснения к постфиксным выражениям .

Цели
Ваша программа должна поддерживать умножение *, целочисленное деление /и скобки (...). Для этого используйте описанный выше алгоритм преобразования инфикса в постфикс, а затем вычислите результат с помощью стека.
Не забывайте о переменных; они и унарный оператор минус все равно должны работать.
Измените результат команды /help, чтобы объяснить все возможные операторы. Вывод команды можно записать в свободной форме.
Программа не должна останавливаться, пока пользователь не введет /exitкоманду.
Обратите внимание, что последовательность +(like +++или +++++) является допустимым оператором, который следует интерпретировать как одиночный плюс. Последовательность -(like --или ---) также является допустимым оператором, и ее значение зависит от длины. Если пользователь вводит последовательность *или /, программа должна вывести сообщение о том, что выражение неверно.
В качестве бонуса вы можете добавить оператор мощности ^, имеющий более высокий приоритет, чем *и /.
> 2^2
4
> 2*2^3
16

Примеры
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> 8 * 3 + 12 * (4 - 2)
48
> 2 - 2 + 3
3
> 4 * (2 + 3
Invalid expression
> -10
-10
> a=4
> b=5
> c=6
> a*2+b*3+c*(2+3)
53
> 1 +++ 2 * 3 -- 4
11
> 3 *** 5
Invalid expression
> 4+3)
Invalid expression
> /command
Unknown command
> /exit
Bye!

8_8

Описание
На этом этапе ваша программа должна поддерживать арифметические операции ( +, -, *, /) с очень большими числами, а также круглые скобки для изменения приоритета внутри выражения.

Есть два способа решить эту проблему. В качестве простого способа вы можете использовать стандартный класс для работы с большими числами, просто правильно примените его к своему решению. Если вы хотите попрактиковаться в алгоритмах, вы можете разработать собственный класс для больших чисел и реализовать алгоритмы для перечисленных арифметических операций.

Пример
Символ «больше», за которым следует пробел ( >), представляет ввод пользователя.

> 112234567890 + 112234567890 * (10000000999 - 999)
1122345679012234567890
> a = 800000000000000000000000
> b = 100000000000000000000000
> a + b
900000000000000000000000
> /exit
Bye!

Программа не должна останавливаться, пока пользователь не введет /exitкоманду.