# The Norm v2.0.2 ru-en
#### I - Предисловие / Foreword
- I.1 - Почему принят стандарт? / Why impose a standard?
- I.2 - Нормы для подачи / The norm for submissions 
- I.3 - Советы / Suggestions
- I.4 - Отказ от ответственности / Disclaimers

#### II -	Нормы / The Norm
- II.1 - Название (Название переменных) / Denomination
- II.2 - Оформление / Formatting
- II.3 - Параметры передаваемые в функцию / Functions parameters
- II.4 - Функции / Functions
- II.5 - Определение имени, структура, перечисление, объединение / Typedef, struct, enum and union
- II.6 - Заголовки / Headers
- II.7 - Макрос и пре-процессоры / Macros and Pre-processors
- II.8 - Запрещенные штуки ! Forbidden stuff !
- II.9 - Комментарии / Comments
- II.10 - Файлы / Files
- II.11 - Makefile

#### III - Дополнения
- III.00 - Пример правильного оформления кода с комментариями
- III.01 - Norminette errors
------------
## I - Предисловие / Foreword
В этом документе описаны стандарты (Нормы) школы 42. Стандарт программирования определяет свод правил, которым нужно следовать во время написания кода. Вы должны всегда следовать правилам Норм во всех C-проектах в школе, если конкретно не указан иной вариант.

> This document describes the applicable standard (Norm) at 42. A programming standard deﬁnes a set of rules to follow when writing code. You must always respect the Norm for all C projects at the school, unless otherwise speciﬁed.

#### I.1 - Почему принят стандарт? / Why impose a standard? 
Две главные цели, которые преследуют Нормы: / The Norms two main objective:
1.	Стандартизировать и правильно оформить ваш код, чтобы все (ученики, администрация и даже вы сами) могли легко читать и понимать его.

> To format and standardize your code so that anyone (students, staﬀ and even yourself) can read and understand them easily.

2.	Помочь вам в написании короткого и простого кода.

> To guide you in writing short and simple code.

#### I.2 - Нормы для подачи / The Norm for submissions
Все ваши C-файлы должны следовать Нормам школы. За этим будут следить те, кто вас проверяет. Если вы совершите любую ошибку по Нормам, то получите 0 за все задание или даже весь проект. Во время проверки ваш проверяющий должен будет запустить проверку “Norminette” с вашими файлами. Только оценка “Norminette” должна быть взята во внимание. Только Обязательная часть Норм будет проверена “Norminette”.

>All of your C ﬁles must respect the school’s Norm. It will be checked by your grader. If you made any Norm error you’ll get a 0 for the exercise or even for the whole project.
During peer-evaluations, your grader will have to launch the “Norminette” present in your submission’s dumps. Only the mandatory part of the Norm will be checked by the “Norminette”.

#### I.3 - Советы / Suggestions 
Достаточно быстро вы поймете, что Нормы не такие страшные, как кажутся. Наоборот, они помогают вам больше чем вы думаете. Они позволяют вам гораздо проще читать код ваших одноклассников и ваш код сам будет читабельным. Наказание за исходный файл с одной ошибкой по Нормам такое же, как и за файл с десятью ошибками. Мы настойчиво рекомендуем вам держать Нормы в голове во время написания кода - даже если вам сначала покажется, что они вас замедляют. Со временем, это превратится в рефлекс.

>You’ll realise soon enough that the Norm isn’t as intimidating as it seems. On the contrary, it’ll help you more than you know. It’ll allow you to read your classmates’ code more easily and vice versa. A source ﬁle containing one Norm error will be treated the same way as a source ﬁle containing 10 Norm errors. We strongly advise you to keep the Norm in mind while coding - even though you may feel it’s slowing you down at ﬁrst. In time, it’ll become a reﬂex.

#### I.4 - Отказ от отвественности / Disclaimers
“Norminette” – это программа. Как и все программы, в ней могут быть баги (ошибки). Если заметили один, то сообщите в соответствующей секции на форме. Однако, так как “Norminette” всегда превалирует, ваш код должен адаптироваться к ее багам.

>“Norminette” is a program, and all programs are subject to bugs. Should you spot one, please report it in the forum’s appropriate section.
However, as the“Norminette” always prevails, all your submissions must adapt to its bugs.

## II - The Norm / Нормы
