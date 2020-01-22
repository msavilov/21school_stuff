> Acum ca ati citit cu totii documentia, cel putin sper ca ati facut-o, vom putea intra in subiect.
Теперь, когда вы все прочитали документацию, по крайней мере, я надеюсь, что вы это сделали, мы сможем перейти к этой теме.

> Inainte de asta, doua-trei mici chestiuni.
А перед этим, еще пара вещей.

> In primul rand, sunt mai multe moduri de a folosi GIT.
Во-первых, есть несколько способов использования GIT.

> Cum ati vazut in documentatie, putem de exemplu sa cream un repository in local pe statia de lucru, putem sa copiem un repository de pe statia de lucru a unui coleg, putem clona un repository de pe propria statie de lucru, sau sa clonam unul de pe un server central, iar apoi sa trimitem acolo modificarile.
Как вы уже видели в документации, мы можем, например, создать локальный репозиторий на Mac, можем скопировать репозиторий с компьютера друзей, я могу клонировать локально репозиторий с моего компьютера или мы можем клонировать репозиторий с главного сервера, а затем отправить изменения туда.

> lar noi asta vom face.
И этим мы сейчас и займемся.

translateme
> Exista un server, numit Vogsphere, care se va ocupa sa creeze pentru voi cate un repository in momentul in care va inscrieti pentru un proiect, si care va va comunica adresa acestuia prin intermediul intranetului.
There is a server, called Vogsphere, that will create a repository for you when you sign up for a project, and that will communicate your address via the intranet.

Этот главный сервер называется "Vogsphere", который автоматически будет создавать репозиторий для вас, когда вы будете регистрироваться на проект, адрес на этот репозиторий будет виден в intranet'e.

> Voi veti merge pe intranet si veti recupera adresa, veti clona acel repository, veti lucra cu el, iar apoi veti trimite modificarile spre Vogsphere.
Вы просто берете и заходите в intranet, получаете адрес, клонируете этот репозиторий, а потом отправляете изменения в "Vogsphere".

> Vom vedea detaliile mai tarziu.
Более подробно мы разберем это позже.

> De asemenea, vorbind de adresa (URL), veti vedea ca eu voi folosi o adresa care pare inventata.
Also, speaking of the address (URL), you will see that I will use an address that seems invented.

Также, говоря об адресе (URL), который я буду использовать в видео, если вам покажется он придуманным,

> Dar nu e asa, va asigur, doar ca eu cunosc deja adresa, iar voi nu o veti stii si veti merge in intranet pentru a recupera adresa repository-ului vostru de fiecare data cand veti avea un nou proiect.

но это не так, уверяю вас, просто я уже знаю адрес, а вы нет и будете заходить в интранет для получения вашего адреса вашего репозитория каждый раз, когда у вас будет новый проект.


> Acum trecem la terminal si incepem cu inceputul, dica “git clone".
Now we go to the terminal and start with the beginning, say "git clone".
Теперь мы заходим в терминал и начнем все с начала, напишем "git clone".

> Pentru “git clone” trebuie sa precizam serverul de unde vrem sa recuperam repozitory-ul, aici “vogsphere@vogsphere.42.fr”, urmat de (doua puncte) si numele repository-ului, asa cum il primiti pe intranet Inca o data, pare inventat, dar nu e, voi il veti vedea pe intranet.
Для использования команды "git clone" нам нужно указать сервер, на котором находится наш репозиторий, здесь это "vogsphere@vogsphere.42.fr", затем две точки (:) и имя (путь) репозитория, который вы должны получить в intranet.


> In orice caz, are mereu aceeasi forma: cod modul / anul scolar / cod instanta / activitate / login-ul sefului grupului.
In any case, it always has the same form: module code / school year / instance code / activity / login of the group leader.

В любом случае, он всегда имеет одну и ту же форму: код модуля / учебный год / код деятельности / код логина лидера группы.

> Seful unui grup format dintr-o pesona este evident acea persoana.

Будучи в группе 1, логично подумать, что я и есть лидер своей собственной группы.

> La final obsevat ca tastez “jOO”, pentru a face clona in dosarul local “jOO”, altfel, clona se va face in dosarul personal, lucru care nu este elegant, iar de indata ce voi incerca sa fac o clona, git nu va suprascrie clona anterioara ci va da mesajul ca nu se poate face pentru ca acea clona exista deja.

