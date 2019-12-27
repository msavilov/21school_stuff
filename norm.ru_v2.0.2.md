# The Norm v2.0.2 en-ru
#### I -	Foreword / Предисловие
- I.1 - Why impose a standard? / Почему принят стандарт?
- I.2 - The norm for submissions / Нормы для подачи
- I.3 - Suggestions / Предложения
-  I.4 - Disclaimers / Отказ от ответственности

#### II -	The Norm / Нормы
- II.1 - Denomination / Название (Название переменных)
- II.2 - Formatting / Оформление
- II.3 - Functions parameters / Параметры передаваемые в функцию
- II.4 - Functions / Функции
- II.5 - Typedef, struct, enum and union / Определение имени, структура, перечисление, объединение
- II.6 - Headers /  Заголовки
- II.7 - Macros and Pre-processors / Макрос и пре-процессоры
- II.8 - Forbidden stuff ! / Запрещенные штуки !
- II.9 - Comments / Комментарии
- II.10 - Files / Файлы
- II.11 - Makefile

#### III -	Дополнения
- III.00 - Пример правильного оформления кода с комментариями
- III.01 - Norminette errors
------------
## I - Foreword / Предисловие
> This document describes the applicable standard (Norm) at 42. A programming standard deﬁnes a set of rules to follow when writing code. You must always respect the Norm for all C projects at the school, unless otherwise speciﬁed.

В этом документе описаны стандарты (Нормы) школы 42. Стандарт программирования определяет свод правил, которым нужно следовать во время написания кода. Вы должны всегда следовать правилам Норм во всех C-проектах в школе, если конкретно не указан иной вариант.

#### I.1 - Why impose a standard? / Почему принят стандарт
The Norms two main objective / Две главные цели, которые преследуют Нормы:
1.	> To format and standardize your code so that anyone (students, staﬀ and even yourself) can read and understand them easily.

Стандартизировать и правильно оформить ваш код, чтобы все (ученики, администрация и даже вы сами) могли легко читать и понимать его.

2.	> To guide you in writing short and simple code.

Помочь вам в написании короткого и простого кода.

#### I.2 - The Norm for submissions / Нормы для подачи
>All of your C ﬁles must respect the school’s Norm. It will be checked by your grader. If you made any Norm error you’ll get a 0 for the exercise or even for the whole project.
During peer-evaluations, your grader will have to launch the “Norminette” present in your submission’s dumps. Only the mandatory part of the Norm will be checked by the “Norminette”.

Все ваши C-файлы должны следовать Нормам школы. За этим будут следить те, кто вас проверяет. Если вы совершите любую ошибку по Нормам, то получите 0 за все задание или даже весь проект. Во время проверки ваш проверяющий должен будет запустить проверку “Norminette” с вашими файлами. Только оценка “Norminette” должна быть взята во внимание. Только Обязательная часть Норм будет проверена “Norminette”.

#### I.3 - Suggestions / Предложения / Советы
>You’ll realise soon enough that the Norm isn’t as intimidating as it seems. On the contrary, it’ll help you more than you know. It’ll allow you to read your classmates’ code more easily and vice versa. A source ﬁle containing one Norm error will be treated the same way as a source ﬁle containing 10 Norm errors. We strongly advise you to keep the Norm in mind while coding - even though you may feel it’s slowing you down at ﬁrst. In time, it’ll become a reﬂex.

Достаточно быстро вы поймете, что Нормы не такие страшные, как кажутся. Наоборот, они помогают вам больше чем вы думаете. Они позволяют вам гораздо проще читать код ваших одноклассников и ваш код сам будет читабельным. Наказание за исходный файл с одной ошибкой по Нормам такое же, как и за файл с десятью ошибками. Мы настойчиво рекомендуем вам держать Нормы в голове во время написания кода - даже если вам сначала покажется, что они вас замедляют. Со временем, это превратится в рефлекс.

#### I.4 - Disclaimers / Отказ от отвественности
>“Norminette” is a program, and all programs are subject to bugs. Should you spot one, please report it in the forum’s appropriate section.
However, as the“Norminette” always prevails, all your submissions must adapt to its bugs.

“Norminette” – это программа. Как и все программы, в ней могут быть баги (ошибки). Если заметили один, то сообщите в соответствующей секции на форме. Однако, так как “Norminette” всегда превалирует, ваш код должен адаптироваться к ее багам.

## II - The Norm / Нормы
