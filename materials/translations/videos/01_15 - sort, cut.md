> Acum ca am vazut cum functioneaza redirectarile, vom putea folosi acest sistem pentru a continua sa manipulam fisierele. 

> Vom vedea о comanda foarte simpla care e "sort". 

> Cum indica si numele, va va permite sa sortati ce ii dati ca parametri, deci ce ii dati sa citeasca de pe intrarea standard in cazul nostru.

> Aici vedem ca a sortat in ordine alfabetica toti utilizatorii.

> Atentie, e о sortare lexicografica, deci bazata pe codul ASCII al caracterelor, deci majusculele sunt inaintea literelor mici.

> Pentru a nu avea acest comportament exista optiuni, alte optiuni pentru a sorta numerele, optiuni pentru a sorta invers. 

> Va las sa cititi "man sort"; ca toate comenzile are multe optiuni. 

> О data sortata iesirea, veti putea de exemplu sa recuperati doar prenumele. 

> Pentru asta exista comanda "cut", care va va permite sa taiati fiecare linie in functie de un delimitator. 

> Keiexemplu daca fac "cut" cu optiunea "jd" pentru delimitator sivoi putea recupera campurile care ma intereseaza. 

> Daca vreau numai primul camp adaug optiunea "-f 1" si recuper doar primele campuri. 

> Revenind la ce am spus mai devreme, adaug optiunea "cat -e" pentru a afisa caracterele non-afisabile, 

> si voi vedea ca aici e un spatiu dupa "maxime", ceea ce nu puteam vedea fara "cat -e". 

> Comanda "cat" e foarte puternica, va permite sa faceti tot felul de lucruri; veti putea de exemplu recupera mai multe campuri, sau о дата de campuri.

> Va fi foarte practic pentru a recupera doar informatiile care va intereseaza 

> din fisiere de genul acesta care sunt separate prin niste delimitatori, 

> fie prin virgula, fie prin punct si virgula, etc. 

> О data се ati reusit sa vedeti asta, 

> (sa zicem pastrand doar prenumele) vom putea modifies aceste prenume.

> De exemplu daca vreau sa schimb 

> sa zicem "thomas" in "Thomas" (cu majuscula), voi putea folosi comanda "sed". 

> Comanda "sed" e о comanda foarte puternica, ce va permite sa modificati fluxul de date. 

> De exemplu ii vom cere sa schimbe "thomas" in "Thomas". 

> (cu un slash in plus...) 

> Si vedem aici ca "Thomas" incepe acum cu о majuscula. 

> In mare ce face? 

> Primul caractep fs"), spune ca facem о inlocuire, deci vom inlocui al doilea parametru cu cel de-al treilea parametru. 

> E foarte simplu. 

> Е о functionalitate simpla a comenzii "sed", in schimb putem face foarte multe cu aceasta comanda, ьо! deci va sfatuiQSc inca о data sa cititi manualul, sau sa va uitati si la exemple pe Internet, vor fi mai sem initiative.

> Puteti face multe modificari, sa modificati un element din doua, sa folositi expresii regulate, cu diverse modele, lucruri foarte complicate, care pot fi foarte puternice daca reusiti sa le stapaniti bine.

> Ultima comanda de modificare de fisiere pe care о vom vedea se numeste "tr". 

> De exemplu, vedem aici accentul in cuvantul "melanie". 

> Asa il inlocuiesc printr-un "e" normal. 

> tr" e simplu: ia doi parametri, un caracter pe care-l vom inlocui, si un al doilea cu care il vom inlocui. 

> De exemplu pot sa adaug un "X" pentru a schimba "x"-ul din "xavier" in majuscula. 

> Si va face schimbarea. 

> Toate aceste comenzi sunt foarte simple; inca о data: uitati-va la manuale, cautati pe internet, sunt foarte simplu de utilizat, trebuie doar experimentat putin la inceput pentru a vedea cum functioneaza.
