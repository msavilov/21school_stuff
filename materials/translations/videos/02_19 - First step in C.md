> Buna ziua si bine ati venit in aceasta prima zi de limbaj C, ziua 02. 

> Vom vedea impreuna cum sa scrieti primul vostru program si cum sa il compilati astfel incat sa fie executat de catre calculator.

> Mai intai, vom deschide cu "emacs" un fisier jour02.c. 

> Extensia .c ne va permite noua si calculatorului sa recunoastem ca este vorba de un fisier sursa. 

> Dupa ce ati deschis un fisier .c cu ajutorul utilitarului "emacs" veti genera un header folosind combinatia de taste Control+C, Control+H. 

> Aceasta combinatie va genera un header standard de-al scolii. 

> Daca folositi utilitarul "vim", va trebui sa folositi tasta F1. 

> Vom incepe prin a declara punctul de intrare in program: functia "main". 

> Fiecare functie scrisa in limbajul C are asociat un tip. 

> Acesta este tipul valorii returnate de functie. Vom incepe asadar sa scriem functia "main" care returneaza o valoare de tip "int".

> Daca functia nu ar returna nimic, vom scrie ca returneaza "void" (care e o valoare nula). 

> Deci nu va returna nimic. 

> Intrucat functia noastra returneaza un "int", 

> vom scrie o instructiune "return(O)" care semnifica faptul ca programul s-a incheiat fara eroare. 

> Prin conventia aceasta semnifica faptul ca totul s-a terminat cu bine. 

> In mod normal, functia "main" are argumente, dar in cazul acestui program vom neglija acest aspect.

> Tocmai am scris o functie care nu face nimic, 

> doar returneaza valoarea 0 semnificand faptul ca executia programului s-a incheiat fara eroare. 

> Vom salva fisierul folosind Control+X, Control+S. 

> Folosind Control+Z vom pune editorul "emacs" in background. Vedeti in "shell" ca e suspendat. 

> Vom compila fisierul folosind compilatorul "gcc". 

> Compilatorul "gcc" are mai multe optiuni. 

> Vom folosi optiunea "-o" care permite specificarea fisierului de iesire, numele executabilului pe care-l vom crea.

> Vom indica un nume pentru fisierul de iesire: jour02. 

> Si-i dam fisierul sursa, jour02.c. 

> Atentie sa nu folositi drept fisier de iesire, fisierul sursa pe care tocmai l-ati creat (jour02.c), deoarece compilatorul va suprascrie continutul acestuia!

> "gcc" a creat fisierul executabil. 

> Priviti, in director avem un fisier jour02 si un fisier jour02.c. 

> Putem executa acum, dupa cum indica drepturile fisierului (optiunea x). 

> Pentru a fi sigur ca executam un fisier din directorul current vom folosi si jour02. 

> Programul este executat si cum nu face nimic, nu vedem nimic afisat. 

> In continuare il vom face sa afiseze ceva. 

> Cu "fg" repunem "emacs" in prim plan ("foreground"). 

> Vom folosi apelul de sistem "write". 

> Vom folosi iesirea standard, care are identificatorul de fisier 1. 

> Vom afisa un singur caracter, si-i spunem cate caractere are sirul, deci unul singur.

> Vom verifica manualul (man) functiei "write". 

> Vom face asta prin Windows+X, man. 

> Si ne vom uita la "man 2 write". 

> "Write" este un apel sistem. Man-urile sunt clasificate pe tipuri, iar 2 este tipul sistem. 

> Deci am cerut "man"-ul de tip 2 al lui "write". 

> Fereastra este impartita in doua. 

> Pentru a trece de la o fereastra la alta folositi Control+X, O. 

> Primul lucru: "write" necesita folosirea header-ului <unistd.h>, pentru ca compilatorul sa stie care e declaratia lui "write",

> si sa stie care-i sunt parametrii, si cel de retur. 

> Deci vom scrie... "#include <unistd.h>". 

> Folositi tot Control+X, O pentru a trece de la o fereastra la alta. 

> "write" cere un file descriptor, deci 1, care reprezinta iesirea standard a programului nostru, 