Заметьте, что в конце я пишу "j00", чтобы сделать клон в локальной папке "j00", если этого не сделать, то клон папки будет сделан в домашнем каталоге, и это мягко говоря "неоч", т.к. как только я попытаюсь сделать клон, git не перезапишет предыдущий клон, а выдаст сообщение, по типу "вы не можете этого сделать, потому что этот клон уже существует".

> Ca atare, puneti intotdeauna un nume de dosar pentru clona la final.
Поэтому, всегда именуйте клонируемый репозиторий.

> De asemenea, pentru a va ajuta sa castigati timp, va arat si niste scurtaturi care simplifica viata.
Чтобы помочь вам сэкономить время, я покажу вам несколько сокращений, которые упростят вашу жизнь.

> Partea de inceput, inainte de cele doua puncte, nu e obligatoriu sa fie scrisa complet, ci puteti folosi “vogsphere.42.fr:...” sau chiar “vgs.42.fr:...”, alt nume scurt pentru Vogsphere.
Во-первых, необязательно писать полностью адрес перед двумя точками (:) "vogsphere.42.fr:...", достаточно написать альтернативный сокращенный адрес "vgs.42.fr:..." для Vogsphere.

> Sau puteti face ca mine, care sunt foarte foarte comod: "vgs:...".
Или вы можете делать, как я, т.к. я очень ленивый: "vgs:..."

> Asta merge foarte bine si asa voi face in aceasta demonstratie.
Мне это сокращение очень подходит и пожалуй я им воспользуюсь для демонстрации.

> Daca voi veti intampina vreo problema cu asta, utilizati forma completa.
Если у вас возникнут проблемы с этим, то используйте полный путь.

> Acum voi face “git clone” si dupa cum vedeti primim o multime de mesaje.
Теперь я воспользуюсь командой "git clone", и как вы можете видеть я получаю очень много сообщений в процессе.

> Nu va ingrijorati, nu sunt mesaje de eroare.
Не переживайте, это не ошибки.

> Atata timp cat nu apare termenul “error” nu este vorba de o eroare.
До тех пор, пока "error" не появится, ошибок там не будет.

> In acest caz, ceea ce imi spune este data la care a inceput operatiunea, si anume ora 17:33 din data 26 iunie 2013.
В данном случае, что он мне показывает, так это дату начала операции, а именно 17:33 26 июня 2013 года.

> Asta va va folosi mai tarziu, dupa cum vom vedea la finalul acestui exemplu.
Мы воспользуемся этим позже, я объясню вам это сразу же, как закончу с примером.


> In orice caz, nu va alarmati, este perfect normal.
В любом случае, не паникуйте, это нормально.

> Acum pot intra in dosarul “jOO” care va fi dosarul meu de lucru, adica este copia locala a repository-ului.
Теперь я перейду в папку "j00", чтобы начать работу со своими файлами, то есть копией локального репозитория.

> Voi face modificari in dosar, de exemplu voi crea un fisier “test.c”, in care voi scrie o functie "main()", care nu face nimic, dar nu e important acum.
Я создам файл, например, "test.c", в котором запишу функцию "main()", которая ничего не делает, но сейчас это не важно.

> II salvez si pentru ca “git” sa-l ia in considerare, trebuie sa-i spunem ca suntem interesati de acest fisier.
Мы сохраним его, и чтобы "git" считал его, мы должны сказать ему, что мы заинтересованы в этом файле.

> Putem verifica cu “git status” pentru a vedea ca in acest moment nu va face nimic daca lansez un “commit”.
Мы можем проверить командой "git status", чтобы увидеть, какие файлы были взяты во внимание. Если я напишу "commit", git ничего не сделает.

> Imi spune ca exista un fisier “test.c”, dar care nu este luat in considerare (“untracked”) pentru moment de “git”.
"git status" говорит мне, что есть файл "test.c", но он не учитывается ("непроиндексирован") для "git" в данный момент.

> Pentru a-l lua in considerare, tastez “git add test.c”.
Чтобы проиндексировать этот файл, введите "git add test.c".

> Putem vedea cu “git status” acum ca, fisierul este in lista de modificari ce vor fi incluse in commit-ul urmator.
Теперь мы можем увидеть в "git status", что этот файл находится в списке изменений, которые будут включены в следующий "commit".

> Pot face un “git commit”.
Теперь я воспользуюсь командой "git commit"

