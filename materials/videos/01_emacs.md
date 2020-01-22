Let's get started with libraries.

I've prepared two files, function "ft_putchar.c" and "ft_putstr.c".

I'am sure you'll all know what these do.

Syntax may be a little different, but I'am sure you'll understand how I did it.

But that's not our main focus right now.

I simply get back to creating a basic program.

So, you know that if I wanted to write "bonjour les gens\n" (Hello people), thanks to our function "ft_putstr", I should write a "main", that calls this function and then compile.

We agree, that if I only compiled my main.c, the compilers gonna have it go at me and tell me, thanks for calling function "ft_putstr" but as I don't know what it is I can't do what you're asking.

So let's add function "ft_putstr.c" and now it tells me "I can't find function "ft_putchar" you're calling in function "ft_putstr.c".

So let's add function "ft_putchar.c" and now it should compile, and display my "bonjour les gens\n".

I'm telling you all of this again, because in order to create libraries, well first need to compile the functions you want to put in it.

if I compile just my function "ft_putstr.c", it will tell me that it still isn't a function "ft_putchar", but most importantly we need a "main", in order to create an executable, as we've learned earlier on in the bootcamp.

But I need to add my function "ft_putstr" to my library and I dont need my "main".

For that "gcc" as an option "-c". Check out the "man" for more info.

But look, it's created a ".o", function "ft_putstr.o". It's an object, it's computer language.

As you can see, if you try to display it, it's nonsensical. Our new computer can read it.

But in order to do anything, we'll need a main.
As I sad earlier, in order to create a library we'll need ".o" files.

Just imagine your program is a wall and your ".o" file is a brick, a brick that's ready and that you'll be able to place in more than one more.

In the sense that's once you've made your brick, you won't need to make it again and each time you'll be able to use it everywhere.

Thats actually quite practical. "gcc" knows about it, you could simply just use our ".o" line this.

---

> Buna ziua tuturor si bun găsit la acest video de introducere.
Привет всем и добро пожаловать на это вводное видео.

> Acest video prezintă “emacs”, unul din cele doua editoare de text
В этом видео мы поговорим о "emacs", один из двух текстовых редакторов

> pe care noi vi le recomandam sa le utilizați.
который мы рекомендуем вам, в дальнейшем, использовать.

> Așadar, cum lansam “emacs” ?
Итак, чтобы запустить "Emacs",

> Pentru a lansa “emacs” e suficient sa tastam
вам нужно введите в консоли "emacs" и имя файла

> in consola “emacs” si numele fișierului.

> O data ajunși in “emacs”, pentru a ieși trebuie tastat “control-X” “control-C
Для того, чтобы выйти из "emacs", введите "ctrl-x" и "ctrl-C".

> Acum ca știm cum sa ieșim din “emacs”,
Теперь, после того как мы узнали, как выйти из “emacs”,

> vom putea incepe sa modificam fisierul.
мы сможем изменить файл.

> Pentrul a-l modifica, nimic mai simplu:
Для того, чтобы изменить его:

> incepem sa testam textul pe care vrem sa-l scriem.
мы просто пишем текст, который захотим.

> O data textul modificat, pentru a-l salva tastam "control-X" "control-S"
Чтобы сохранить наш набранный текст, нажмитие "ctrl-X" "ctrl-S".

> Putem vedea in partea de jos ca intr-adevar
В нижней части экрана вы можете увидеть на какие клавиши нажимать.

> continutul s-a salvat in dosarul "dossier" in fisierul "main.c".
содержимое было сохранено в папке "dossier" в файле" "main.c".

> O mica informatie care v-ar putea fi utila,
Немного информации, которая может вам пригодиться,

> si anume cum sa trecem aplicaatia in background.
а именно как запустит приложение в фоновом режиме.

> Aceasta nu e specifica programului "emacs"
Это не относится к программе "emacs",

> ci sistemului de operare (shell) care va permite sa faceti asta;
это shell комманда, которая позволяет вам это делать;

