> Buna ziua. In acest video vom vorbi despre tablouri. 

> Mai devreme am vazut ca putem declara variabilele "a" si "b" pe stiva, 

> si ca ne putem plimba intre cele doua pentru ca sunt foarte aproape in stiva. 

> Acum as vrea sa am 10 valori "int". 

> In loc sa definesc 10 variabile de tip "int", voi declara o singura variabila care contine 10 valori de tip. Acesta este un tablou. 

> Luam niste cod pe care-l aveam dinainte. 

> Putem declara o variabila simpla de tip "int" scriind "int b;". 

> Acum voi scrie "tab", si veti vedea o noua modalitate de scriere: 

> cand scriu "int tab[10];", spun ca pe stiva vor exista 10 valori "int", iar "tab" va fi un pointer implicit spre prima dintre aceste valori "int". 

> Vorbim tot despre pointeri. 

> Aici, in "putaddr" de obicei pun o adresa, acum pun "tab". 

> Si aici daca vreau sa afisez o valoare din "tab" (desi deocamdata n-am inserat niciuna), voi utiliza iarasi"[]". 

> Pentru a accesa primul element, scriu "tab[O]". 

> Veti vedea imediat de ce scriu *'tab[O]". 

> Va arat prima data ca merge. 

> "tab[O]" are valoarea 42. 

> Compilez... 

> Execut... 

> Vedem ca "tab" e o adresa, si ca ”tab[O]" e 42. E ceea ce voiam. 

> Acum va voi explica de ce prima valoare din tablou este "tab[OJ". 

> Deocamdata nu e foarte clar... 

> Pentru ca "[0]" (de fapt a pune ceva intre paranteze patrate) e echivalent cu "*(tab + ce e intre paranteze) 

> Deci "tab[0]=42;" si "*(tab+0)=42;" e exact acelasi lucru. 

> Si va voi demonstra asta. 

> Recompilez... 

> Reexecut... 

> Am tot valoarea 42. 

> Asta pentru ca "tab" este un pointer spre primul element dintr-un tabou de "int". 

> Deci cand scriu +0, e adresa primului element. 

> Deci cand scriu *(tab+O) ajung pe un "int” care e primul element al tabelului. 

> Deci "tab[OJ" e acelasi lucru cu ce am scris mai sus. 

> Daca vreau sa accesez al patrulea element din tablou, voi scrie *(tab+3). 

