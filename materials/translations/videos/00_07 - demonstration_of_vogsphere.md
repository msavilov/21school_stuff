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

> Pentru a face asta, asa cum ati vazut in documentatie, utilizam “git push” pentru a trimite modificarile spre serverul distant.
Как мы уже знаем, чтобы отправить изменения на удаленный сервер, мы используем команду "git push".

> Vom putea folosi mai tarziu “git pull” pentru a recupera modificari de pe serverul distant.
Позже у нас будет возможность использовать "git pull", чтобы получить изменения с удаленного сервера.

> Acum facem un “git push”.
Теперь делаем "git push".

> Daca fac operatia acum imediat, nu va functiona, pentru un motiv foarte simplu, si anume ca la primul “push” trebuie sa precizam, care e destinatia, aici “origin”, si care e branch-ul pe care vrem sa il trimitem, aici “master”.
Если я прямо сейчас сделаю "git push", то ничего не сработает, по очень одной простой причине, при первом "push" нам нужно указать git'у место назначения, которым будет "origin", а также ветку "master", на которую мы хотим отправить

> Daca nu intelegeti nu e foarte grav, trebuie doar sa stiti ca pentru primul “push” trebuie folositi “git push origin master”, iar in continuare doar “git push”.
Не переживайте, если не поняли, просто запомните, что в первый раз мы пишем "git push origin master" и потом мы пишем только "git push"

> Mesajul primit imi spune ca am trimis un nou brach “master” in repository.
В сообщении, которое я получил, говорится, что я отправил в новую ветку "master" в моем репозитории, что есть хорошо.

> Inca ceva important: opreratia “git push” nu se face doar o data si gata, ci puteti face “push” de cate ori doriti, nu este nici o problema.
Еще один важный момент: использование команды "git push" не будет выполняться единожды, вы можете ее использоваться столько раз, сколько захотите.

> De exemplu pot sa creez un fisier “text.txt” cu un continut oarecare, pot sa-l adaug la un commit, sa fac commit-ul si apoi sa refac un “git push”.
К примеру, я могу создать файл "text.txt" с всякой херней внутри, я могу добавить его в "commit", выполнить "commit", а затем сделать "git push".

> De data aceasta nu mai e nevoie sa precizez “origin master”, iar git trimite fisierele mele spre Vogsphere.
На этот раз мне не надо указывать "origin master" и git отправит мои файлы на Vogsphere.

> Acestea fiind zise, s-ar putea sa aveti indoieli despre succesul operatiei “git push”.
Тем не менее, у вас могут быть сомнения в успехе выполнения команды "git push".

> Pentru a verifica ce s-a trimis, e suficient sa faceti o noua clona a repository-ului cu “git clone”, doar ca in loc sa folosim numele “jOO”, folosim de exemplu “jOO-verif’.
Чтобы проверить, что именно было отправлено на сервер, достаточно сделать новый клон репозитория с "git clone", просто, вместо имени "jOO" мы напишем, например, "jOO-verif".

> Mergeti apoi in noua clona, si tot ce gasiti aici este exact ceea ce se gaseste pe serverul Vogsphere.
Затем заходим в репозиторий, который мы склонировали, и все, что вы найдете там, будет находиться в репозитории на сервере Vogsphere.

> Continutul va fi de altfel ceea ce va gasi corectorul, fie el uman sau automat, pentru notare.
Содержимое вашего репозитория также может быть взято для проверки, не важно кто именно будет проверять, человек это или Moulinette.

> Insist pe acest lucru: doar ceea ce se gaseste pe Vogsphere va fi corectat.
Еще раз хочу подчеркнуть: проверенными будут только те файлы, которые будут находиться на Vogsphere, если там будет находиться что-то еще или вы забыли что-то загрузить, то проверять это не будут.

> Orice altceva, daca ati uitat sa trimiteti spre server, nu conteaza, nu va fi notat.

> Fiti foarte atenti la acest lucru.
Будьте аккуратнее с этим.

> Am terminat cu asta, am facut multe operatii pentru a explica lucruri foarte simple.
Теперь, когда со всем этим закончили, ощущение такое, что я рассусоливаю вам такие простые вещи, поэтому время для маленького примера, без пустой болтавни, чтобы показать, как все это работает.

> Acum voi reface un mic exemplu succint, pentru a putea vedea fara complicatii parazite cum functioneaza sistemul.

> Reiau de la inceput.
И так, начнем все сначала.

> Prima data folosim “git clone”.
Сперва делаем "git clone".

> Clonam deci repository-ul de pe Vogsphere, specificand destinatia clonei, aici “jOO”.
Итак, мы склонировали наш репозиторий с репозитория на Vogsphere, указав место назначения клона, тут это "jOO".

