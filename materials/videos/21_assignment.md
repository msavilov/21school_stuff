### [Assignment](https://youtu.be/RzTDMUt3mgo) ###

---
В этом видео я научу вас, как объявить и назначить указатель на что-то.
> Buna ziua. In acest video vom discuta despre cum declaram si cum asignam valori pointerilor.

> Hello. In this video I will teach you how to declare and assign a pointer to something.

Как вы можете видеть, мы подготовили функцию "main" в роли примера, и некоторые другие функции, о которых мы поговорим позже.
> Am pregatit o functie "main" cu un exemplu, dupa cum puteti vedea, si cateva functii despre care vom vorbi mai tarziu.

> We have prepared a "main" function with an example, as you can see, and some functions that we will talk about later.

Теперь я объясню вам, как мы объявлять указатель на "int."
> Si va voi explica cum declaram un pointer catre un "int".

> And I'll explain how we declare a pointer to an " int."

Потому что указатель должен «указывать» на что-то.
> Pentru ca un pointer trebuie sa "pointeze" (arate) catre ceva.

> Because a pointer has to" point " to something.

И мы должны сказать ему тип, на который он укажет.
> Si trebuie sa-i spunem tipul catre care va pointa.

> And we have to tell him the type he will point to.

translateme
> Suna putin complicat, dar e destul de simplu.

> Sounds a bit complicated, but it's pretty simple.

translateme
> Asadar, as vrea sa fac un pointer la un int.

> So, I'd like to do a pointer to an int.

translateme
> Pentru asta scriem "int", si apoi, legat de variabila...

> For this we write "int", and then, related to the variable...

translateme
> (dupa standardul folosit de noi; am putea sa punem * si in stanga, dar standardul aplicat ne impune asta)
> (according to the standard used by us; we could put * and left, but the standard applied imposes this)
> (according to the standard used by us; we could put * and to the left, but the applied standard imposes this on us)

translateme
> Deci scriind aceasta linie am declarat "ptr" care e un pointer catre "int".

translateme
> inseamna ca e pointer, si pointeaza catre ceea ce se afla in stanga, si anume un "int".

translateme
> Acum, as vrea sa iau adresa variabilei "a" si sa o stochez in "ptr".

translateme
> Pentru ca dupa cum v-am spus mai inainte, un pointer contine o adresa.

translateme
> Si acesta va contine adresa unui "int".

translateme
> Inainte declarati "a = 3" (a ia valoarea 3).

translateme
> Acum voi scrie "ptr = ...".

translateme
> Si in cazul de fata vom folosi caracterul ampersand (&) pentru a putea recupera adresa unei variabile in C.

translateme
> Si asa recuperez adresa lui "a". Deci scriu "&a;", si am scris ca "ptr" e egal cu adresa lui "a".

translateme
> Deci "ptr" va contine adresa lui "a".

translateme
> Cam totul are o adresa in C.

translateme
> Si va voi dovedi asta imediat.

translateme
> Vom afisa asta pe ecran.

translateme
> Voi afisa valoarea lui "ptr", am facut o functie pentru asta.

translateme
> Afisam valoarea...

translateme
> Vedem adresa lui "a".

translateme
> Observam ca nu este valoarea variabilei "a", este adresa ei.

translateme
> Putem de exemplu modifica valoarea variabilei "a", a = 42.

translateme
> Daca apoi afisez iar adresa lui "a", va fi neschimbata.

translateme
> Voi repune in "ptr" adresa lui "a", si vedem ca nu s-a schimbat.

translateme
> "a" e un spatiu in memorie, chiar daca-l modific adresa nu se modifica.

translateme
> Dupa cum vedeti am de doua ori acelasi lucru.

translateme
> Deci, am vazut ca putem pune adresa unui "int" intr-un pointer catre "int".

translateme
> Acum voi incerca sa fac o eroare.

translateme
> Voi declara o variabila de tip "char" si ii voi da o valoare (c = 'b').

translateme
> Voi incerca sa stochez adresa variabilei "c" in pointerul "ptr".

translateme
> Ce se va intampla?

translateme
> Avem o eroare: "assignement from incompatible pointer type".

translateme
> Aceasta eroare inseamna ca incerc sa stochez adresa unei variabile de tip "char" intr-un pointer la "int".

translateme
> Aceasta operatiune nu este posibila.

translateme
> Ce ar trebui sa fac? Ar trebui sa am un pointer la "char" in loc de pointer la "int".

translateme
> Acum "ptr" a devenit pointer catre "char".

translateme
> Recompilez... Si functioneaza.

translateme
> Am vazut cum putem dereferentia o variabila, adica cum putem recupera adresa unei variabile si cum o putem asigna unui pointer.

translateme
> In videoclipul urmator vom vedea cum putem utiliza acest pointer ca sa accesam variabila.


Hello in this video I'm going to teach you how to declare and assign pointer to something.

So I prepared my main screen,  as you can see on the screen I also prepared a couple of functions  which we'll talk about later.

I'm going to explain you how to declare a pointer to int because the pointer must point to something and you have to tell it what kind of thing it should point to.

It's easier then it seems you'll see.  So I want to do a pointer to an int. it's quite simple just type int and then stick to  your variable. 

We could put the star on the left to but to respect our schools Norm we have to put it  on the right.

See what I just did I've declared my pointer PTR to int. 

The star means it's a pointer,  it's points to  whatever is on the left,  in this case an int.

Now I want to take "a"  address  and put it in "PTR".  As I said earlier a pointer contains an address.  Here  it contains an int  address. So before  when you want to declare and to set "a = 3" (a is variable 3)  you type (a = 3). 

Now I'm going to declare PTR = &...  Is equal to something,  and we are going need the ampersand sign to retrieve  the address off something.

Here I want to retrieve "a" adress. So ptr = &a, so here