> Operatia +3 (din cauza ca folosim ”int"-uri) inseamna de fapt in memorie +12. Deci +3*4 bytes. 

> Pentru ca tipul "int" ocupa 4 bytes. 

> Deci reincep, dupa ce am pus "[3]" mai jos, si "+3" mai sus, si tot merge. 

> Deci am un spatiu de memorie de 10 elemente. 

> Daca primul element din tablou are indexul 0, atunci ultimul element are indexul 9, si nu indexul 10, va rog sa fiti atenti. 

> Pentru a accesa ultimul element din tablou, indexul lui e dat de lungimea tabloului minus 1. 

> Pentru ca accesam primul element cu 0. 

> Acum ca am vazut asta va voi demonstra ca e un pointer. 

> Declaram un pointer "*ptr". 

> Si scriu "ptr = tab;", caci "tab" e o adresa. Sper ca va compila, pentru ca uneori pot fi probleme. 

> Compileaza fara erori. Revin in program. 

> "ptr" a luat valoarea lui "tab". "tab" dupa cum va amintiti e o adresa. 

> E adresa primului element al tabloului. 

> Deci daca scriu "*(ptr+3)"... "ptr+3" e o adresa, "*(ptr+3)" e un "int". 

> Si ii dau valoarea 867. 

> Si aici voi afisa tot "tab[3J". 

> Oare o sa mearga? 

> 867... Deci inca suntem ok. 

> Vedeti, tablourile sunt o maniera de a scrie mai simplu aritmetica pointerilor si ne permit sa declaram un numar de elemente. 

> Pentru a fi exhaustivi vom declara un tablou de intregi. 

> Si mai jos voi face un tablou... 

> Hai sa fim chiar completi. 

> II vom numi "tab2", tot cu 10 elemente. 

> Si lui ii spunem "tabptr" ca sa nu va incurcati, 

> si el are doua elemente, dar ce elemente? Pe stiva voi pune doi pointeri catre "int". 

> Este un tablou de pointeri spre "int". 

> Si putem face asta la infinit. 

> Sa modificam asta.. 

> Imaginati-va ca vreau sa modific "tab2" prin intermediul "tabptr". 

> Deci care e tipul lui "tabptrfOj"? Pointer catre "int". 

> Deci el va primi adresa unui "int", deci ii voi da valoarea lui "tab". 

> tabptr[1] = tab2; 

> Si acum vreau sa modific "tab2[3J" prin "tabptr" acum ca am legat "tabptr" la tablouri. 

> ar trebui sa mearga. 

> Pentru a vedea "tab2[3] , folosesc tabptr[1]" care e echivalent la "tab2", si acum adaug [3]", si daca pun 42

> ar trebui sa mearga. 

> Voi sterge afisarea adresei. Vom incerca.. 

> Deci dupa cum vedeti, in "tabptr[OJ" (care e un pointer catre "int") am pus valoarea lui "tab", in "tabptr[1]", "tab2". 

> Si retestam, deci prin "tabptr" am setat corect valoarea lui "tab2[3]" la 42. 

> Veti vedea ca e foarte logic ceea ce facem. 

> Cum putem face asta cu pointeri? (Cu asta terminam videoul.) 

> Cum scriem asta cu pointeri? 

> V-am spus ca daca punem ceva intre e ca si cum am scrie * elementul din stanga plus ce e intre paranteze. 

> Deci voi transforma "tabptr[1][3]" in ceva cu stelute. 

> Voi incepe prin a scapa de "[3]". 

> Deci "*(tabptr[1] + 3)", pentru ca "tabptr[1J" e elementul din stanga lui "[3]". 

> (tabptr[1] + 3) = 42; 

> Va rearat linia. In mod normal cele doua linii sunt echivalente. 

> Vom testa. 

> Ar trebui sa compileze... 

> Afisam tot 42. 

> Acum facem aceeasi operatie pentru "[1]". 

> Recompilez... Relansez... Afisam tot 42! 

> Deci linia de mai jos e echivalenta cu asta. 

> Deci la ce voiam sa ajung... Vedeti ca "tabptr" e un tablou de pointer catre "int". 

> Si "tab" e un tablou de "int", deci e un pointer catre "int". 

> Deci "tabptr" e un pointer de pointeri catre "int", 

> ceea ce se vede bine pentru ca pentru a accesa un "int", 

> (elementul la care ajung pana la urma e un "int" caruia pot sa-i dau valoarea 42) 

> trebuit sa folosesc doua stelute. 

> Prima data am adaugat 1 la adresa continuta in "tabptr", 

> deci 4 pentru ca un pointer e echivalent la 4 bytes... 

> de fapt chiar 8, pentru ca fiind pe 64 bits un pointer are 8 bytes, 

> am vazut ce se gaseste la aceasta adresa... 

> Si de fapt acolo se gaseste "tab2". 

> Deci am ajuns la "tab2". 

> Si la "tab2" am adaugat 3, si am cautat ce se afla la aceasta adresa, ca si cum as fi scris "tab2[3J", si i-am dat valoarea 42. 

> Am facut o trecere rapida prin tablouri. 

> Atentie, ultimul punct de care am uitat. 

> Atentie, daca scrieti asta: "int tab[10][10];", "tab" nu e un pointer de pointeri catre "int". 

> Si trebuie sa fiti foarte atenti la asta, pentru ca de fapt "tab" e un pointer catre "int". 

> Doar ca puteti sa-l accesati intr-o functie folosind cele doua paranteze patrate, 

> dar daca vreti sa-l dati unei alte functii veti avea probleme. 

> Deci va las pe voi sa va jucati cu tablourile de tablouri, 

> acum ca ati vazut ca putem avea tablouri de pointeri, tablouri simple, 

> deci tablouri de "int", de pointeri catre "int" si de pointeri catre pointeri catre "int".. 

> Va las deci pe voi sa va jucati cu ele.