> un buffer care e un sir de caractere (noi i-am dat unul care contine doar 

> si dimensiunea (numarul de bytes care trebuie scrisi). 

> Salvam programul cu Control+X, Control+S. 

> Control+Z pentru a suspenda "emacs". 

> Si relansam compilarea. 

> Totul a decurs ok. 

> Relansam programul. 

> Si ne afiseaza un pe ecran. 

> De ce ne afiseaza un procent dupa? 

> Poate pentru ca nu avem un retur la linie. 

> Adaugam un retur la linie ("\n") si-i spunem ca sirul nostru are acum 2 caractere. 

> Recompilam. 

> Si relansam. 

> Acum pare mai bine. 

> Acum ca am facut aceasta prima functie, vom pune "write" intr-o functie "ft_putchar()",

> care va returna si ea un "int". 

> Deci "putchar" va lua un parametru "char c". 

> Si vom pune "write"-ul din "main" mai sus. 

> Folositi Control+K pentru operatia "Cut" (de doua ori pentru a lua si returul la linie). 

> In functia noastra putem scrie caracterul pe care l-am primit. 

> Aici vom face ceva ce e probabil cam complicat pentru voi, 

> vom da adresa caracterului in loc de caracterul in sine (cu 

> ceea ce ne va permite sa-l transformam in sir de caractere (ceea ce numim "char *"). 

> Deci aici putem sau sa returnam 0 (totul e ok), sau sa punem "void" (functia nu returneaza nimic).

> In cazul de fata doar returnam 0. 

> Vom folosi functia "ft_putchar". 

> Si aici vom folosi' in loc de ", pentru a preciza ca e un caracter, 

> si nu un sir de caractere. 

> Si o vom face de doua ori, pentru a putea transmite si "\n". 

> Folositi Control+X, 1 pentru a inchide fereastra "man" din partea de jos. 

> Programul nostru se va executa incepand cu "main". 

> Apoi intram in "main", 

> apelam functia "ft_putchar", pe care o vedem aici, 

> scrie ceea ce i-am dat in parametrul "char c", 

> face "return", si ne gasim la finalul acestei functii. 

> Apoi continuam. 

> Si ajungem la "ft_putchar" care afiseaza returul la linie, "\n". 

> La fel, revenim aici, la "write", cu "c" egal cu '\n', revenim din functie, si am terminat.

> Testam. 

> Cu Control+X, Control+S salvam programul. 

> Recompilam. 

> Relansam. 

> Si a afisat ceea ce voiam. 

> Trecem la o ultima etapa putin mai complicata: o functie care afiseaza de "n" ori caracterul trimis ca parametru. 

> O numim "ft_nputchar". 

> "c" este caracterul pe care vrem sa il scriem, iar "int n" este numarul de aparitii. 

> Aici folosim acest "int n" pentru a numara. 

> Deci sau il vom modifica (decrementandu-l), vom folosi un contor "i",

> care porneste de la 0. 

> Cat timp "i" este mai mic decat "n", 

> vom afisa in bucla caracterul

> apeland functia "ft_putchar". 

> Si vom incrementa contorul "i", 

> "j = j + 1" pentru a avea contorul de bucla, 

> si o data ce "i" este egal cu "n", ne oprim. 

> Deci daca dam un parametru "n" egal cu 1, 

> incepem cu i = 0, 

> 0 < 1, deci totul e ok si executam prima data bucla. 

> Incrementam "i" cu 1 si acesta trece de la 0 la 1. 

> Revenim in bucla, si avem 1 < 1, 

> expresia e falsa. 

> Deci bucla se opreste. 

> Si ne aflam aici, returnand 0 pentru ca functia e gata. Vom incerca acelasi lucru, vom apela "ft_nputchar" pentru a afisa de 42 de ori caracterul 

> si apoi un retur la linie. 

> Control+Z pentru a pune "emacs" in background. 

> Recompilez. 

> Relansez. 

> Sa verificam. 

> In mod normal vom avea 43 de caractere, pentru ca avem si caracterul "\n" la final. 

> Avem deci 43 de caractere ca rezultat al programului nostru. 

> Sunteti acum pregatiti sa scrieti primul vostru program in C. 

> A fost un exemplu foarte simplu. 

> Nu mai ramane decat sa treceti la treaba! Multumesc.