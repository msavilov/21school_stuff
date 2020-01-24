> Buna ziua, in acest video vom vedea cum putem dereferentia un pointer: cum putem accesa valoarea

> variabilei spre care pointeaza. 

> lata funcția "main" utilizata si in videoclipul anterior. 

> Avem o variabila "a" de tip "int" si un pointer "ptr" carea pointeaza spre un "int". 

> După cum am văzut mai devrem am pus in "a" valoarea 3.

> Pointerul "ptr" pointeaza spre adresa variabilei "a", cum am văzut inainte. 

> Acum vreau sa accesez valoarea variabilei spre care pointeaza "ptr". 

> E destul de simplu, trebuie doar scris "*ptr". 

> Daca vreți sa va amintiți, "ptr" e un pointer spre "int", deci "*ptr" este un "int". 

> Chiar e atat de simplu. 

> Asta e tot ce trebuie sa va amintiți ca sa nu aveți probleme cu pointerii. 

> Folosesc funcția "ft_putnbr" care-mi permite sa afișez un număr, si deci daca o apelez asa...

> Vedeți ca primește ca parametru un "int", deci as avea eroare daca nu ii dau un "int". 

> In cazul de fata "*ptr" e un "int", pentru ca ”*ptr" inseamna ca ma voi uita la adresa pointata de "ptr". 

> Compilez.. 

> Execut si obțin valoarea 3. 

> Acum, ca sa va dovedesc ca intr-adevar căutăm valoarea lui "a", 

> voi afișa o data "a", apoi ii voi schimba valoarea. li dau acum valoarea 42, afișez si un "\n" sa fie mai clar, si reafisez valoarea din "*ptr",

> si veți vedea... Avem o eroare... 

> ghilimelele duble ("). 

> Trebuie sa folosim ’ in loc de " atunci când avem un singur un caracter. Vom vedea in alt video la ce folosesc

> ghilimelele duble ("). 

> Acum reexecut, si prima data afișez 3, apoi afișez 42. 

> Deci am reușit sa vad valoarea. 

> Dar pot de asemenea modifica direct valoarea. 

> Deci daca fac "*ptr = 42;", si afișez valoarea lui "a", reîncep, recompilez... si am același lucru. 

> Deci când scriu "*ptr" aici ce se intampla? 

> Prima acțiune, "ptr" este o adresa, deci cu "*ptr" voi vedea ce e la aceasta adresa, 

> si apoi pun valoarea 42 la adresa la care ma găsesc.

> Deocamdată e destul de simplu. 

> Complicam puțin lucrurile, veți vedea ca putem avea pointeri către pointeri. 

> Deci "ptr2" este un pointer la pointer la "int".

> Deci "ptr2" pointeaza spre adresa unui pointer la "int". 

> Lui "ptr2" ii voi asigna adresa unui pointer către "int", deci adresa pointerului "ptr", nu adresa lui "a". 

> Acum fac același lucru, dar adaug o noua steluta *... 

> Si aici. Si vom avea același rezultat. 

> Pentru ca "ptr2" conține adresa "ptr". Când fac "*ptr2" obțin un pointer către "int". Acum adaug o noua steluta; deci prima data ma duc sa vad ce e in adresa pointata de "ptr2".

> In cazul de fata e o noua adresa, si cu a doua * merg cu un rang mai departe, 

> si ajung la variabila "a". 

> Si acum pot sa o afișez. 

> Deci ”**ptr2" e un "int", deci toate operațiunile acestea vor funcționa. 

> Sa vedem daca merge. 

> In mod normal... merge. 

> Doar pentru amuzamentul vostru va voi arata un exemplu pe care il am pregătit. 

> Putem face asta la infinit. 

> Deci am "ptr", "ptr2", "ptr3", etc., si am pointer către pointer către pointer, etc. 

> Cred ca ati înțeles logica: "ptr" e un pointer către "int", deci pointeaza către "a", 

> "ptr2" e un pointer către pointer către "int", etc. 

> Afișez valoarea lui "a" trecând prin "ptr7", pointer către pointer către... Multi pointeri. 

> Si voi afișa valoarea lui "a".

> Vom vedea daca merge. In mod normal, da.

> Daca totul e ok.

> M-am încurcat... Reincerc, o sa reusesc pana la urma. 

> Am compilat "main2.c". 

> Se afiseaza valoarea 3, deci prin "ptr7", la care am ajuns prin multi pointeri, am putut afișa valoarea lui "a". 

> Ati invatat cum sa dereferentiati pointerii si cum sa va jucati cu ei,

> in videoul următor vom vedea aritmetica cu pointeri.