> Intru in dosar, voi face niste operatii, voi crea un fisier “tata.txt” in care scriu “toto".
Я захожу в эту новую папку, создаю там файлы.

> Adaug fisierul cu “git add”, facem commit pentru a crea o versiune revizuita cu “git commit”, cu mesaje care ar fi bine sa fie mai explicite decat in acest exemplu, iar apoi impingem (“push”) modificarile spre server cu “git push”.
Мы добавляем файлы через "git add", потом включаем их через "git commit", делаю commit файлов, чтобы создать новую версию с командой "git commit" с более развернутым сообщением, чем в моем примере, а затем мы делаем push на сервер, через команду "git push".

> O data ce am facut asta, e gata, modificarea pe care am facut-o e inregistrata pe serverul Vogsphere.
Теперь, после того, как я все это сделал, все мои изменения теперь будут в папке на сервере Vogsphere.

> lar daca vreau sa verific acest lucru, pot sa fac o noua clona “jOO-verif’, cum fac aici, si sa intru in dosar pentru e vedea ca regasesc tot continutul.
И если я захочу в этом убедиться, я могу сделать новый клон "j00-verif", такойже как и тут и зайти в него, чтобы проверить и убедиться, что все находится на своих местах.

> Folosind “cat tata.txt” vad ca regasesc ce am scris in fisier.
И через команду "cat tata.txt" увидеть, что текст находится там и все хорошо.

> Nu este nici o problema, totul este in repository, deci am trimis corect spre server modificarile.
Проблем никаких нет, все находится в репозитории, а значит я правильно отправил все изменения на сервер.

> Acestea fiind zise, inca doua-trei informatii destul de importante.
Еще немного важных моментов, о которых вам нужно знать.

> In primul rand, asa cum am precizat mai inainte, corectorul automat, si nu doar el, ci si corectorul uman, nu va lua in considerare decat ceea ce gaseste pe Vogsphere.
Во-первых, как я уже сказал, Moulinette и также ваш проверяющий, когда будут проверять, то будут учитывать только те файлы, которые будут находиться в репозитории на Vogsphere.

> Daca vreodata veti spune ca ati utiat sa trimiteti anumite modificari pe server, nu se va lua in considerare.
If you ever say that you failed to send certain changes to the server, it will not be considered.
И если вы скажете "даа, я забыл отправить это на сервер", то это трюк не сработает,

> Nu se admite nici o scuza, se corecteaza doar ceea ce este pe server.
никаких исключений, только то содержимое, которое находится в вашем репозитории на сервере будет проверено.

> O repet de multe ori si stiu ca devine obositor, dar e foarte foarte important.
Я знаю, что я часто повторяюсь и что вас это утомляет, но это очень, очень и очень важно.

> E esential sa nu suferiti din cauza unei astfel de erori.
Вы должны быть абсолютно уверены, что не допустите эту ошибку.

> De asemenea, cand veti lucra in grup, (eu am facut exemplul singur si asta e foarte usor), dar in grup va veti lovi de problema sincronizarii versiunilor intre membrii grupului.
Также, когда вы будете работать в группе, (тут я конечно делал все в одиночку и это прекрасно), но в группе вы столкнетесь с проблемой синхронизации версий между членами группы.

> Asta se rezolva foarte simplu cu ajutorul comenzii “git pull”, despre care nu va voi spune acum mai multe pentru ca o gasiti in documentatie ca sa stiti cum se foloseste.
Это все легко решить с командой "git pull" и больше я ничего не добавлю т.к. вам нужно самим прочесть документацию, если вы захотите узнать побольше об этом.

> In al doilea rand, serverul Vogsphere are limitare la dimesniunea fiecarui repository, limita fiind de 100MB.
Во-вторых, на сервере Vogsphere есть ограничение по допустимому размеру для всех репозиториев, ограничение составляет 100MB.

> In mod normal nu ar trebui nici macar sa va apropiati de aceasta limita, dar daca veti incepe sa puneti multe lucruri in repository, aveti grija sa nu depasiti limita, deoarece a trece de 100MB e considerat o utilizare abuziva a resurselor, iar astfel de abuzuri se sanctioneaza destul de sever, asa ca va recomand sa nu ajungeti in astfel de situatii.
Как правило, не стоит даже приближаться к этому лимиту, но если вы начинаете добавлять очень много вещей в репозиторий, то такие злоупотребления наказываются достаточно строго, поэтому я рекомендую вам не попадать в такие ситуации. Будьте осторожны и не превышайте лимит, так как превышение 100MB считается нецелевым использованием ресурсов.

> Sa continuam.
Продолжим.