> Parametrul “-m” imi permite sa precizez un mesaj de commit direct in linia de comanda.
с параметром "-m", который позволяет указать "commit"у сообщение, которое я пропишу в коммандой строке.

> Nu sunt obligat sa-l folosesc, dar eu o fac pentru ca nu am chef sa folosesc editorul pentru asta.
I dont have the right one, but I'am going to do it right now, because I'am too lazy to open a header.

> Asadar, “git commit” imi reia mesajul “Creation de test.c”, si a facut un commit cu crearea fisierului de test.
Итак, «git commit» резюмирует мое сообщение «Creation de test.c» и создает "commit" с созданием test.c файла.

> Daca verificam acum cu “git status” putem vedea ca acum nu mai este nimic pregatit pentru un nou commit.
Если мы проверим сейчас «git status», то увидим, что сейчас нет файлов, которые можно за"commit"тить.

> Pot face alte modificari, de exemplu pot schimba fisierul “test.c” pentru a adauga un “ft_putchar(‘f)”, inainte de “return”, iar acum imi spune ca, desi e vorba de un fisier care e luat in considerare, este o modificare ce nu este pregatita pentru “commit”.
Я могу внести некоторые изменения, например я хочу изменить файл «test.c», чтобы добавить туда «ft_putchar()» перед «return»,и теперь он говорит мне, что этот файл непроиндексирован и является модификацией (он изменен), которая не готова для "commit"а.

> Asta pentru ca, de fiecare data cand facem o modificare, trebuie sa-i spunem explicit ca ne intereseaza.
Каждый раз, когда вы делаете изменения, вы должны сказать git'у, какие файлы вы хотите проиндексировать.

> Tastez “git add test.c” si apoi refac un “git commit” cu mesajul de rigoare.
Введите «git add test.c» и затем напишите «git commit» с соответствующим сообщением.

> Mesajele de commit pe care le folosesc aici sunt desigur reduse, dar voi in proiectele reale ar trebui sa puneti mesaje mai lungi si semnificative pentru a va orienta mai usor in istoric.
commit сообщение, которые я здесь напишу, конечно, сокращено, но в реальных проектах вы должны писать более развернутые и более значимые сообщения, чтобы вам было легче ориентироваться в истории commit'ов.

> Asadar, am facut mai multe commit-uri, ceea ce e foarte dragut, dar acum, trebuie sa le propagam spre serverul distant.
Итак, мы сделали несколько коммитов, что очень хорошо и теперь мы должны отправить их на удаленный сервер.

> Pentru moment, commit-urile sunt doar la mine in local, iar Vogsphere nu le cunoaste absolut deloc.
На данный момент, коммиты являются локальными, и Vogsphere о них не знает.

translateme
> Pentru a face asta, asa cum ati vazut in documentatie, utilizam “git push” pentru a trimite modificarile spre serverul distant.
To do this, as you saw in the documentation, we use "git push" to send the changes to the remote server.

Как мы уже знаем, чтобы отправить изменения на удаленный сервер, мы используем команду "git push".


> Vom putea folosi mai tarziu “git pull” pentru a recupera modificari de pe serverul distant.

Позже у нас будет возможность использовать "git pull", чтобы получить изменения с удаленного сервера.

translateme
> Acum facem un “git push”.

translateme
> Daca fac operatia acum imediat, nu va functiona, pentru un motiv foarte simplu, si anume ca la primul “push” trebuie sa precizam, care e destinatia, aici “origin”, si care e branch-ul pe care vrem sa il trimitem, aici “master”.

translateme
> Daca nu intelegeti nu e foarte grav, trebuie doar sa stiti ca pentru primul “push” trebuie folositi “git push origin master”, iar in continuare doar “git push”.

translateme
> Mesajul primit imi spune ca am trimis un nou brach “master” in repository.

translateme
> Inca ceva important: opreratia “git push” nu se face doar o data si gata, ci puteti face “push” de cate ori doriti, nu este nici o problema.

translateme
> De exemplu pot sa creez un fisier “text.txt” cu un continut oarecare, pot sa-l adaug la un commit, sa fac commit-ul si apoi sa refac un “git push”.

translateme
> De data aceasta nu mai e nevoie sa precizez “origin master”, iar git trimite fisierele mele spre Vogsphere.

translateme
> Acestea fiind zise, s-ar putea sa aveti indoieli despre succesul operatiei “git push”.

