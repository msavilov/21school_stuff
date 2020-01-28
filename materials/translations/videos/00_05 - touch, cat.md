> Deci acum ca am văzut cum sa ne plimbam in sistemul de fișiere, si ce este un sistem de fișiere,

**датуте**

> sperând ca ati inteles bine, vom vedea cateva comenzi care va vor fi utile in piscina

> sperând ca ati înțeles bine, vom vedea cateva comenzi care va vor fi utile in piscina

> si de altfel, care va vor fi utile tot timpul.

> Prima e comanda "touch", care va permite sa creați un fișier,

> comanda "cat" care va permite sa vedeți ce e in fișier si vi-l afiseaza pe ecran,

> comanda "cp" care copiaza, "mv" care muta,

> "rm", pe care am vazut-o deja impreuna, si va permite sa stergeti,

> si "chmod" care va permite sa schimbați drepturile pe un fișier sau un director,

> lucru important, ca prietenii voștri sa nu se amuze stergandu-va fișierele de exemplu; știind ca oricum vor incerca.

> Deci, prima comanda: "touch".

> La fel, când nu stiti, tastati, vedeți ce se intampla, si daca sunteti șmecheri faceți "man touch",

> si asa stiti cu ce opțiuni o puteti utiliza.

> La fel: rezumatul, descrierea si opțiunile, si asa mai departe.

> Deci, "touch"... Fac "cd", sunt in directorul meu, fac "ls”, bine, creez un director.

> Directorul e creat aici.

> Intru in el.

> Si aici scriu "touch" si imi creez fișierul.

> Asa, deci am fișierul meu caruia pot sa-i spun oricum.

> O mica precizare: daca scrieți asta, nu da același rezultat.

> Va las sa va dati seama singuri ce s-a intamplat, nu va explic.

> Si după ce facem curățenie, la fel, cu comanda "rm", si aici iarasi va arat ceva si va las sa va dati seama singuri ce face.

> Atentie: a se folosi cu precauție!

> Asa, deci am directorul meu.

> drwxr-xr-x* 41 boc al staff 1394 Jul 1 17:91 ..

Ibacal9"ac6 M) ~/Kr*a*tbaaa-fl

Am văzut "touch". Acum ca am văzut cum creem fișiere, ne vom uita ce e inauntru fișierului.


> Pentru asta exista comanda "cat".

> Nu va arat manualul de fiecare data, cred ca ati înțeles logica.

> Deci daca fac "cat" pe un fișier .c, sau de orice alt fișier, ce e in fișier va aparea pe ecran.

> Atentie, merge cu orice; cu fișierele de tip text, si de asemenea cu fișierele binare.

> Vom vedea mai târziu; veți avea surprize, nu va da același rezultat.

> Deci știu crea un fișier, știu sa ma uit in el, acum vom invata sa copiem fișierul.

> Ma intorc in super directorul meu unde nu e nimic, fac un "touch".

> Vom schimba, ceva mai original de data asta.

> Fac un "ls", si vad fișierul meu.

> Acum, am greșit si am creat fișierul in directorul "Krpestbeau", dar voiam sa-l pun in directorul meu "home".

> In cazul asta, folosesc comanda "cp", care copiaza, pun fișierul sursa, sursa a ceea ce vreau sa copiez, si destinația.

> De cele mai multe ori sub Unix ordinea e sursa, apoi destinație.

> Si deci directorul părinte.

> Daca fac asta, mal am inca fișierul acoJo unde ma aflu, si daca fac "cd pentru a urca in directorul de deasupra,

> si fac un "ls", vad fișierul "30_1estgentir care a fost copiat.

> Si, bineînțeles, daca șterg fișierul "30_1estgentil", si ma intorc in "Krpestbeau", il am inca aici (pentru ca a fost copiat).

> Mai departe: l-am copiat, dar voiam sa-l mut (m-am încurcat prima data, nu sunt prea talentat).

> Imi zic, de data asta chiar il voi deplasa: deci exista o comanda care se numește "mv".

> Toate comenzile in Unix, ca regula generala, au o logica.

> "cp" - copiez, "mv" - "move", "ls" - listez, si asa mai departe.

> Deci "mv", sursa, si destinația.

> Acum daca fac "ls", nu mai e aici, "30_1estgentil” a plecat, si e aici.

> In plus veți vedea ce data e aici, deci ca a fost mutat acum.

> Asa, deci știu deplasa, știu copia, știu șterge (asa, deci a dispărut), ne mai ramane un lucru de văzut, "chmod".

> "chmod”, cum indica si numele, schimba "modul", schimba drepturile pentru a fi mai exact.

> Revin in directorul meu.

> Un mic sfat, Unix e "case sensitive", bănuiesc ca stiati, dar in caz ca nu,

> asta inseamna ca daca puneți o majuscula in numele fișierului vostru, tine cont de majuscula.

> Puteti avea doua fișiere cu același nume, unul cu majuscule, unul cu litere mici, nu e același fișier.


> Deci "chmod", fac un "touch", asa, mi-am creat fișierul.

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
