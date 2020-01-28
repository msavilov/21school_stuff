> Deci acum ca am văzut cum sa ne plimbam in sistemul de fișiere, si ce este un sistem de fișiere, sperând ca ati inteles bine, vom vedea cateva comenzi care va vor fi utile in piscina sperând ca ati înțeles bine, vom vedea cateva comenzi care va vor fi utile in piscina si de altfel, care va vor fi utile tot timpul.

Итак, теперь, когда мы увидели, что такое файловая система и как ее просматривать, надеюсь, вы самостоятельно запомнили, как это делать, то давайте посмотрим на некоторые команды, которые будут полезны вам до конца Бассейна по Си и сам факт пользы будет периодический.

> Prima e comanda "touch", care va permite sa creați un fișier, comanda "cat" care va permite sa vedeți ce e in fișier si vi-l afiseaza pe ecran, comanda "cp" care copiaza, "mv" care muta, "rm", pe care am vazut-o deja impreuna, si va permite sa stergeti, si "chmod" care va permite sa schimbați drepturile pe un fișier sau un director, lucru important, ca prietenii voștri sa nu se amuze stergandu-va fișierele de exemplu; știind ca oricum vor incerca.
>The first is the "touch" command, which will allow you to create a file, the "cat" command that will allow you to see what's in the file and display it on the screen, the "cp" command that copies, "mv" that moves, " rm ", which we have already seen together, and will allow you to delete, and" chmod "which will allow you to change the rights on a file or a directory, important thing, that your friends will not have fun deleting your files. example; knowing they'll try anyway.
>the first command line is "touch" - create file, "cat" - previewer files content (displays a file content on screen), "cp" - copy, "mv" - move, "rm" - remove (as seen earlier on), "chmod" - changes access permissions to file system objects, that's important to know in order to dodge classmates pranks on your work, they'll try anyway.

Первая команда "touch" - создать файл, "cat" - обзор содержимого файла (выводит содержимое на экран), "cp" - копировать, "mv" - переместить, "rm" - удалить (как вы уже видели), "chmod" - сменить права доступа к объектам файловой системы, это очень важно знать, чтобы избежать пранков над вашей работой, вашими одноклассниками.

> Deci, prima comanda: "touch".

И так, первая команда "touch".

> La fel, când nu stiti, tastati, vedeți ce se intampla, si daca sunteti șmecheri faceți "man touch", si asa stiti cu ce opțiuni o puteti utiliza.

И как всегда, давайте попробуем. Очевидно, что "touch" просто бесполезно, поэтому давайте введем "man touch". Как обычно, краткое содержание, описание и опции.

> La fel: rezumatul, descrierea si opțiunile, si asa mai departe.
> Deci, "touch"... Fac "cd", sunt in directorul meu, fac "ls”, bine, creez un director.
>so, "touch"... If I type "cd" and then "pwd"  in my directory, "ls -la" lists all the files in the directory, let's create a new directory "mkdir Krpestbeu", "ls" my directory is being created.

И так, "touch"... Я напишу "cd", потом "pwd" в своем каталоге, выведу подробно информацию о содержимом в каталоге через "ls -la", теперь создам новый каталог "mkdir Krpestbeu", затем "ls" и собственно увижу созданный каталог.

> Directorul e creat aici.
> let's go in "cd Krpestbeu" and "ls" it's empty. now let's create our first file "touch beeoneestpasbeau", here we go, "ls -la" my new file is here.

Теперь перейдем "cd Krpestbeu" и через "ls" увидим, что там пустой. Теперь создадим первый файл "touch beeoneestpasbeau", ну вот, теперь через "ls -la" видим, что наш новый файл тут.

> Intru in el. Si aici scriu "touch" si imi creez fișierul. Asa, deci am fișierul meu caruia pot sa-i spun oricum. O mica precizare: daca scrieți asta, nu da același rezultat. Va las sa va dati seama singuri ce s-a intamplat, nu va explic.
>just so you know, if you do this "touch bee one est pas beau" here's what happens see on screen, you can figure it out on your own.

И чтобы вы лучше понимали, если я сделаю так "touch bee one est pas beau", то вот что произойдет, посмотрите на экран и думаю вы сами все поймете.

> Si după ce facem curățenie, la fel, cu comanda "rm", si aici iarasi va arat ceva si va las sa va dati seama singuri ce face. Atentie: a se folosi cu precauție! Asa, deci am directorul meu.
> and now if you want to clean it out, you can use the command "rm", I'm going to add a little something to the "RM" command line, you can figure it out for yourselves. but remember to use this with caution.

