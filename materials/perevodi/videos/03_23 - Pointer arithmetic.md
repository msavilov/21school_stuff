> Buna ziua. In acest video vom vorbi despre aritmetica pointerilor. 

> Sper sa va concentrati pentru ca este momentul in care in general lumea se pierde. 

> Sunt lucruri destul de simple, dar in mod ciudat lumea are probleme cu aceste notiuni... 

> lata o functie "main" pregatita in avans. 

> Variabilele "a" si ”b" sunt de tip "int" cu valori asignate. 

> Am folosit functiile definite mai sus pentru a afisa adresa variabilei "a", valoarea lui "a", adresa lui "b", valoarea lui "b". 

> Sa vedem rezultatul. 

> Execut... 

> Compilez... 

> Execut... 

> Observam ca "a" si "b" au aproape aceeasi adresa, doar ca adresa lui "a" este la 4 bytes departare de "b". 

> Este normal, am vorbit anterior despre stiva ("stack"). Cand declarati ceva pe stiva (care e in capatul superior al adreselor), adresele scad in valoare. 

> Deci diferenta intre "a" si "b" e de 4 pentru ca tipul "int" ocupa 4 bytes. 

> lata asadar explicatia pentru care adresa lui "a" este cu 4 bytes mai mare decat adresa lui "b". 

> Acum voi putea utiliza pointerii pentru a ma deplasa 

> Deci voi face un pointer: 

> Si voi face ca in "ptr" sa am adresa lui "b

> Daca vreau sa reproduc ce aveam inainte, ar trebui sa pun, in locul adresei lui "a", ("ptr" este adresa lui "b") deci adresa lui "a" ar trebui sa fie ptr+4. 

> Dar compilatorul e mai destept, stie ca "ptr" este un pointer la "int", si va multiplica valoarea pe care o aditionati cu dimensiunea tipului (aici "int"). 

> Pentru ca e logic ca vreti sa va mutati din "int" in "int". 

> Deci ca sa ajung de la "b" la "a", trebuie sa scriu ptr+1. 

> Aici afisam valoarea lui "a". 

> Mai devreme am folosit * pentru a afisa o valoare. 

> Deci "*ptr" ar trebui sa afiseze valoarea lui "b". 

> In schimb nimic nu imi interzice sa scriu *(ptr+1). 

> Deci iau adresa din "ptr", fac +1, si compilatorul stie ca sunt intr-un pointer catre "int", deci aduna 4 bytes, si * va spune "vezi ce e la adresa asta". 

> Deci in mod logic aici afisez adresa si valoarea lui 

> Deci voi afisa 3, chiar daca aici "ptr" pointa catre "b". 

> Recompilez... 

> Daca comparati cu executia anterioara a programului veti vedea ca am afisat adresa lui "a". 

> E o mica diferenta, e ciudat... 

> De fapt e pentru ca am recompilat programul si reexecutat programul, dar e ok... 

> Important e ca sunt pe "a", chiar daca am pornit cu adresa lui "b". 

> De fiecare data cand relansez programul adresele se pot schimba, dar asta e o alta poveste. 

> Vom vedea ca daca avem variabile de tip "char", unele lucruri se vor schimba. 

> Sa folosim variabilele "a" si "b" de tip "char", si pointerul "*ptr" la "char" (in loc de "int"). 

> Voi schimba aici, pentru ca nu mai pot pune numarul 3, voi pune caracterul ASCII 3 (doar ca sa va incurc putin...). 

> Voi pune caracterul ASCII 'o' in "b". 

> Si aici in loc de "ft_putnbr" folosim "ft_putchar" care afiseaza un character. 

> Deci acum am "a" care contine valoarea ASCII '3', "b" care contine 'o', "ptr" care pointeaza catre "b", ptr+1 va contine adresa lui "b" plus 1, pentru ca tipul "char" are dimensiunea de 1 byte (deci ne deplasam din byte in byte). 

> De altfel voi adauga o linie in plus: voi afisa adresa lui "b", iar apoi restul. 

> Recompilam si executam... 

> Observati ca diferenta dintre adresa lui "b" si adresa lui "a" este 1, pentru ca acum lucrez pe "char". 

> Putem face asta cu orice tip de variabile. 

> Si de fiecare data compilatorul cunoaste marimea variabilei catre care pointati, deci se va deplasa in mod corect. 

> Ultimul punct, doar pentru a ne amuza.. 

> Voi reveni rapid la variabile de tip "int". 

> Voi repune "int"-uri si ne vom distra doua secunde... In fine, pe mine ma distreaza... 

> Voi pune a=1 si b=42. 

> Vom pastra... inclusiv afisajul adresei lui "b". 

> Si aici voi pune ptr+a. 

> Si la fel aici pun plus "a". 

> Pentru ca putem face suma dintre un pointer si un "int", e ca si cum as pune 1, 

> 1 e o variabila statica, ce nu va misca, ”a" chiar e o variabila, dar nu conteaza. 

> Deci cand fac asta ce se intampla? Afisez adresa lui "b", adresa lui "a"... 

> Si... am uitat sa schimb "putchar" in "putnbr". 

> Deci iata ca am afîsat 1, care e valoarea lui "a". 

> Plecand de la "ptr" care pointeaza catre "b". 

> Am facut turul aritmeticii de pointeri, nu e mai complicata de-atat, trebuie sa va amintiti ca puteti face calcule cu o adresa, si apoi folosi * pentru a vedea ce e la noua adresa.