> tastand “control-Z" puteti suspenda “emacs”,
набрав «ctrl-Z», вы cможете приостановить «emacs»

> pentru a avea acces la consola si a tasta alte comenzi.
для того, чтобы получить доступ к консоли и вводить другие команды.

> De indata ce tastati “fg” veți reveni in “emacs” acolo unde l-ati oprit.
Введя в консоли “fg” вы вернетесь в “emacs”, там, где вы его приостановили.

> Apoi, pentru a va deplasa mai rapid,
Чтобы быстро передвигаться по тексту,

> puteti tasta "control-E" sau "control-A"
вы можете нажать "ctrl-E" или "ctrl-A",

> pentru a merge direct la inceputul, respectiv sfarsitul liniei.
тем самым вы перейдете к концу или к началу строки.

> Pentru a face cautari, de exemplu pentru a cauta cuvantul "return",
Для поиска, например, для поиска слова "return",

> tastati “control-S” si textul “return”, iar programul il va găsi.
введите "ctrl-S" и искомое слово "return".

> Pentru a deschide un alt fisier, tastati "control-X" "control-F".
Чтобы открыть другой файл, введите "ctrl-X" "ctrl-F".

> In partea de jos vedeti ca programul cauta ruta unui nou fisier,
Внизу видно, что программа просит ввести название файла,


> deci daca scrieti "main.c" de exemplu, programul deschide acelasi fisier.
так что, если вы напишите "main.c" например, то соотвественно программа откроет этот файл.

> Daca deschideti un fisier nou, programul va deschide
Если вы откроете новый файл,

> o zona de editare (buffer) goala unde veti putea scrie functia voastra de test,
то программа откроет пустую область редактирования (буфер), в которой вы сможете записать свою тестовую функцию,

> iar pentru a-l salva tastati "control-X" "control-S".
и чтобы сохранить его, введите "ctrl-X" "ctrl-S".

> Acum vreau sa pot vedea la stanga fișierul de test iar la dreapta fișierul “main".
Теперь, я хочу слева на экране увидеть тестовый файл, а справа "main" файл.

> Pentru asta trebuie sa impart ecranul pe verticla (split),
Для этого я должен разделить экран по вертикали (split),

> iar pentru asta tastez "control-X" "3"
и для этого я нажму "ctrl-X" "3"

> Pentru a imparti ecranul pe orizontala voi putea tasta "control-X" "2"
Чтобы разделить экран по горизонтали, я должен нажать "ctrl-X" "2"

> Pentru u ma deplasa dintr-o zona de editare in alta, voi tasta "ctrl-x" "o"
Чтобы перейти из одной области редактирования в другую, я нажму "ctrl-x" "o"

> si se vede ca intr-adevar cursorul se deplaseaza.
и вы можете наблюдать, что курсор передвигается по этим областям.

> Daca doresc sa inchid o zona de editare, voi tasta "ctrl-x" "0" (zero),
Чтобы закрыть текущую область редактирования, введите "ctrl-x" "0" (ноль),

> are inchde zona curenta.

> Deci, daca vreau sa deschid alt fisier, cum am facut mai inainte,
И так, чтобы открыть другой файл

> voi tasta “control-X” “control-F’ si recuperez fișierul “main.c".
Я нажму "ctrl-X", "ctrl-F" и верну файл "main.c" обратно.

> lata deci o utilizare simpla de "emacs"
Такое вот простое использование "emacs"

> care va va fi suficienta in timpul "piscinei"
будет достаточным во время "бассейна",

> pentru a edita si a face exercitiile care vi se vor cere.
для редактирования и выполнения заданий.

> O ultima infomatie: pentru exercitiile de C,
И еще кое-что: для упражнений на С,

> va vom cere sa introduceti antetul scolii 42,
мы будем просить вас ввести заголовок школы 42,

> pentru aceasta veti face "ctrl-C" "ctrl-H",
для этого нажмите "ctrl-C" и "ctrl-H",

> care va crea antetul 42.
и у вас появится заголовок школы.

> Multumesc frumos.
Вуаля, спасибоу.