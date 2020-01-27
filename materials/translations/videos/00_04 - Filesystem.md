> Am văzut impreuna cateva comenzi de baza pentru a se deplasa in directoare si subdirectoare, a crea un director, a-l șterge.

И так, после того, как мы рассмотрели некоторые простые команды, которые позволяют нам перемещаться по поддиректориям директорий, создавать новый директории и удалять их и т.д.

> Acum vom reveni mai in detaliu la întrebarea ce e un sistem de fișiere, la ce corespunde, si, acum ca aveți comenzile ca sa deplasați in directoare, va fi probabil mai simplu sa intelegi totul.

Мы более подробно рассмотрим концепцию файловой системы, для чего она нужна, и теперь, когда вы знаете команды для перемещения по директориям, то наверное, вам будет проще понять это видео.

> Un sistem de fișiere e, in mare, modul de organizare al fișierelor pe hard disk.

Файловая система - это способ организации файлов на жестком диске.

> E reprezentat de un slash rădăcină, baza sistemului vostru.

Директория, прямо или косвенно включающий в себя все прочие директории и файлы файловой системы, называется корневой "root", она обозначается символом "/" (slash).

> De acolo aveți alte directoare, pe care vi le puteti imagina ca niște cutii in care puteti pune alte cutii, care sunt si ele subdirectoare.

> In aceste cutii puteti pune obiecte, care sunt fișiere, si asa mai departe.

Начиная с "root" у нас есть директории, и эти директории можно представить, ввиде коробок, в которые вы можете поместить больше коробок, поддиректорий.

> Deci puteti avea un director cu mai multe subdirectoare, in fiecare subdirector fișiere, etc.

А в эти коробки вы можете поместить объекты или файлы и т.д.
И так, получается у вас может быть директория с поддиректориями, которые заполеныны файлами и т.д.

> Putem vedea asta ca un arbore, si de altfel vorbim despre arborescenta de fișiere si de sistem de fișiere.

Зачастую ее представляют ввиде дерева каталогов (директорий).

> Deci cum v-am spus, sistemul vostru de fișiere se numește "/".

Итак, как я уже говорил, ваша корневой каталог обозначен символом slash "/".

> Daca tastati "cd /", sunteti la baza sistemului vostru.

Если вы введете "cd /" то окажитесь в корневом каталоге вашей файловой системы.

> Trebuie sa intelegeti ca in sistemul de fișiere exista partea "sistem", unde utilizatorul nu are neaparat drepturile, si unde probabil nici nu poate sa intre.

Необходимо понимать, что в файловой системе есть "системная" часть, к которой пользователь не имеет права доступа и куда он не сможет войти.

> Apoi aveți directorul "home", care va va urmări oriunde, independent de calculatorul pe care sunteti, care conține fișierele voastre.

Затем, у вас есть домашний каталог "home", который будет следовать за вами куда угодно, независимо от того, на каком компьютере вы находитесь в школе и этот домашний каталог будет содержать все ваши личные файлы.

> Cum sunteti pe "/", daca faceți "ls -la" cum am văzut inainte, vedeți mai multe fișiere.

И так, как мы все уже видели, если я введу "ls -la" находясь в "/", то мы увидим множество файлов.

> Deci după cum v-am spus, cel mai in stanga aveți drepturile.


Так что, как я уже говорил, слева у нас колонка прав доступа.

> "d" inseamna "directory" si semnifica un director.

"d" - это каталог.

> "-" semnifica un fișier, nu un director.

"-" - значит, что это файл, не каталог.

> Vedeți aici un director... si un fișier; si partea cu drepturile.

И так, директории, файл, а далее идут права доступа "rwxrwxrwx".

> O sa reusesc... Asa... Drepturile.

> Utilizatorul caruia ii aparține directorul. Grupul utilizatorului. Marimea.

User, кому эти каталоги / файлы пренадлежат, группа к которой принадлежит сам user, размер файла / каталога, временная метка, когда создали или изменили и имя.

> Data ultimei modificări sau data creării. Si numele.

> ".." după cum v-am spus e directorul de deasupra (in arborescenta).

".." - как я уже сказал, представляет собой предыдущий каталог

> Imi veți spune "Suntem in /. Daca fac .. ?" Pai daca faceți "..", pur si simplu ramaneti in "/".

Вы спросите "Мы в /, если я перейду в .. , то что произойдет?" Чтож, если вы попытаетесь перейти в ".." из корневого каталога, то ничего не произойдет, сами попробуйте.

> Daca faceți "cd" pur si simplu, veți merge in directorul "home" al vostru.

Если вы просто введете "cd", то вас перенаправит на ваш личный домашний каталог.

> Aduceti-va aminte, "pwd" va arata unde sunteti.

Помните, "pwd" покажет вам, где вы находитесь.

> Veți remarca de asemenea, ca directorul vostru de "home" e reprezentat printr-o tilda (un mic val).

Также, вы заметите, что ваш домашний каталог отображается ввиде тильды "~", маленькой волны.

Когда вы увидите тильду, эту волну, то это будет значить, что вы дома, в домашнем каталоге.

> Când vedeți asta, doar sunteti in directorul vostru.
