> Buna ziua. In acest video vom vorbi despre sirurile de caractere. 

> Inca de la inceput, am putut vedea ce este un caracter. 

> Reluam un exemplu simplu de functie "main". 

> Declaram o variabila "c" de tip "char" care ia valoarea caracterului ASCII 

> Daca fac "putchar(c)" ar trebui sa afis '*' pe ecran. 

> Compilam, executam... 

> Intr-unul dintre videourile precedente m-am incurcat si am folosit ghilimele. 

> Si ghilimelele sunt folosite pentru definirea sirurilor de caractere. 

> e sunt sirurile de caractere? 

> Sirurile de caractere sunt o multime de bytes situati unul langa altul, care fiecare contin cate un caracter. 

> Ultima valoare dintr-un sir ar trebui sa fîe caracterul ASCII *\0' sau valoarea numerica 0 (sunt echivalente). 

> Pentru ca fiecare caracter ASCII are un cod numeric unic asociat. 

> Acest caracter defineste deci sfarsitul sirului. 

> Cum putem folosi asta? 

> E simplu. Cand scrieti, de exemplu, "toto", va fi inlocuit cu adresa primului element al sirului "toto". 

> Deci adresa lui "t". 

> Atentie... Vorbim despre adrese, deci despre pointeri, deci probabil va spuneti ca vom avea cu siguranta nevoie de un pointer. 

> O sa-l numim "str" de data asta... De fapt nu, il voi numi tot "ptr", ca sa vedeti ca e acelasi lucru, folosim tot pointeri. 

> Si aici voi scrie intr-un mod diferit de cum am scris inainte... 

> Desi... pana la urma il scriu totusi mai jos, in modul standard. 

> ptr = "toto"; 

> Am facut un abuz de limbaj, pentru ca abia v-am spus ca "toto" e un sir de bytes care se termina prin '\0', si ca modul de scriere "toto" va returna adresa primului caracter. 

> "ptr" nu poate contine altceva decat o adresa. 

> Asta e un punct foarte important. 

> Pentru restul videoului, de acum incolo, vom vorbi despre siruri de caractere, dar amintrti-va ca atunci cand spunem pointer catre un sir de caractere, de fapt vorbim de un pointer catre un "char",  pointer catre primul element din sir, si speram ca atunci cand parcurgem sirul prin aritmetica de pointeri la sfarsit vom gasi un ’\0' care ne va spune sa ne oprim. 

> Cand scriem asta compilatorul pune in memorie "toto", deci caracterele 't', 'o', deci le va pune in memorie si va va returna adresa primului 't' din "toto". 

> Ca demonstratie, daca aici afisez "*ptr", deci elementul pointat de catre "ptr", in mod normal ar trebui sa afisez un ’t'. Si chiar l-am afisat. 

> Dupa cum va amintiti v-am spus ca putem scrie si altfel, vom utiliza in continuare apelul folosind paranteze patrate. 

> Si ar trebui sa faca acelasi lucru, fac asta doar ca sa va reimprospatez memoria. Deci afisez tot 't'. 

> Daca vreau sa ma deplasez in sirul de caractere "toto"... 

> Mai tineti minte ce v-am spus mai devreme? V-am spus ca alocati 10 elemente pe stiva cu acel tablou, deci pentru a accesa ultimul element folositi indexul 9. 

> Deci cate elemente am alocat pentru "toto"? Am alocat... nu 4 cum va spuneti toti, ci 5, pentru ca dupa cum v-am spus la sfarsit e un 'XO’. 

> Deci am 5 elemente pe stiva, dar ’\0* e un caracter special care ne permite sa stim cand sa nu mai avansam in memorie pentru ca am terminat de citit sirul. 

> Deci cand creati manual siruri de caractere trebuie sa le terminati pintr-un '\0', daca nu, toate programele care vor citi siruri de caractere vor continua sa citeasca pana la primul '\0’, si riscati sa crape. 

> Si nu e bine sa crape programele... 

> "ptr[1]" e primul 'o’, "ptr[2]" al doilea 't', si "ptr[3]" e ultimul 'o'. 

> Deci il vom afisa. 

> Cool. Am afisat ultimul ’o'. 

> Daca acum caut "ptr[4]" (pentru ca avem 5 elemente in stiva), veti vedea ca nu afiseaza nimic. 

> Voi folosi acum "cat -e". 

> Si "cat -e" imi va face sa apara caracterele "non-afisabile", si ceea ce vedeti aici e un '\0'. 

> Deci e un sfarsit de sir de caractere. 

> Deci acum am afisat sfarsitul sirului de caractere "toto". 

> Ceva foarte important de stiut: cand scrieti asta, "toto" v-a dat o adresa. 

> Dar "toto" e intr-o parte a memoriei unde nu aveti voie sa scrieti. 

> Daca acum vreau sa transform "toto" in "poto", deci: ptr[O] = 'p'; (si nu sirul de caractere "p", nu e acelasi lucru) veti vedea ca in mod normal (si pentru asta reafisez "ptr[O]"), sau nici macar nu va compila,  sau programul va crapa. 

> Si in cazul de fata a crapat cu eroarea "bus error". 

> E exact ce voiam sa va arat. "toto" e intr-o zona in care nu avem dreptul sa scriem. 

> Singura modalitate prin care as putea scrie in "toto", e daca as fi declarat un tablou, fara marime, si as fi pus sirul de caractere in el. 

> O data ce ati scris asta, compilatorul stie ca ati vrut sa alocati un tablou, si sa puneti "toto" in el. 

> Va va aloca 5 elemente, 't', 'o', 't', 'o', '\0', dupa cum va amintiti. 

> deci 5 elemente, si va pune adresa lor pe stiva, in "ptr", si "ptr" va fi un pointer catre acest lucru. 

> Daca acum fac acelasi lucru... sa incercam... fac acelasi lucru si de data asta a mers, si am 'p' ca prim caracter al sirului. 

> Asta pare amuzant deocamdata, dar mai e ceva ce vreau sa va arat, ca sa fie totul clar. 

> Acum 30 de secunde eram pe "char *ptr", si: ptr = "toto"; 

> Aici eram. Ce se intampla daca iau un al doilea "char "ptr2", si voi scrie: ptr2 = "lol"; 

> Si acum scriu "ptr = ptr2 

> Ce se intampla cand caut "ptr[O]"? 

> Pai, daca urmarim logica, "ptr2" ia adresa primului T din "lol". 

> "ptr" ia adresa primului ’t’ din "toto". 

> Acum cand scriu "ptr = ptr2;", in dreapta am un pointer catre "char", in stanga am un pointer catre "char", am

> dreptul sa scriu asta. 

> Deci ce e "ptr2"? E doar o adresa. "ptr" e si el o adresa. 

> Deci acum am suprascris adresa din "ptr" cu adresa din "ptr2". 

> Si acum "ptr" pointeaza catre 'l'-ul din "lol". 

> Deci daca execut asta (si daca nu am gresit nimic), voi afisa un T. 

> Am facut turul sirurilor de caractere; amintiti-va deci ca sirurile sunt caractere (bytes) unele dupa altele, care se termina printr-un ’\0*. 