Теперь, если вам нужно удалить что-то, то вы можете воспользоваться командой "rm", я добавлю некоторые опции к этой команде, думаю вы сами сможете выяснить, за что они отвечают, но не забывайте использовать все это с некоторой осторожностью.

> Am văzut "touch". Acum ca am văzut cum creem fișiere, ne vom uita ce e inauntru fișierului. Pentru asta exista comanda "cat". Nu va arat manualul de fiecare data, cred ca ati înțeles logica. Deci daca fac "cat" pe un fișier .c, sau de orice alt fișier, ce e in fișier va aparea pe ecran.
> I saw "touch". Now that we've seen how we create files, we'll look at what's inside the file. For this there is the command "cat". I will not show you the manual every time, I think you understand the logic. So if I do "cat" on a .c file, or any other file, what's in the file will appear on the screen.
>so we've covered touch, now that we can create files let's check out their content. in order to do that we'll use the following command line "cat". I'm not going to read you the man every single time, I hope you get it by now. so "cat" on a file .c or whatever type of file for that matter. what is in that file will be displayed on-screen.

И так, мы рассмотрели команду "touch", теперь, когда мы можем создавать файлы, то давайте просмотрим их содержимое. Чтобы это сделать, мы будем использовать команду "cat". Я надеюсь вы поняли, что я не собираюсь каждый раз читать вам man. И так "cat" файла с расширением ".c" или любого другого расширения, которое нас будет волновать. То, что будет находиться в файле будет выведено на экран.

> Atentie, merge cu orice; cu fișierele de tip text, si de asemenea cu fișierele binare. Vom vedea mai târziu; veți avea surprize, nu va da același rezultat. Deci știu crea un fișier, știu sa ma uit in el, acum vom invata sa copiem fișierul. Ma intorc in super directorul meu unde nu e nimic, fac un "touch". Vom schimba, ceva mai original de data asta. Fac un "ls", si vad fișierul meu. Acum, am greșit si am creat fișierul in directorul "Krpestbeau", dar voiam sa-l pun in directorul meu "home".
>
> Attention, it goes with everything; with text files, and also with binary files. We will see later; you will have surprises, it will not give the same result. So I know how to create a file, I know how to look in it, now we will learn how to copy the file. I go back to my super director where there is nothing, I make a "touch". We will change, something more original this time. I'm doing an "ls", and I see my file. Now, I made the mistake and created the file in the "Krpestbeau" directory, but I wanted to put it in my "home" directory.
>
> works on everything, files .c, files txt, binary files, we'll see that later on. so now you know how to create a file, I also know how to look inside one, now I need to know how to copy a file. Lets go back to my awesome directoty which is empty. "touch" something original, the name of the file has no importance. "ls"...yeap it's here. Oh nooo, I've made a mistake, it's in my "Krpestbeau" directory I want to be it in my home directory.