> Ati putut observa mai devreme ca atunci cand am utilizat “git clone”, (refac operatia ca sa vedeti mai bine), am un mesaj care imi spune ca operatia a inceput la o anumita data.
Вы наверное уже заметили, что когда я использовал команду "git clone" (выполню ее еще раз, чтобы вы еще раз увидели), то я получаю сообщение о том, что операция началась в определенное время.

> Acesta precizeaza data pe care serverul o ia in considerare pentru a determina daca mai aveti sau nu dreptul de a scrie in repository.
Сервер будет учитывать это время / дату, чтобы определить, имеете ли вы право на запись файлов в репозиторий или нет.

> Fiecare proiect are data limita de predare, iar din momentul expirarii acestui termen, cu precizie de secunda, nu veti mai avea dreptul sa faceti “push” cu nimic spre repository-ul proiectului.
У каждого проекта будет дедлайн и по истечении крайнего срока, с точностью до секунды, у вас больше не будет прав на push чего-либо в репозиторий проекта на основном сервере.

> Aceasta data e folosita ca garantie, in cazul in care va conectati la server pentru a face “push” cu doar cateva secunde inainte de expirarea termenului, si pentru a sti ca operatia a inceput de exemplu la ora 23, 41 de minute si 50 de secunde.
Эта дата используется в качестве гарантии, в случае, если вы подключитесь к серверу, чтобы сделать "push" всего за несколько секунд, до истечении крайнего срока и убедиться, что операция началась, например в 23:41:50.

> Deci, chiar daca operatiunea dureaza foarte mult (de exemplu daca ceilalti 1000 de colegi ai vostri se conecteaza pentru a face “push” in acelasi timp, putin probabil, dar chiar si in acest caz), ora care determina daca aveti acces este cea de inceput, adica ora din mesaj.
И даже если выполнение самой операции будет идти очень долго, например, если 1000 других ваших коллег подключатся и сделают push одновременно, что маловероятно, но даже в этом случае, время, которое было зафиксировано в сообщении, оно определяет, есть ли у вас доступ на запись файлов.

> Ca atare, chiar daca operatia “push” dureaza 5 minute si se termina la ora 23 si 46 de minute, in timp ce ora limita este 23 si 42 de minute, nu e grav, pentru ca a inceput inainte de ora limita.
Даже если выполнение "push" длится уже 5 минут и выполнится он в 23:42, в то время, как 23:42 это крайний срок, не важно, вы выполнили команду до 23:42, важно только то, что у вас был доступ к выполнению команды push, чтобы закончить проект.

> Ceea ce conteaza este sa nu intrerupeti conexiunea.
Самое главное не прерывать соединение.

> Daca intrerupeti cu “ctrl-C” si vreti sa reluati, poate ca ora limita a trecut deja si veti fi blocati.
Don't push "ctrl-C" to cancel a clone while cloning it either, because if you restart cloning, maybe the time limit will now have expired and nothing will save you.

Если вы прервёте клонирование с помощью "ctrl-C" и захотите его возобновить, то возможно срок подачи уже истечет и вас уже ничего не спасет.

> De asemenea, veti observa poate, daca sunt multe conexiuni in acelasi timp, ca veti avea un mesaj cum ca sunteti in coada de astepare dupa ce lansati comanda.
Также, вы можете заметить, что при наличии множества соединений одновременно, у вас будет сообщение о том, что вы находитесь в очереди, после отправки вашего запроса.

> Din nou, nu e grav, dar sa nu intrerupeti conexiunea.
Не паникуйте и не прерывайте соединение.

> Serverul va spune ca e suprasolicitat si ca trebuie sa asteptati.
Сервер скажет вам, что он перегружен, и что вы должны подождать.

> Veti fi informati periodic cu numarul de persoane din fata voastra in coada.
Вас будут периодически информировать о количестве людей перед вами в очереди, на отправку запроса.

> Inca o data, nu va alarmati, e perfect normal, trebuie sa asteptati.
Опять же, не волнуйтесь, это совершенно нормально, просто немного подождите.

> Inca doua-trei informatii de final.
И еще кое-что на последок.

> Identificarea pe server se face cu ceea ce numim ticket “Kerberos".
Идентификация на сервере выполняется через тикеты "Kerberos".

> II primiti in mod automat cand va conectati pe statia voastra de lucru.
Вы будете автоматически их получать, когда будете логиниться на компьютере.

> Dar, asa cum va veti da seama la un moment dat, ticketele Kerberos expira, deci trebuie reinnoite din cand in cand.
Но в какой-то момент вы поймете, что тикеты имеют истекают по времени, поэтому, время от времени, их надо будет обновлять.

