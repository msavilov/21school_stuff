> Am ajuns acum la partea bonus a zilei. 

> Aceasta parte nu e obligatorie pentru a face exercitiile zilei, 

> în schimb va va fi foarte utila in viata voastra de programator, si chiar si pentru resl 

> Mai devreme vorbeam de iesirea standard. 

> Daca luam exemplul nostru: daca execut "cat" pe fisier, a mers, totul a functionat corect si totul e afisat pe iesirea standard. 

> In schimb daca-i cer sa afiseze ceva ce nu exista, imi va da un mesaj pe iesirea de eroare. Deci... 

> Cum putem vedea asta? Daca fac "cat" pe fisierul si fac "pipe" prin "rev", vom vedea ca fisierul e inversat. 

> Inseamna ca continutul fisierului a fost scris in iesirea standard, si "pipe" a trimis iesirea standard ca intrare standard pe "rev", si "rev" si-a facut treaba.

> In schimb daca acum dau un fisier care nu exista, 

> "cat" va afisa eroarea pe iesirea de eroare, si "rev" nu va citi aceasta iesire de eroare, pentru ca citeste doar intrarea/iesirea standard, si nu va inversa linia de eroare. 

> Aceasta poate sa fie sau nu interesant: puteti sa vreti sa inversati si aceasta iesire de eroare. 

> Cum facem asta? 

> Cu niste redirectari suplimentare. 

> Daca vrem sa redirectam tot ce e pe iesirea de eroare, si sa tratam rezultatul ca si cum ar fi iesirea standard, vom face asta: "2>&1 

> Deci "2" va corespunde iesirii de eroare, "1" va corespunda iesirii standard,

> si asa ii spunem ca tot ce vine pe iesirea de eroare va fi tratat ca si cum ar fi pe iesirea standard. 

> Daca acum facem "| rev", vom vedea ca mesajul a fost inversat cu succes, pentru ca a fost tratat ca si cum ar fi fost o iesire standard.

> In mod similar a ceea ce am avut inainte, putem redirecta tot ce e "2", deci iesire de eroare, intr-un fisier.

> Daca fac asta, cer sa redirectionez "2" in "error", si apoi ma uit sa vad ce e in "error", vedem mesajul de eroare dinainte.

> Si daca-l facem de mai multe ori, 

> il avem o singura data pentru ca a fost suprascris. 

> Si avem redirectarea dubla, care va va permite sa adaugati mesajul la sfarsitul fisierului. 

> Acest lucru poate fi foarte util daca aveti o lista de fisiere, 

> si aveti erori in ele, 

> si vreti sa recuperati doar partea care a mers sau partea care nu a mers, etc. 

> Cu aceste redirectari veti putea sa aveti de exemplu toate fisierele care au dat erori in fisierul "error".

> Alt lucru care va va fi foarte util e un fisier special (care nu e chiar un fisier), "/dev/null". 

> In mare tot ce e scris spre "/dev/null" va fi pur si simplu sters, "uitat". 

> Deci aici nu se va intampla nimic, fisierul "/dev/null" nu exista cu adevarat, deci rezultatul nu va fi adaugat in el. 

> La ce poate folosi? La a sterge o parte din rezultat, pentru a pastra de exemplu doar mesajele de eroare. 

> Daca vrem sa avem toate mesajele de eroare, acum e cam dezordine, trebuie urcat ca sa le vedem. 

> Daca-i spunem ca tot ce a functionat sa fie trimis spre "/dev/null", nu mai apar decat mesajele de eroare. 

> Inca o data, acest lucru poate fi foarte util pentru face debug, sau pentru a verifica daca scripturile functioneaza corect, e ceva foarte important de stiut in continuare.


