> Buna ziua tuturor, si bine ati venit la a doua zi de "shell".

Привет всем, и добро пожаловать в день посвященный "shell".

> leri ati vazut comportamentul de baza al "shell"-ului, ati putut vedea cum sa va deplasati untr-un director, cum sa creați un nou director, cum sa redenumiti un fișier, etc.

Вчера вы увидели базовое поведение «shell» оболочки. Вы могли видеть, как перемещать каталог, как создать новый каталог, как переименовать файл и т. д.

> Astăzi ne vom concentra pe tratarea conținutului unui fișier.

Сегодня мы сосредоточимся на работе с содержимым файла.

> De exemplu, sa-l afișam, sa-l filtram si chiar sa-l modificam.

Например: отобразите его, отфильтруйте и даже отредактируйте.

> i vom vedea o a doua noțiune care e foarte importanta, redirectarfl.

Мы увидим второе очень важное понятие - Перенаправления.

> Redirectarile sunt ceva ce veți folosi foarte mult pentru toata piscina si de-a lungul intregii voastre vieți de programator.

Перенаправления - это то, что вы будете часто использовать во время всего бассейна и на протяжении всей своей жизни как программиста.

> Deci vom incepe cu comenzile de afișare, care va vor permite sa afișați lucruri in ieșirea standard (vom vedea ce inseamna aceste "lucruri”).

Итак, начнем с команд отображения, которые позволят вам отображать вещи в стандартном выводе (посмотрим, что означают эти «вещи»).

> Deci pentru inceput, funcția de baza e "echo".

Итак, для начала, основная функция - «echo».

> Echo" va permite sa afișam ce ii dam in parametru, va reafisa asta pe ieșirea standard.

«Echo» позволит нам отобразить то, что мы даем им в параметре, он сделает это заново при стандартном выводе.

> Deci daca fac 'echo "bonjour’", va răspunde 'bonjour1. Nimic foarte interesant aici.

Так что, если я сделаю 'echo' "bonjour", он ответит  "bonjour". Здесь нет ничего интересного.

> Putem vedea ca poate lua mai multi parametri si ca ne afiseaza toti parametri pe care i-i dam.

Мы можем видеть, что он может принимать больше параметров, и он показывает нам все параметры, которые мы даем.

> Deci deocamdată va întrebați la ce folosește asta, dar vom vedea mai târziu in videouri care e utilitatea comenzii "echo".

Так что сейчас вам будет интересно, что это использует, но позже мы увидим в видеороликах, какова утилита команды 'echo'.

> O a doua comanda care va fi foarte utila pentru afișarea conținutului unui fișier e comanda "cat".

Вторая команда, которая будет очень полезна для отображения содержимого файла, - это команда «cat».

> "cat" ia intre altele un fișier ca parametru, si va va afișa conținutul acestui fișier.

"Cat", в частности, принимает файл в качестве параметра и отображает содержимое этого файла.

> După cum vedeți, "cat" ne-a afișat toate liniile fișierului, fara sa gandeasca.

Как видите, "cat" показала нам все строки файла, не задумываясь.

> "cat" are mai multe opțiuni, de exemplu daca ne uitam in manual vedem opțiunea "-e" care va fi foarte utila pentru voi in toata piscina care afiseaza caracterele "neafisabile".

У «cat» есть несколько опций, например, если мы посмотрим в руководстве, мы увидим опцию «-e», которая будет очень полезна для вас на бассейне, который отображает «не отображаемые» символы.

> Deci daca refac exemplul "cat -e" si fișierul meu, vom vedea ca la sfârșitul fiecărei linii apare un "$" care reprezintala returul la linia următoare.

Поэтому, если я переделал пример с практическими рекомендациями и мой файл, мы увидим, что в конце каждой строки есть «$», который представляет возврат к следующей строке.

> Va v-a fi foarte util pentru toate subiectele, când va vom ruga sa faceți o afișare fara retururi la linie vom face un "cat -e" sa va aratam ca nu exista la sfarsit, ceea ce inseamna ca nu sunt retururi la linie.

Это будет очень полезно для всех тем, когда мы просим вас сделать показ без возврата строки, мы сделаем "cat -e", чтобы показать вам, что нет конца, что означает, что нет никаких возвратов строки.

> Doua comenzi care sunt destul de asemanatoare sunt "less" si "more",care sunt de asemenea doua comenzi ce va vor permite si ele sa faceți afisari pe ieșirea standard dar intr-un mod mai interesant.

Две команды, которые очень похожи, «меньше» и «больше», которые позволят вам отображать стандартный вывод, но более интересным способом.

>De exemplu daca fac un "more" si numele meu de fisier, nu se afiseeaza toate liniile deodata,

Например, если я ddtle «more» и мое имя файла, не все строки отображаются одновременно,

> pot sa folosesc săgețile sa urc si sa cobor, pot sa caut in fișier.

Я могу использовать стрелки, чтобы идти вверх и вниз, я могу искать файл.

> De exemplu când caut prima persoana care se numește "Mathieu", voi ajunge pe prima linie cu o persoana numita "Mathieu”.

Например, когда я ищу первого человека по имени 'Матье', я попаду на первую строку с человеком по имени 'Матье'.

> Va vorbeam de asemenea de comanda "less", care face cam același lucru, dar e si mai avansata.

Я также говорил о команде 'less', которая делает то же самое, но еще более продвинута.

> Deci va sfătuiesc sa folosiți "less", caruia ii sunt adaugate tot timpul noi funcționalități, si care e actualizata, spre deosebire de "more" care acum e cam moarta.

Поэтому я советую вам использовать «less», к которому постоянно добавляются новые функции и который обновляется, В отличие от «more», который сейчас мертв.

> Aceasta comanda "less" e utilizata pentru "man", pentru a avea efectul de deplasare, de cautare, etc. Deci puteti avea același lucru pe propriile fișiere.

Команда 'less' используется для 'man', чтобы иметь эффект перемещения, поиска и т. Д. Таким образом, вы можете иметь то же самое в своих файлах.