> Daca vreti sa verificati ca aveti un ticket Kerberos valid, puteti folosi comanda “klist”, care va lista ticketele voastre.
Если вы хотите проверить, что у вас сейчас действительный Kerberos тикет, то вы можете воспользоваться командой "klist", которая покажет вам ваши тикеты.

> De exemplu eu am aici un ticket Kerberos care expria in 27 iunie 2013 la ora 3 dimineata.
Например, у меня есть тикет, который истечет 27 июня 2013 года в 3 часа утра.

> II voi distruge in mod intentionat pentru a vedea ce se intampla daca nu-l avem.
Сейчас я намеренно уничтожу их, чтобы посмотреть, что произойдет, если у меня их не будет.

> Execut “kdestroy” si dupa cum vedeti nu mai am nici un ticket.
Выполняем команду "kdestroy" и как вы видите, у меня нет тикетов.

> Acum, daca incerc sa execut “git clone”, imi va da un mesaj de acces interzis (“permission denied”).
Теперь, если я попытаюсь использовать команду "git clone", то мне выдаст сообщение ("permission denied").

> Utilizez comanda “kinit” cu numele de utilzator si parola mea, pentru a obtine un ticket nou.
Теперь воспользуюсь командой "kinit" с моим логином и паролем, чтобы получить новый тикет.

> Cu “klist” verifc faptul ca am un ticket, iar acum pot sa execut “git clone”, operatie care va functiona fara nici o problema.
С помощью "klist" я проверю, есть ли у меня тикет, и теперь я могу выполнить команду "git clone", которая будет работать без проблем.

> Asadar, daca va veti lovi de aceasta problema, veti sti ca solutia este “kinit”.
Так что, если вы столкнетесь с этой проблемой, то вы будете знать, что решение через "kinit".

> O ultima informatie despre o operatie pe care nu ati vazut-o pentru ca am facut-o inainte, dar pe care va trebui sa o faceti cand incepeti sa lucrati pe statia voastra de lucru.
И еще кое-что чего вы не видели, т.к. я вам этого еще не показывал, когда вы воспользуетесь комьютером в первый раз, вам нужно будет сделать это самостоятельно.

you won't have it when you'll use your computer for the first time, so you'll have to do it yourself.

translateme
> Cand veti incerca sa faceti un “commit”, “git” va va atentiona ca nu cunoaste numele si nici mail-ul vostru, si veti vedea un mesaj foarte lung de eroare pentru a va configura accesul la “git”.
Когда вы захотите сделать "commit", "git" вам скажет "я не знаю не знаю ни логина, ни пароля, но я сгенерирую автоматически их для тебя" и вы увидите очень длинное сообщение об ошибке, которое говорит вам чтобы вы настроили ваш "git" и т.д.

translateme
> Este foarte simplu, trebuie lansate doua comenzi, pe care “git” vi le indica.
Это очень просто, вы должны будете выполнить две команды, которые вам указывает «git».

translateme
> Ca atare, nu va impacientati cand veti vedea mesajul, nu ati stricat nimic.
Поэтому когда вы это увидите, то не переживайте, вы нигде не накосячили, просто делайте, так как сказано.

translateme
> Faceti ceea ce va indica, completand numele si email-ul, si “git” va fi multumit.
Напишите ваше имя, фамилию и почту и "git" будет рад этому.

translateme
> Am facut practic turul complet al cunostintelor necesare pentru a folosi serverul Vogsphere, iar eu va recomand inca o data sa mergeti sa cititi documentaia de pe “git-scm.com”, pentru ca “git” e un sistem foarte evoluat care ofera mult mai multe posibilitati decat extrem de simplul exemplu pe care vi l-am prezentat azi.
Так, мы обсудили почти все, что вам нужно знать о Vogsphere, я еще раз настаиваю на том, чтобы вы прочитали документацию на сайте “git-scm.com”, потому что «git» - это очень продвинутая система, которая предлагает гораздо больше возможностей, чем в том простом примере, который я вам сегодня показал.

translateme
> Ce am aratat eu este esentialul necesar pentru a va putea preda proiectele, dar se pot face lucruri mult mai geniale cu “git” daca stiti sa-l folositi, incat ar fi pacat sa nu va documentati despre asta si sa nu utilizati toate posibilitatile acestui minunat program.
this was just the essential to manage deliverin something
Все это является основой для управления отправкой чего-либо. В любом случае вы сможете сделать очень много классных штук с "git", зная лишь только как их использовать, будет очень стыдно не проинформировать себя в этом и не воспользоваться каждой возможностью этой замечательной программы, которая вам предлагает.

translateme
> Ajunge cu propaganda pentru “git”, va doresc o zi buna si pe curand!
И пожалуй на этой пропаганде "git" и я желаю вам отличного дня, еще увидимся.