translateme
> Pentru a verifica ce s-a trimis, e suficient sa faceti o noua clona a repository-ului cu “git clone”, doar ca in loc sa folosim numele “jOO”, folosim de exemplu “jOO-verif’.

translateme
> Mergeti apoi in noua clona, si tot ce gasiti aici este exact ceea ce se gaseste pe serverul Vogsphere.

translateme
> Continutul va fi de altfel ceea ce va gasi corectorul, fie el uman sau automat, pentru notare.

translateme
> Insist pe acest lucru: doar ceea ce se gaseste pe Vogsphere va fi corectat.

translateme
> Orice altceva, daca ati uitat sa trimiteti spre server, nu conteaza, nu va fi notat.

translateme
> Fiti foarte atenti la acest lucru.

translateme
> Am terminat cu asta, am facut multe operatii pentru a explica lucruri foarte simple.

translateme
> Acum voi reface un mic exemplu succint, pentru a putea vedea fara complicatii parazite cum functioneaza sistemul.

translateme
> Reiau de la inceput.

translateme
> Prima data folosim “git clone”.

translateme
> Clonam deci repository-ul de pe Vogsphere, specificand destinatia clonei, aici “jOO”.

translateme
> Intru in dosar, voi face niste operatii, voi crea un fisier “tata.txt” in care scriu “toto".

translateme
> Adaug fisierul cu “git add”, facem commit pentru a crea o versiune revizuita cu “git commit”, cu mesaje care ar fi bine sa fie mai explicite decat in acest exemplu, iar apoi impingem (“push”) modificarile spre server cu “git push”.

translateme
> O data ce am facut asta, e gata, modificarea pe care am facut-o e inregistrata pe serverul Vogsphere.

translateme
> lar daca vreau sa verific acest lucru, pot sa fac o noua clona “jOO-verif’, cum fac aici, si sa intru in dosar pentru e vedea ca regasesc tot continutul.

translateme
> Folosind “cat tata.txt” vad ca regasesc ce am scris in fisier.

translateme
> Nu este nici o problema, totul este in repository, deci am trimis corect spre server modificarile.

translateme
> Acestea fiind zise, inca doua-trei informatii destul de importante.

translateme
> In primul rand, asa cum am precizat mai inainte, corectorul automat, si nu doar el, ci si corectorul uman, nu va lua in considerare decat ceea ce gaseste pe Vogsphere.

translateme
> Daca vreodata veti spune ca ati utiat sa trimiteti anumite modificari pe server, nu se va lua in considerare.

translateme
> Nu se admite nici o scuza, se corecteaza doar ceea ce este pe server.

translateme
> O repet de multe ori si stiu ca devine obositor, dar e foarte foarte important.

translateme
> E esential sa nu suferiti din cauza unei astfel de erori.

translateme
> De asemenea, cand veti lucra in grup, (eu am facut exemplul singur si asta e foarte usor), dar in grup va veti lovi de problema sincronizarii versiunilor intre membrii grupului.

translateme
> Asta se rezolva foarte simplu cu ajutorul comenzii “git pull”, despre care nu va voi spune acum mai multe pentru ca o gasiti in documentatie ca sa stiti cum se foloseste.

translateme
> In al doilea rand, serverul Vogsphere are limitare la dimesniunea fiecarui repository, limita fiind de 100MB.

translateme
> In mod normal nu ar trebui nici macar sa va apropiati de aceasta limita, dar daca veti incepe sa puneti multe lucruri in repository, aveti grija sa nu depasiti limita, deoarece a trece de 100MB e considerat o utilizare abuziva a resurselor, iar astfel de abuzuri se sanctioneaza destul de sever, asa ca va recomand sa nu ajungeti in astfel de situatii.

translateme
> Sa continuam.

translateme
> Ati putut observa mai devreme ca atunci cand am utilizat “git clone”, (refac operatia ca sa vedeti mai bine), am un mesaj care imi spune ca operatia a inceput la o anumita data.

translateme
> Acesta precizeaza data pe care serverul o ia in considerare pentru a determina daca mai aveti sau nu dreptul de a scrie in repository.

translateme
> Fiecare proiect are data limita de predare, iar din momentul expirarii acestui termen, cu precizie de secunda, nu veti mai avea dreptul sa faceti “push” cu nimic spre repository-ul proiectului.