Это работает со всеми расширениями, .c файлы, .txt файлы, бинарные файлы, все это мы позже рассмотрим. И так теперь вы знаете как создавать файлы, также знаете как просматривать то, что находится внутри этих файлов, теперь нам нужно узнать, как копировать файлы. Давайте вернемся в мой офигенный пустой каталог. Создадим что-нибудь оригинальное через "touch", имя файла особой роли не играет. "ls"... и агамс, файл тут. О нееет( Я кое-где ошибся, он находится в каталоге "Krpestbeau", а мне нужно, чтобы он был в моем "home" каталоге.

> In cazul asta, folosesc comanda "cp", care copiaza, pun fișierul sursa, sursa a ceea ce vreau sa copiez, si destinația. De cele mai multe ori sub Unix ordinea e sursa, apoi destinație. Si deci directorul părinte. Daca fac asta, mal am inca fișierul acoJo unde ma aflu, si daca fac "cd pentru a urca in directorul de deasupra, si fac un "ls", vad fișierul "30_1estgentir care a fost copiat. Si, bineînțeles, daca șterg fișierul "30_1estgentil", si ma intorc in "Krpestbeau", il am inca aici (pentru ca a fost copiat).
>
> In this case, I use the "cp" command, which copies, puts the source file, the source of what I want to copy, and the destination. Most times under Unix order is the source, then destination. And so the parent director. If I do this, I still have the file where I am, and if I do "cd to go up to the directory above, and do a" ls ", I see the file" 30_1estgentir that was copied. And, of course, if I delete the file "30_1stgentil", and I go back to "Krpestbeau", I still have it here (because it was copied).
>
> that's okay though, I know "cp". "cp source destination" source equals file, destination equals the directory, you'll notice that source destination is pretty standard in UNIX. So, "cp" "myfile" "myparentdirectory", in this case is my home directory.  if I do "ls" my file is still here and if I do "cd" then "ls" my files also here as it's been copied. If I remove this one with "rm" the file is gone, but the original copy is still there.

Ничего страшного, я ведь знаю команду "cp". "cp soure destination", source - это ваш файл, destination - каталог, вы потом еще заметите, что source и destination довольно таки стандартизировано в UNIX. И так, "cp" "myfile" "myparentdirectory", в данном случае это "home" каталог. Теперь, если я сделаю "ls" то мой файл все еще здесь, а если я сделаю "cd", потом "ls", то мой файл также здесь, так как я его скопировал. Если я удалю файл через "rm", то он исчезнет, но его копия останется здесь.

> Mai departe: l-am copiat, dar voiam sa-l mut (m-am încurcat prima data, nu sunt prea talentat). Imi zic, de data asta chiar il voi deplasa: deci exista o comanda care se numește "mv". Toate comenzile in Unix, ca regula generala, au o logica. "cp" - copiez, "mv" - "move", "ls" - listez, si asa mai departe. Deci "mv", sursa, si destinația. Acum daca fac "ls", nu mai e aici, "30_1estgentil” a plecat, si e aici. In plus veți vedea ce data e aici, deci ca a fost mutat acum.

> Asa, deci știu deplasa, știu copia, știu șterge (asa, deci a dispărut), ne mai ramane un lucru de văzut, "chmod". "chmod”, cum indica si numele, schimba "modul", schimba drepturile pentru a fi mai exact. Revin in directorul meu. Un mic sfat, Unix e "case sensitive", bănuiesc ca stiati, dar in caz ca nu, asta inseamna ca daca puneți o majuscula in numele fișierului vostru, tine cont de majuscula. Puteti avea doua fișiere cu același nume, unul cu majuscule, unul cu litere mici, nu e același fișier. Deci "chmod", fac un "touch", asa, mi-am creat fișierul.

> O data creat, aveți ca de obicei numele, si drepturile asociate.

> Deci, nu are "d", e un fișier, "r" pentru "read", "w" pentru "write", "x" pentru "execute".

> De fiecare data veți avea drepturile voastre (unu, doi, trei),

> drepturile pentru cei din același grup ca voi (care e grupul "staff' in cazul de fata),

> Si drepturile pentru restul planetei. Adică cei care nu sunt in grupul vostru, si care nu ești tu.

> Va voi da doua exemple, si apoi va veți descurca cu "man", experimentând si vazand ce se intampla.

> Dacâ fac un "chmod.OOO" deci 0 pentru mine, 0 pentru cei din grupul meu, 0 pentru planeta intreaga, cu numele fișierului meu,

> ce se intampla: nu mai e nici un drept pe fișier.

> Imi veți spune, cum pot schimba acum drepturile? Unix e inteligent, știe ca e fișierul vostru, va aparține.

> Daca faceți "7" pentru voi, deci "700", Enter, si faceți un "ls -la" (atentie, doar "ls" nu va afiseaza drepturile),

> "ls -la" si numele de fișier, am deci drepturile de citire, scriere, executare.

> Grupul meu nu are drepturi, si restul planetei nu are drepturi.

> Daca altcineva decât voi incearca sa citească fișierul vostru, nu va avea acces.

> Nici la citire, nu va putea face "cat" pe el, nu va putea sa-l copieze, nu va putea face nimic cu el.

> Daca vreau de exemplu sa fac ca oamenii sa poate doar citi fișierul meu,

> ”644”, si ce se intampla acum?

> Eu am drepturile de citire si scriere.

> Ati remarcat ca am îndepărtat "x"-ul, care se refera la executare pentru fișierele binare,

> aici e un fișier text, n-avem nevoie sa-l executam, deci l-am sters, nu folosește la nimic.

> Grupul meu poate citi, si restul planetei poate citi.

> In schimb nu au "w"-ul, deci nu au drepturile de scriere, si nu vor putea sa scrie in fișier.

> Daca vin in directorul vostru, si fac un "cat" si numele de fișier, cum v-am aratat inainte, vor vedea ce e in el.

> In cazul de fata e gol, dar vor vedea ce e in el.


> Deci "chmod" e un pic complicat la inceput, va trebui sa va obisnuiti,

> experimentați făceți teste, veți vedea de fiecare data ce se intampla de fiecare data când schimbați "chmod"-ul,

> "555" de exemplu pentru fanii Subaru, faceți "ls -la", si s-a intamplat ceva.

> Vedeți ce se intampla, incercati sa intelegeti, si nu va faceți probleme, chiar daca va stergeti toate drepturile, putem sa vi le redăm.
