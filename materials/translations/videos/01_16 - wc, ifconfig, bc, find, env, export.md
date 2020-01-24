> Vom vedea acum un mic numar de comenzi care va vor fi foarte utîle. 

> Tunt niste comenzi foarte usoare, pe care nu vom petrece foarte mult timp. 

> Prima e "wc" si pur si simplu va calcula numarul de linii, de caractere si de cuvinte care sunt inf^jrHÎsîer 

> Daca iau fisierul exemplu de inainte, si fac un "wc" pe acest fisier, voi vedea ca sunt 400 de linii, 405 cuvinte si 7446 caractere. 

> "wc" poate primi mai multe fisiere ca si parametri. 

> "wc *" imi va da pentru fiecare fisier din director numarul de linii, etc., si-mi va da si totalul. 

> Aceasta comanda, ca toate celelalte vazute azi, poate sa citeasca pe intrarea standard. 

> Daca fac "cat" si numele fisierului nostru, recuperez numele "Thomas", 

> si apoi il redirectez spre "wc -I" pentru a avea doar numarul de linii, 

> voi vedea ca exista 7 "Thomas" in baza de date. 

> E foarte practic pentru a numara rezultatele. 

> Alta comanda simpla e comanda "file". 

> "file" va va da pur si simplu informatii despre fisierul dat ca parametru. 

> Aici putem vedea ca acest fisier e in UTF-8, ca e fisier text, deci are un tip MIME care corespunde la text, numarul magic al fisierului, etc.

> Alta comanda, "ifconfig", care va va da informatii despre reteaua voastra. 

> De exemplu puteti vedea adresele IP, adresele MAC, etc. 

> Ultima comanda tot destul de usoara: comanda "bc". 

> "bc" e foarte simplu: e un calculator. 

> Daca tastati "2+3", va va da rezultatul "5", nimic complicat. "bc" e foarte puternic, poate face multe calcule stiintifice, cosinus, sinus, exponentialele, puterile, etc.

> oate face calcule de baza de numeratie: poate face un calcul in baza 2 si sa va dea rezultatul in baza 16, etc. 

> Deci "bc" e foarte util, si in plus, citeste din intrarea standard, deci daca fac "echo 1 +2" si il trec prin "bc", imi va da "3".

> Deci "bc" poate fi util daca vrem sa calculam de exemplu suma numarului de linii, sau alte lucruri de genul asta. 

> Ultima comanda pe care o vom vedea azi, care e putin mai complicata, dar nici ea nu e foarte grea, e comanda "find". 

> find" in mod normal va lista toate fisierele din directorul pe care i-l dam ca parametru. 

> Deci "find ." ne va da toate fisierele din 

> Daca facem "find /usr" ne va da toate fisierele din 'Vusr".

> Observam ca face o cautare recursiva, deci va cauta de asemenea si in subdirectoare. 

> Unde "find" e foarte puternica, e cand incepem sa filtram fisierele pe care le dorim. 

> exemplu, filțrul cel mai simplu e dupa nume; deci daca vreau toate fisierele care incep cu "Is", aceasta comanda ni le va da. 

> Putem filtra dupagdata ultimei modificari, putem filtra dupa marime, putem filtra dupa faptul ca e un fisier, director, executabil, etc. 

> "find" va va permite de asemenea sa faceti actiuni pe aceste fisiere. 

> Puțem sa le afisam, putem sa le stergem, putem lansa alte comenzi plecand de la "find"; "find" e intr-adevar foarte puternica. 

> Nu vom face turul tuturor optiunilor; va rog sa cautati pe Internet, pe "man find" dar si cum oamenii folosesc "find", 

> pentru a vedea toate posibilitatile disponibile pentru aceasta comanda. 

> Ultimul lucru pe care vreau sa-l vedem e ceea ce numim "mediul". 

> Ce e mediul ("environement")? 

> E pur si simplu o lista de variabile prezente in "shell" si care sunt transmise in mod automat tuturor fisierelor binare, si tuturor scripturilor. 

> Daca facem "env" vom vedea lista acestor variabile. 

> Vedem ca se merge pe un sistem de cheie si valoare; "PATH" are aceasta valoare. 

> "PATH" e folosit de "shell" de exemplu ca sa stie unde se gasesc toate fisierele binare. 

> Vom avea utilizatorul vostru ("user"), care se numeste "bocal" in cazul de fata. 

> Vom avea "TERM" care la noi e "xterm", etc. 

> La ce foloseste asta? 

> La a parametra scripturile "shell". 

> De exemplu daca vrem sa adaugam o variabila "LINE", 

> care corespunde la numarul de linie pe care sa-l caute scriptul, putem face "LINE=3". 

> Daca ne uitam in mediul nostru, variabila "LINE" a fost creata cu valoarea "3 

> si pentru a o accesa putem scrie pur si simplu "$LINE". 

> Daca fac "echo $LINE", se va afisa "3", pentru ca "$LINE" va fi inlocuita de valoarea ei. 

> Pur si simplu. 

> Deci variabilele de mediu va vor permite sa configurati scripturile "shell", 

> bocalsi ma* tarzii^sf configurati "makefile"-uri, pentru a putea avea comportamente diferite in functie de variabilele de mediu.
