> Buna ziua din nou. 

> Vom termina ziua despre pointeri cu aspecte legate de utilizarea lor. 

> Pentru ca pana acum ne-am jucat cu pointerii in interiorul unei functii "main" si probabil ca inca nu vedeti adevarata miza. 

> Veti incepe sa intelegeti miza in continuare, de indata ce veti putea aloca memorie. 

> Pana acum am utilizat stiva de memorie, de fiecare data aveam variabile numite "a”, "b", etc., recuperam adresa lor, cunoasteam in mare zona de memorie in care erau salvate. 

> In curand o sa vedeti ca putem aloca memorie, fara sa stim in ce zona de memorie este facuta alocarea si aici vor interveni pointerii. 

> lata un exemplu simplu de utilizare a pointerilor care ne va fi util astazi. 

> Avem o functie "main" si o functie "fct". 

> In functia "main" am declarat o variabila "a" de tip "int" si i-am dat valoarea 42. 

> Apoi am apelat functia "fct" cu parametrul 

> In functia "main", voi afisa apoi valoarea "a" si un retur la linie ('\n').

> Functia "fct" ia un parametru de tip "int" pe care l-am numit tot "a" (ca sa va incurc), si ii da valoarea 12. 

> Dupa parerea voastra ce se va afisa pe ecran: 12 sau 42? 

> Cel mai bun mod... Nu puteti sa "stricati" calculatorul, deci nu ezitati sa testati. 

> Se afîseaza 42.. 

> Voi reveni in cod. Afisam 42... Uitati-va aici: variabila "a" din functia "main" are valoarea 42. 

> Atunci cand apelam o functie, transmitem parametri prin copiere. Deci nu am transmis "a”, ci o copie a valorii lui "a". 

> Parametrul "a" din functia "fct" e o copie a celui din "main", deci doar primeste valoarea 42. 

> Cand modific "a"-ul de aici, dandu-i valoarea 12, e vorba de "a"-ul din functie. 

> Dar "a"-ul din "main" nu s-a schimbat. 

> Inca o data, nu am transmis "a"-ul din main, am trasmis o copie a valorii lui. 

> Cum facem ca sa modificam valoarea variabilei "a" din functia "main" folosind functia "fct"? 

> In loc sa transmitem valoarea lui "a", vom transmite adresa lui "a". 

> Si aici, functia "fct" va primi ca parametru un pointer la "int" in loc de un simplu "int". 


> devenit pointer catre "int", si daca vreau sa modici valoarea "a"-ului din functie, trebuie sa-l dereferentiez aici. 

> Daca ati urmarim videoclipurile anterioare de astazi, ar trebui sa fie clar. 

> Apelez functia "fct" transmitand o copie a adresei lui "a" printr-un pointer la "int" (caruia ii spun tot "a", ca sa va incurc). 

> Am facut astfel incat la adresa spre care pointeaza pointerul "a" sa salvam valoarea 12. 

> Sa vedem ce obtinem... 

> Acum avem valoarea 12. 

> Putem folosi un pointer fie pentru a ne deplasa intr-un tablou sau intr-un sir de caractere (care e un tablou de "char"), 

> fie pentru a transmite adresa unei variabile si a o modifica intr-o functie. 

> Aceasta din urma este una dintre formele cele mai frecvent utilizate pentru pointeri. 

> Concluzionam aici cursul de pointeri de astazi. 

> Daca aveti neclaritati, nu ezitati sa urmariti din nou toate cursurile de astazi, dar mai ales, nu ezitati sa incercati voi insiva. 

> Sa nu va fie frica de faptul ca ati putea strica computerul. Si analizati atent mesajele de eroare. Compilatorul a fost facut sa va ajute. 

> Va urez o zi buna si mult curaj.