translateme
> Aceasta data e folosita ca garantie, in cazul in care va conectati la server pentru a face “push” cu doar cateva secunde inainte de expirarea termenului, si pentru a sti ca operatia a inceput de exemplu la ora 23, 41 de minute si 50 de secunde.

translateme
> Deci, chiar daca operatiunea dureaza foarte mult (de exemplu daca ceilalti 1000 de colegi ai vostri se conecteaza pentru a face “push” in acelasi timp, putin probabil, dar chiar si in acest caz), ora care determina daca aveti acces este cea de inceput, adica ora din mesaj.

translateme
> Ca atare, chiar daca operatia “push” dureaza 5 minute si se termina la ora 23 si 46 de minute, in timp ce ora limita este 23 si 42 de minute, nu e grav, pentru ca a inceput inainte de ora limita.

translateme
> Ceea ce conteaza este sa nu intrerupeti conexiunea.

translateme
> Daca intrerupeti cu “ctrl-C” si vreti sa reluati, poate ca ora limita a trecut deja si veti fi blocati.

translateme
> De asemenea, veti observa poate, daca sunt multe conexiuni in acelasi timp, ca veti avea un mesaj cum ca sunteti in coada de astepare dupa ce lansati comanda.

translateme
> Din nou, nu e grav, dar sa nu intrerupeti conexiunea.

translateme
> Serverul va spune ca e suprasolicitat si ca trebuie sa asteptati.

translateme
> Veti fi informati periodic cu numarul de persoane din fata voastra in coada.

translateme
> Inca o data, nu va alarmati, e perfect normal, trebuie sa asteptati.

translateme
> Inca doua-trei informatii de final.

translateme
> Identificarea pe server se face cu ceea ce numim ticket “Kerberos".

translateme
> II primiti in mod automat cand va conectati pe statia voastra de lucru.

translateme
> Dar, asa cum va veti da seama la un moment dat, ticketele Kerberos expira, deci trebuie reinnoite din cand in cand.

translateme
> Daca vreti sa verificati ca aveti un ticket Kerberos valid, puteti folosi comanda “klist”, care va lista ticketele voastre.

translateme
> De exemplu eu am aici un ticket Kerberos care expria in 27 iunie 2013 la ora 3 dimineata.

translateme
> II voi distruge in mod intentionat pentru a vedea ce se intampla daca nu-l avem.

translateme
> Execut “kdestroy” si dupa cum vedeti nu mai am nici un ticket.

translateme
> Acum, daca incerc sa execut “git clone”, imi va da un mesaj de acces interzis (“permission denied”).

translateme
> Utilizez comanda “kinit” cu numele de utilzator si parola mea, pentru a obtine un ticket nou.

translateme
> Cu “klist” verifc faptul ca am un ticket, iar acum pot sa execut “git clone”, operatie care va functiona fara nici o problema.

translateme
> Asadar, daca va veti lovi de aceasta problema, veti sti ca solutia este “kinit”.

translateme
> O ultima informatie despre o operatie pe care nu ati vazut-o pentru ca am facut-o inainte, dar pe care va trebui sa o faceti cand incepeti sa lucrati pe statia voastra de lucru.

translateme
> Cand veti incerca sa faceti un “commit”, “git” va va atentiona ca nu cunoaste numele si nici mail-ul vostru, si veti vedea un mesaj foarte lung de eroare pentru a va configura accesul la “git”.

translateme
> Este foarte simplu, trebuie lansate doua comenzi, pe care “git” vi le indica.

translateme
> Ca atare, nu va impacientati cand veti vedea mesajul, nu ati stricat nimic.

translateme
> Faceti ceea ce va indica, completand numele si email-ul, si “git” va fi multumit.

translateme
> Am facut practic turul complet al cunostintelor necesare pentru a folosi serverul Vogsphere, iar eu va recomand inca o data sa mergeti sa cititi documentaia de pe “git-scm.com”, pentru ca “git” e un sistem foarte evoluat care ofera mult mai multe posibilitati decat extrem de simplul exemplu pe care vi l-am prezentat azi.

translateme
> Ce am aratat eu este esentialul necesar pentru a va putea preda proiectele, dar se pot face lucruri mult mai geniale cu “git” daca stiti sa-l folositi, incat ar fi pacat sa nu va documentati despre asta si sa nu utilizati toate posibilitatile acestui minunat program.

translateme
> Ajunge cu propaganda pentru “git”, va doresc o zi buna si pe curand!