### video: [Introduction to pointers](https://youtu.be/lxpt8AVQ5Kc) ###

---

Здравствуйте и добро пожаловать на day03, день указателей.
> Buna ziua si bine ati venit la ziua 03, ziua pointerilor.
> Hello and welcome to day 03, the day of the pointers.

Указатели - это новый тип переменных, которые вы изучите.
> Pointerii reprezinta un tip nou de variabila pe care ii veti invata.
> Pointers are a new type of variable that you will learn.

Это, на мой взгляд, один из наиболее полезных типов переменных в C, который позволяет хранить адрес другой переменной и изменять его удаленно, и конечно, вскоре мы увидим как это сделать.
> Este dupa parerea mea unul dintre cele mai utile tipuri de variabile in C, care va permite sa stocati adresa unei alte variabile si sa o modificati la distanta, si vom vedea imediat cum.
> It is in my opinion one of the most useful types of variables in C, which allows you to store the address of another variable and modify it remotely, and we will see immediately how.

Чтобы использовать указатели, вы должны понимать один важный элемент: память.
> Pentru a putea utiliza pointerii e nevoie sa intelegeti un element important: memoria.
> To use pointers you need to understand one important element: memory.

При запуске, процесс имеет право использовать всю память в 32 bits: 4 GB, а 64 bits: 2 GB при мощности 64.
> Atunci cand este lansat, un proces are drept sa utilizeze toata memoria, in 32 de biti: 4 GB, iar in 64 de biti: 2 la puterea 64, faceti voi calculale.
> When it is launched, a process has the right to use all the memory, in 32 bits: 4 GB, and in 64 bits: 2 at the 64 power, you make calculations.

Это и есть виртуальная память.
> Aceasta este memoria virtuala.
> This is virtual memory.

Эта память отображается либо в ОЗУ, либо на жестком диске; поищите информацию на эту тему, чтобы узнать больше о памяти, в том числе о подкачке памяти.
> In spate, aceasta memorie este mapata sau in memoria RAM sau pe hard-disk; faceti o scurta cautare sa aflati mai multe depre memorie, inclusive despre memoria swap.
> In the back, this memory is mapped either in RAM or on the hard disk; make a short search to find out more about memory, including about swap memory.

Эта память управляется MMU (блоком управления памятью), что позволяет нам иметь память в определенном месте (физически) на компьютере.
> Aceasta memorie este gestionata de MMU (Memory management unit), care ne permite sa avem memoria intr-un anume loc (fizic) pe calculator.
> This memory is managed by MMU (Memory management unit), which allows us to have memory in a certain place (physically) on the computer.

Однако, процесс имеет собственную область памяти, которой он управляемуют автономно.
> In schimb un proces are alocata o zona de memorie proprie pe care o gestioneaza autonom.
> Instead, a process has its own memory area that it manages autonomously.

Память разделена на две части: память высокого уровня и память низкого уровня.
> Memoria este divizata in doua parti: memoria de nivel inalt si memoria de nivel jos
> The memory is divided into two parts: high level memory and low level memory.

Высокоуровневая память называется ("stack").
> Memoria de nivel inalt este numita stiva ("stack").
> High-level memory is called a stack.

Например, при выделении переменной «int» выделитcя 4/8 байтов (в зависимости от архитектуры) памяти в stack'e, то есть в памяти высокого уровня.
> Atunci cand alocati o variabila de tip "int" de exemplu, alocati 4/8 bytes (in functie de arhitectura) de memorie pe stiva, deci pe memoria de nivel inalt.
> When allocating an "int" variable for example, allocate 4/8 bytes (depending on the architecture) of memory on the stack, so on high level memory.

Таким образом, вы находитесь наверху всего в памяти, на уровне 2A64, и медленно спускаетесь вниз, насколько вы добавите новых элементов, настолько и понизится stack.
> Deci sunteti sus de tot in memorie, la nivelul 2A64, si coborati incet, incet; cu cat adaugati mai multe elemente cu atat coborati in stiva.
> So you are at the top of everything in memory, at level 2A64, and go down slowly, slowly; as you add more items as you lower the stack.

Низкоуровневая память называется «heap». Мы изучим это в другой день.
> Memoria de nivel jos este numita "heap". O vom analiza intr-o alta zi.
> The low level memory is called "heap". We will analyze it another day.

Это область, где вы можете выделить память, но, как я уже сказал, мы изучим это в другой день.
> E zona in care puteti voi sa alocati memorie, dar cum am spus vom vedea asta in alta zi.
> It is the area where you can allocate memory, but as I said we will see this another day.

Итак, начиная со следующего видео мы продолжим говорить об указателях, как они работают, как мы можем их использовать, о номенклатуре и т.д.
> Deci vom merge mai departe sa vorbim despre pointeri, cum functioneaza, cum ii putem folosi, nomenclatura, etc., incepand cu videoul urmator.
> So we will go on to talk about pointers, how they work, how we can use them, nomenclature, etc., starting with the following video.