### [Assignment](https://youtu.be/RzTDMUt3mgo) ###

---

> Buna ziua. In acest video vom discuta despre cum declaram si cum asignam valori pointerilor.

> Am pregatit o functie "main" cu un exemplu, dupa cum puteti vedea, si cateva functii despre care vom vorbi mai tarziu.

> Si va voi explica cum declaram un pointer catre un "int".

> Pentru ca un pointer trebuie sa "pointeze" (arate) catre ceva.

> Si trebuie sa-i spunem tipul catre care va pointa.

> Suna putin complicat, dar e destul de simplu.

> Asadar, as vrea sa fac un pointer la un int.

> Pentru asta scriem "int", si apoi, legat de variabila...

> (dupa standardul folosit de noi; am putea sa punem * si in stanga, dar standardul aplicat ne impune asta)

> Deci scriind aceasta linie am declarat "ptr" care e un pointer catre "int".

> inseamna ca e pointer, si pointeaza catre ceea ce se afla in stanga, si anume un "int".

> Acum, as vrea sa iau adresa variabilei "a" si sa o stochez in "ptr".

> Pentru ca dupa cum v-am spus mai inainte, un pointer contine o adresa.

> Si acesta va contine adresa unui "int".

> Inainte declarati "a = 3" (a ia valoarea 3).

> Acum voi scrie "ptr = ...".

> Si in cazul de fata vom folosi caracterul ampersand (&) pentru a putea recupera adresa unei variabile in C.

> Si asa recuperez adresa lui "a". Deci scriu "&a;", si am scris ca "ptr" e egal cu adresa lui "a".

> Deci "ptr" va contine adresa lui "a".

> Cam totul are o adresa in C.

> Si va voi dovedi asta imediat.

> Vom afisa asta pe ecran.

> Voi afisa valoarea lui "ptr", am facut o functie pentru asta.

> Afisam valoarea...

> Vedem adresa lui "a".

> Observam ca nu este valoarea variabilei "a", este adresa ei.

> Putem de exemplu modifica valoarea variabilei "a", a = 42.

> Daca apoi afisez iar adresa lui "a", va fi neschimbata.

> Voi repune in "ptr" adresa lui "a", si vedem ca nu s-a schimbat.

> "a" e un spatiu in memorie, chiar daca-l modific adresa nu se modifica.

> Dupa cum vedeti am de doua ori acelasi lucru.

> Deci, am vazut ca putem pune adresa unui "int" intr-un pointer catre "int".

> Acum voi incerca sa fac o eroare.

> Voi declara o variabila de tip "char" si ii voi da o valoare (c = 'b').

> Voi incerca sa stochez adresa variabilei "c" in pointerul "ptr".

> Ce se va intampla?

> Avem o eroare: "assignement from incompatible pointer type".

> Aceasta eroare inseamna ca incerc sa stochez adresa unei variabile de tip "char" intr-un pointer la "int".

> Aceasta operatiune nu este posibila.

> Ce ar trebui sa fac? Ar trebui sa am un pointer la "char" in loc de pointer la "int".

> Acum "ptr" a devenit pointer catre "char".

> Recompilez... Si functioneaza.

> Am vazut cum putem dereferentia o variabila, adica cum putem recupera adresa unei variabile si cum o putem asigna unui pointer.

> In videoclipul urmator vom vedea cum putem utiliza acest pointer ca sa accesam variabila.
