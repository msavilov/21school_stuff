# Полотенце #
“A towel, [The Hitchhiker's Guide to the Galaxy] says, is about the most massively useful thing an interstellar hitchhiker can have.”

---

### 1.1 - OS: Windows 10 (Bash + Visual Studio Code) ###
Для тех, кто не хочет закачивать образы и запускать их на виртуальной машине предлагаю этот самый простой и удобный способ.
1. Открываем Start menu в Windows 10 и ищем PowerShell, запускаем его от имени администратора
2. Прописываем в PowerShell чтобы активировать Bash в Windows и настроить ее под себя:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
3. Скачиваем Linux Ubuntu из Microsoft Store и запускаем ее. Она должна обновиться!
4. Вероятнее всего, что некоторые пакеты вы установить не сможете, поэтому читаем вывод в терминал и ищем решение. Я решил проблему так:    
   1. Переключаемся в root ```sudo su``` и скачиваем обновления: ```apt-get update```
   2. Устанавливаем для теста gcc: ```sudo apt install gcc```. Если установка прошла успешно, то значит можно работать.
5. Скачиваем [Visual Studio Code](https://code.visualstudio.com/)    
Это редактор кода, он довольно многофункционален и гибок. Вы его можете и не устанавливать, а пользоваться только самой консолью Linux Ubuntu, кому как удобней будет, во всяком случае я советую попробовать и то, и то.
6. Заходим в Visual Studio Code и меняем терминал: ctrl+shift+p → Terminal: Select Default Shell → WSL Bash
   * Терминал открываем снизу или crtl+shift+'

### 1.2 - OS: Linux Ubuntu ###
1. Скачиваем VMware (ищите на торрентах repack, могу лишь посоветовать nnm-club.ru).
2. Скачиваем [Ubuntu Desktop](https://ubuntu.ru/get).
3. Устанавливаем виртуалку в VMware, ничего сложного нету, главное выделите 20 гб свободного места.
4. Сразу смело ставьте эти пакеты, через терминал:
   ```
   sudo apt install gcc && git && make && vim && gnome-tweak-tool
   ```
   gnome-tweak-tool нужна для изменения раскладки на alt-shift: заходим в Tweaks → KeyBoard&Mouse → Additional Layout Option → Switch to, меняем на нужную раскладку

### 1.3 - OS: macOS Sierra ###
macOS Sierra - для тех, кто хочет понять, с какой OS мы будем работать в школе.
1) Образ macOS [Sierra v.10.12.5 (16F73)](https://nnmclub.to/forum/viewtopic.php?t=1151080)
2) [Установка](https://youtu.be/WYkgtMEDUXQ) macOS Sierra VMWare Workstation 
3) У кого bootloop при старте, пишем в файле macOS 10.13.vmx
```
cpuid.1.eax = "0000:0000:0000:0001:0000:0110:1010:0101"
smc.version = "0"
```
4) [Настройка клавиатуры](https://o7planning.org/ru/11555/how-to-use-windows-like-shortcuts-in-mac-os-virtual-machine)

---

### 2.1 - Терминал: подсказки по работе ###
```
cd *каталог* – перейти в каталог
cd .. – выйти на каталог ниже
ls -l – показать все файлы в текущем каталоге
ls -la – показать все файлы вкл. скрытые
rm Rf *каталог* - удалить каталог с файлами без запросов на резрешение удаления
sudo su – выйти в root
exit – выйти из root

dpkg --list - показать установленные пакеты
sudo apt-get purge --auto-remove packagename - удалить установленный пакет
```

### 2.2 - Терминал: переходим с bash на zsh
Почему? Читаем [habr](https://habr.com/ru/post/326580/)
1. Устанавливаем zsh ```sudo apt-get install zsh```
2. Скачиваем и устанавливаем oh-my-zsh ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
3. Сделать ZSH шеллом по умолчанию ```sudo usermod -s /usr/bin/zsh имя_юзера```, после установки нужно перезагрузить терминал.
4. Чтобы выбрать новую тему, исправьте значение переменной ```ZSH_THEME="agnoster"``` в файле ~/.zshrc и перезагрузите терминал.
   * Тема agnoster: для нормальной работы требуется скачать шрифты [fonts-powerline](https://github.com/powerline/fonts) и перезагрузка терминала или самой машины.
   * Не забудьте скачать и установить сами шрифты себе, (если используете терминал через Win10) [DejaVuSansMono](https://github.com/powerline/fonts/tree/master/DejaVuSansMono).
     * Для Bash на Ubuntu на Windows: заходим в терминал → кликаем на значок слева сверху → Настройки → Шрифт → Выбираем ```DejaVu Sans Mono for Powerline```.
     * Для Visual Studio Code: ctrl+shift+p → Open settings UI → Terminal → меняем Font Family ```DejaVu Sans Mono for Powerline``` и Font Size на 12.
   * Делим строку (~с текущей директорией и >input) на две строки: редактируем файл ```~/.oh-my-zsh/themes/agnoster.zsh-theme``` → 82 строка (раздел promt_end), ```echo -n "%{%f%}"``` меняем на ```echo -n "\n%{%f%}"```. Если хотите чтобы перед input у вас был символ ">", то ```echo -n "\e[m\n>%{%f%}"```.
5. Чтобы были подсказки по установке пакетов - добавляем строчку в ~/.zshrc,  ```. /etc/zsh_command_not_found```

---

### 3.1 - Vim: [Vundle plugin manager](https://github.com/VundleVim/Vundle.vim) ###
* Устанавливаем плагин согласно инструкции, в пункте, где надо прописывать в ~/.vimrc (если его нет, то создайте) - комментируем дефолтные плагины, которые показаны для иллюстрации.    
*	Если ставили zsh, то следуя одному из пункту установки – пишем в ~/.vimrc в конце файла, под всеми настройками.
```set shell=/bin/zsh```

### 3.2 - Vim: [NERDTree + nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin)
1. Прописываем в ~/.vimrc в разделе плагинов для Vundle
```
Plugin 'scrooloose/nerdtree'
Plugin 'Xuyuanp/nerdtree-git-plugin'
```
2. Под Vundle прописываем настройки для плагина
```
"/NERDTree settings/ 
let g:NERDTreeIndicatorMapCustom = {
    \ "Modified"  : "✹",
    \ "Staged"    : "✚",
    \ "Untracked" : "✭",
    \ "Renamed"   : "➜",
    \ "Unmerged"  : "═",
    \ "Deleted"   : ":heavy_multiplication_x:",
    \ "Dirty"     : "✗",
    \ "Clean"     : "✔︎",
    \ 'Ignored'   : '☒',
    \ "Unknown"   : "?"
    \ }
"Stick this in your vimrc to open NERDTree with Ctrl+n (you can set whatever key you want):
"Bind ctrl+n
map <C-n> :NERDTreeToggle<CR>
"Show hidden files
let NERDTreeShowHidden=1
```
3. Для установки и обновления плагином в vim пишем ```:PluginInstall```, чтобы открыть дерево используем ctrl+n, переключаться между окон в vim ctrl+w

### 3.3 - Vim: [Monokai тема](https://github.com/tomasr/molokai) + Syntax hightlight ###
1. Создаем папку под настройки vim в домашнем каталоге, если ее там нет ```mkdir -p ~/.vim/colors```
2.	Скачиваем, устанавливаем и удаляем скачанную папку
```
git clone https://github.com/sickill/vim-monokai.git ~/vim-monokai && mv -v ~/vim-monokai/colors/monokai.vim ~/.vim/colors/ && rm -Rf ~/vim-monokai
```
3.	[Airline: темы стрелок](https://github.com/vim-airline/vim-airline). Прописываем в ~/.vimrc в раздел bundle:
```
Plugin 'vim-airline/vim-airline'
Plugin 'Yavor-Ivanov/airline-monokai-subtle.vim'
```
4.	Прописываем в ~/.vimrc в конце дока
```
"подсветка синтаксиса
syntax enable

"/Theme settings/
"выбор цветовой схемы
colorscheme monokai
let g:airline_theme = 'monokai_subtle'

"если стрелки не заработали
let g:airline_powerline_fonts = 1
```
5.	Для установки и обновления плагинов через Vundle в vim пишем ```:PluginInstall``` и перезагружаем терминал

### 3.4 - Vim: 42header (+ для Visual Studio Code) ###
Обязательный заголовок школы 42, без него Normanette будет ругаться, а Moulinette откажется проверять.    
Для visual studio code - [vsix ext](https://marketplace.visualstudio.com/items?itemName=kube.42header)    
Для vim:
1.	Создаем папку под vim плагины в домашнем каталоге, если ее там нет ```mkdir -p ~/.vim/after/plugin```
2.	Скачиваем, перемещаем и удаляем из дом.каталога
```
git clone https://github.com/pandark/42header.vim.git ~/42header.vim && mv -v ~/42header.vim/plugin/42header.vim ~/.vim/after/plugin/ && rm -rf ~/42header.vim
```
3.	Настраиваем $USER и $MAIL: заходим в ~/.zshrc (или ~/.bashrc) и прописываем строки
```
export USER=*username*
export MAIL=*usermail*
```
4.	Перезагружаем терминал и тестим командой ```:FortyTwoHeader``` в vim 
5.	Чтобы поменять с :FortyTwoHeader на :Stdheader - измените строку 187 в ~/.vim/after/plugin/42header.vim на ```command! Stdheader call s:fortytwoheader ()```.    
   Чтобы забиндить Хедер на f5, пропишите ```nmap <f5> :Stdheader<CR>``` в файле ~/.vimrc (если его нет, то создайте)

### 3.5 - Vim: Code lifehack's ###
Пропишите данные команды в конце файла vim ~/.vimrc:
```
"/Code lifehack's/
"показать нумерацию строк
set number

"подсвечивает курсор
set cursorline

"подсвечивает текущую строчку
set cursorcolumn

"копирует отступы с текущей строки и добавляет их при добавлении новой
set autoindent

"c indent = копирует отступы с текущей строки и добавляет их при добавлении новой для *.c файлов
set cindent

"добавляет ) после написания символа (
inoremap ( ()<left>
inoremap () ()

"добавляет } после написания символа {
inoremap { {}<Left><enter><up><end>
inoremap {} {}<Left>

"добавляет " после написания символа "
inoremap " ""<left>
inoremap "" ""

"подсвечивает красным пробелы в конце строки
highlight ExtraWhitespace ctermbg=red guibg=red
match ExtraWhitespace /\s\+$\|\s+\s{1}/

"подсвечивает синим строку, если та будет превышать 80 знаков
highlight MoreThan80 ctermbg=blue guibg=blue
:2match MoreThan80 /\%81v.\+/

"определяет ширину 1ой Tab'уляции в 4 пробела
set tabstop=4

"определяет ширину 1ой Tab'уляции в 4 пробела, при сдвиге выделенного вертикального блока вправо
set shiftwidth=4

```

Работа с Vim:
```
https://vimhelp.org/terminal.txt.html#terminal-use
:term – открыть терминал в vim
:q! – принудительно выйти
:w – сохранить
:wq – сохранить и выйти
сtrl+w – переключаться между окнами
```

---

### 4.1 - Code_check: Norminette ###
Проверка кода на соответствие нормам  
Вне школы. Репозиторий [AzRunRCE](https://github.com/AzRunRCE/42-C-Norme)
   * Уже готовый .exe 42-C-Norme/bin/Debug/appRegex.exe. Код перемещаем в файл My_app.c и запускаем exe.
   * Установите ```sudo apt install mono-complete```, чтобы использовать .exe файлы на Linux через ```mono program.exe```.
   * Альяс, который упрощает работу. В файле ~/.zshrc пропишите следующую строку (если файла ~/.zshrc нет то создайте его):
    ```alias norm="cd /mnt/d/Work/21school/21school_piscine-c/.debug/ && mono appRegex.exe && cd -"``` Затем перезапустите iTerm или Terminal и набирайте norm.    

В школе. Проверка файлов стандартной Norminette:
   * Для проверки использовать команду norminette -R CheckForbiddenSourceHeader в директ. с программой на с
   * Для проверки файлов типа *.h используется только norminette, без флагов
   * Альяс, который упрощает работу. В файле ~/.zshrc пропишите следующую строку (если файла ~/.zshrc нет то создайте его):
   ```alias norm="norminette -R CheckForbiddenSourceHeader"```. Затем перезапустите iTerm или Terminal и набирайте norm.

### 4.2 - Code_check: 42Stupidity ###
Компилирует, тестит (~Moulinette) и проверяет официальной Norminette (если вы залогинились в системе школы).
1.	Клонируем репоз. в домашний каталог в новую папку 42Stupidity
```
git clone https://github.com/mirror12k/42us-stupidity.git ~/42Stupidity
```
2.	Переходим в созданный каталог и создаем каталог, где будут храниться наши решения с файлами
```
cd ~/42Stupidity && mkdir day02/ex00
```
Или клонируем свой репоз. с выполненными заданиями day02 в текущий каталог
```
git clone vogsphere@vogsphere.21-school.ru:intra/2019/activities/piscine_c_day_02/nick day02
```
3.	spawn skript cоздает скрипты (сценарий проверки) для всех задач из каталога day02
```
./spawn.pl <day_repo> config_d<day_number>.pl
```
4.	Компилируем соотвествующий main.c для каждой функции
```
./tools/build.sh
```
5.	Проверяем наши ответы. Выполняем все тесты для каждой функции. Хорошие тесты будут отмечены, как 'good', ошибки будут выведены с большими восклицательными знаками.
```
./tools/check_all.sh
```
6.	Проверяем наши ответы на Normiette с соотвествующими флагами
```
./tools/verify.sh
```
7. Мои alias, мне так проще, не вините меня. У меня просто в папке .debug все эти инструменты для проверки
```
alias day02="./spawn.pl ../02_day02 config_d02.pl && ./tools/build.sh && ./tools/check_all.sh"
```

### 4.3 - Code_check: Towel ###
Упрощает работу (на основе 42Stupidity), действие в одну команду.
1. Клонируем репозиторий в домашний каталог в новую папку Towel
```
git clone https://github.com/oscardemadriz/towel.git ~/Towel
```
2. Переходим в созданный каталог ```cd ~/Towel```
2. Клонируем свой репоз. с выполненными заданиями day05 в текущий каталог Towel
```
git clone vogsphere@vogsphere.21-school.ru:intra/2019/activities/piscine_c_day_05/nick day05
```
3. Возможно понадобится сменить права доступа ```chmod +x towel.sh```
4. Проверяем на Norminette, комплируем и тестим ```./towel.sh day05```

### 4.4 - Code_check: code lifehack's
1. В ~/.zshrc, компилируем с флагами и проверяем main.c
```
alias main="gcc -Wall -Wextra -Werror main.c -o test && ./test"
```

---

### 5.1 - Help_stuff: 42 Homebrew ###
https://github.com/kube/42homebrew    
Moves temporary Homebrew data (Temp and Cache) to /tmp, leaving your home directory cleaner.

### 5.2 - Help_stuff: 42_RU_vogsphere_access remote ###
https://github.com/school21moscow/42_RU_vogsphere_access

---

### 6.1 - VSC: настройки ###

Easy Code
   * [one-monokai тема](https://marketplace.visualstudio.com/items?itemName=azemoh.one-monokai)
   * https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight
   * https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces
   * https://marketplace.visualstudio.com/items?itemName=SirTori.indenticator
   * https://marketplace.visualstudio.com/items?itemName=lmcarreiro.vscode-smart-column-indenter
   * https://marketplace.visualstudio.com/items?itemName=456ken.multicolorhighlighter
   * https://marketplace.visualstudio.com/items?itemName=emmanuelbeziat.vscode-great-icons

Comment
   * https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments
   * https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree
   * https://marketplace.visualstudio.com/items?itemName=ExodiusStudios.comment-anchors
   * [Better Comment / через Ctrl+/](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.bettercomment)

GitHub Markdown
   * [Markdown All in One / все для работы с .md](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
   * https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview
   * https://marketplace.visualstudio.com/items?itemName=darkriszty.markdown-table-prettify
   * https://marketplace.visualstudio.com/items?itemName=jojoco.markdownfromcsv

Other
   * https://marketplace.visualstudio.com/items?itemName=tomoki1207.pdf
   * https://marketplace.visualstudio.com/items?itemName=funkyremi.vscode-google-translate

usersettings
   * Отключить карту сбоку: In your user settings set minimap to false ("editor.minimap.enabled": false,)