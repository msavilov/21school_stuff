> Buna ziua tuturor. Pentru început, astazi vom vedea shell-ul.

> Deci ce este shell-ul? In bara de taskuri de jos aveți un element numit iTerm.

> Acesta va va deschide un terminal.

> O data ce sunteti in terminal, vom incepe cu ceva foarte simplu: daca vreți sa iesiti, scrieți "exit".

> Aceasta comanda paraseste terminalul.

> Pentru a redeschide un terminal, aveți iarasi bara de jos, si, la fel, terminalul.

> II vom pune in fullscreen, va fi mai simplu.

> La ce folosește un terminal? La a rula comenzi si la a vedea rezultatul comenzilor.

> Pana aici e destul de simplu.

> Avem un sistem de fișiere Unix. (Suntem in MacOs, dar ramane un sistem de fișiere Unix.)

> Acest sistem de fișiere e organizat cam ca si in Windows, cu managerul de fișiere, doar ca aici lucram in consola.

> Pentru a începe: foarte simplu, o comanda de baza: "pwd".

> Aceasta comanda va da ca rezultat directorul curent in care va găsiți.

> E important, va permite sa va plimbați printre directoare, pentru ca aici nu suntem intr-o interfața grafica.

> O data ce stiti unde sunteti, puteti folosi alta comanda, care se numește "ls".

> E cam echivalentul comandei "dir", pentru cei care cunosc comenzile Windows.

> Acest "ls" listează fișierele si directoarele din locul in care va aflati.

> Nu afiseaza fișierele ascunse; vom reveni la asta ceva mai târziu.

> înainte de toate, comanda cea mai importanta pe care trebuie sa o cunoașteți e "man", m-a-n.

> Daca tastati doar "man", va va intreba ce pagina de manual vreți.

> Deci "man" inseamna "manual", si pentru toate comenzile care exista (absolut toate), e referința voastra.

> Când nu stiti ceva, tastati "man" si numele comenzii, "man", spațiu, "ls".

> Aici va explica ls ("list directory contents ), si aveți rezumatul comandei: opțiunile, cum se folosește, si descrierea tuturor opțiunilor.

> Va las sa le cititi, va va amuza... sau nu.

> In orice caz, înainte de a întreba pe cineva cum funcționează o comanda, încercați "man".

> Si pentru cei care vor sa se amuze, exista "man man": asta va explica cum funcționează "man" (cu opțiuni).

> Deci amintiti-va, tastati "man" când nu stiti ceva, toate răspunsurile sunt acolo.

> Deci stiti sa faceți "ls" (care va listează fișierele).

> Va dau doar o mica opțiune, "ls -I": va afiseaza si detaliile.

> Printre aceste detalii găsiți, in stanga, drepturile fișierelor (revenim mai târziu la ele)... sau directoarelor...

> Grupul, in cazul de fata "staff”; utilizatorul, "bocal"; timestampurile...

> Si cel mai la dreapta, numele directorului sau fișierului.

> A doua opțiune: tot "I", si "a", care va permite sa afișați fișierele ascunse, daca exista.

> Deci tot ce vedeți cu punct in fata, e un fișier ascuns.

> Puteti intra in ele, la fel, daca faceți "cd" va puteti deplasa: ".ssh", de exemplu, si Enter.

> Daca nu stiti unde sunteti, "pwd". Si puteti iar executa "ls -I" si va da ce e in ".ssh".

> Pentru a reveni inapoi faceți "cd ("change directory"). Si ati revenit inapoi.

> De altfel, vedeți ca daca faceți "ls -la", primele in lista sunt "." si ".."

> Punctul e directorul curent, cele doua puncte reprezintă directorul imediat dinainte.

> O data ce stiti face asta, exista inca o comanda, de fapt doua-trei pe care le vom vedea împreuna.

> Deci ce face "mkdir"? Daca nu știm, tastam comanda, si va da utilizarea ei.

> Si la fel, daca nu va ajunge, faceți "man mkdir", si aveți detaliul.

> Va previn in schimb ca sunt comenzi care se executa fara opțiuni, deci daca le tastati doar ca s^ testati, uneori veți avea surprize.

> Va sfătuiesc sa cititi manualul înainte sa utilizați comenzile.

> Deci sa ne imaginam, sunt in directorul meu, vreau sa ajung in ziua 0; sunt in ziua 0.

> Vreau sa creez un director cu loginul meu.

> Voi face un "mkdir", spațiu, numele directorului.

> "ls", si vad directorul meu, numit "krp"; e un "d" pentru "director" la început,

> drepturile fișierului, utilizatorul, grupul, si data la care l-am creat.

> Pot sa merg in el: daca fac "ls -la" nu e nimic decât(directorul curent), si (directorul precedent).

> Daca fac "cd Enter, vad ca 'Vkrp" a dispărut si sunt in ziua 00.

> "pwd", si afișez "/Users/bocal/jOO".

> Deci astea sunt comandele de baza, pentru a va deplasa de la un director la altul,

> a crea un director, pentru a afla unde sunteti, si stiti ca trebuie sa folosiți "man".

> Veți vedea des ca asistenții, când ii veți intreba ceva, va vor întreba daca ati citit manualul.

> Daca nu ati facut-o, evitati sa intrebati.

> O mica comanda care poate fi utila: "rm".

> Deci "rm", va previn, poate strica lucruri, "rm" șterge.

> Deci tot "man rm", daca vrem sa ne documentam, poate fi folositor.

> Aveți diversele opțiuni.

> Si glumele pe care vi le vor face prietenii: marele "rm -Rf' (recursiv, si care nu cere confirmare),

> șterge tot, plecând de unde sunteti, inclusiv toate subdirectoarele.

> Deci va previn de-acum contra șmecherilor care va vor spune sa executați asta.

> Acum, imi vad directorul "krp", daca fac "rm krp" nu va merge.

> Si nu merge, pentru ca e un director. Si daca cititi manualul, veți intelege de ce.

> Deci "rm -rf krp", Enter, "ls", si "krp" nu mai exista, a fost sters.

> Nu cautati "unrm", sau "undelete", sau cine știe ce altceva, sau unde e coșul de gunoi, nu merge.

> Nu mai exista, si gata.

> Asta e tot pentru azi, vom reveni mai târziu la cum sa ne deplasam pe discurile din rețea, ce sunt ele,

> ce e un link simbolic, si alte lucruri de genul asta care va vor fi utile.