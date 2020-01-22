> Vom vedea acum cum putem inlantui aceste comenzi.

> Pentru asta vom vedea cateva noțiuni.

> Ce putem deja retine e ca comenzile pe care le-am văzut pana acum sunt foarte unitare

> Putem afișa un fișier, putem sa recuperam primele 10 linii (sau primele "n"), sau ultimele "n", si putem filtra.

> Dar nu putem sa facem aceste operațiuni legate intre ele.

> Al doilea lucru pe care-l putem observa, e ca totul se afiseaza pe ieșirea standard, deci in principiu ecranul.

> Daca reluam exemplul de mai devreme, daca fac un "cat" pe fișier, conținutul va fi afișat pe ecranul nostru.

> Dar mai exista un comportament al tuturor acestor comenzi, e comportamentul fara fișier.

> Daca de exemplu tastez doar "cat", "cat” va aștepta sa-i dam informații pe intrarea standard.

> Va aștepta sa tastez ceva ce va înlocui apoi conținutul fișierului.

> Daca tastez "bonjour", o data ce apaș Enter imi va reafisa "bonjour".

> In mare, tot ce va citi pe intrarea standard (tastatura), va reafisa pe ieșirea standard (ecranul).

> Pentru a ieși din modul citire e "Ctrl+D".

> Deocamdată nu e foarte interesant, dar vom vedea cum sa redirectionam aceste ieșiri si intrări standard,

> Deocamdată nu e foarte interesant, dar vom vedea cum sa redirectionam aceste ieșiri si intrări standard,

> ceea ce va va permite sa inlantuiti comenzile.

> Reluând exemplul de mai devreme, exemplul de baza cu 'echo "bonjour'", va afișa doar "bonjour" pe ieșirea standard.

> Daca vreau ca aceasta ieșire standard sa nu fie ecranul, ci un fișier, va trebui sa redirectionez ieșirea standard spre fișier.

> Pentru astafolosim caracterul ">" care va spune "in loc sa afișezi pe ecran, afiseaza in fișierul din parametru".

> Daca fac 'echo "bonjour" > output', nu se va intampla nimic pe ecran, in schimb daca ne uitam a fost creat fișierul "output”,

> si daca ne uitam in conținutul lui, exista "bonjour”.

> Deci redirectarea noastra a funcționat.

> In schimb daca reincep o a doua, a treia si a patra oara, si ma uit in fișier, avem doar un singur "bonjour".

> De ce? Pentru ca la fiecare redirectare, va șterge conținutul fișierului "output" si-l va inlocui cu noua ieșire.

> Acest comportament nu e neaparat ceea ce vreți sa vedeți, si de asta avem o dubla redirectare spre dreapta,

> care va permite, in loc sa inlocuiti conținutul fișierului, sa adaugati la sfârșitul fișierului ("append").

> Daca fac asta si afișez conținutul fișierului "output", avem al doilea "bonjour" care a fost pus la sfârșitul fișierului, si după primul "bonjour".

> Acestea sunt redirectarile drepte, redirectarile ieșirii standard.

> Putem redirecta intrarea standard de asemenea.

> Depi daca fac "cat", in loc sa scriu pe tastatura a-i da ceva de citit, pot redirectiona un fișier, pe intrarea lui standard.

> Deci ce va face aici? In loc sa citească pe tastatura, va citi din fișier.

> Deci de fapt aceasta sintaxa e echivalenta a celeilalte, doar ca nu lucrează la fel.

> Aici va deschide fișierul, aici va continua sa citească de pe intrarea standard, doar ca i-am "fentat" intrarea standard pentru a citi din fișier.

> Deci ce veți putea face cu asta?

> Vedeți de exemplul ca puteti folosi "cat", in loc de a afișa pe ieșirea standard, pentru a redirectionata spre altceva.

> Ce ar fi util ar fi sa puteti redirectiona spre alta comanda.

> Aici intervine simbolul

> Daca facem un "cat" si ca-l trimitem ("|", "pipe") spre 'grep "Mathieu'", ne va afișa doar liniile cu "Mathieu".

> Deci ce s-a întâmplat?

> Comanda "cafjn loc sa scrie pe ieșirea standard, va scrie in "pipe", si "grep", in loc sa citească pe intrarea standard, va citi in "pipe".

> Deci pana la urma e ca si cum "cat" ar scrie direct in intrarea standard a "grep",

> deci "grep" in loc sa pornească de la un fișier va porni de la rezultatul comenzii "cat".

> Aceste "pipe" se pot inlantui la infinit.

> Daca vreau sa recuperez doar prima linie, ajunge sa fac asta.

> Ieșirea standard a "grep", ceea ce avem aici, trece in "head", care ne va selecționa prima linie si avem deci rezultatul dorit.

> Aceste "pipe" sunt foarte practice in toata viata de programator,

> va permit cu aceste mici comenzi unitare sa faceți inlantuiri foarte lungi si foarte complicate care vor face exact ce vreți voi.

> Șî e ce va vom ruga sa faceți foarte des, ca sa ajungeți la rezultatele pe care vi le cerem in exercițiile acestei zile.