# Home startup
Откуда весь материал? Из сети. Все собрано по кусочкам и лично для себя. Я не выкладываю и выкладывать не буду готовые решения задач с комментраиями. Тут собраны материалы, которые помогут вам только организовать граммотную работу с самим кодом. Я не могу точно сказать, что это вам все пригодится в школе, т.к. я сам не знаю, что там будет. Прежде всего, думаем исключительно своей головой, никто за вас решать задачи не будет. Всем добра.

------------

### 1.1 - Windows 10 (Bash + Visual Studio Code)
Для тех, кто не хочет закачивать образы и запускать их на виртуальной машине предлагаю этот самый простой и удобный способ.
1. Открываем Start menu в Windows 10 и ищем PowerShell, запускаем его от имени администратора
2. Прописываем в PowerShell чтобы активировать Bash в Windows и настроить ее под себя:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
3. Скачиваем Linux Ubuntu из Microsoft Store и запускаем ее. Она должна обновиться!
4. Вероятнее всего, что некоторые пакеты вы установить не сможете, поэтому читаем вывод в терминал и ищем решение. Я решил проблему через ```apt-get update```:    
   1. Переключаемся в root и скачиваем обновления: ```sudo su && apt-get update```
   2. Устанавливаем для теста gcc: ```sudo apt install gcc```. Если установка прошла успешно, то значит можно работать.
5. Скачиваем [Visual Studio Code](https://code.visualstudio.com/)    
Это редактор кода, он довольно многофункционален и гибок. Вы его можете и не устанавливать, а пользоваться только самой консолью Linux Ubuntu, кому как удобней будет, во всяком случае я советую попробовать и то, и то.
6. Заходим в Visual Studio Code и меняем терминал: ctrl+shift+p → Terminal: Select Default Shell → WSL Bash
   * Терминал открываем снизу или crtl+shift+'

### 1.2 - Linux Ubuntu
1. Скачиваем VMware (ищите на торрентах repack, могу лишь посоветовать nnm-club.ru).
2. Скачиваем [Ubuntu Desktop](https://ubuntu.ru/get).
3. Устанавливаем виртуалку в VMware, ничего сложного нету, главное выделите 20 гб свободного места.
4. Сразу смело ставьте эти пакеты, через терминал:
```
sudo apt install gcc && git && make && vim && gnome-tweak-tool
```
   * gnome-tweak-tool нужна для изменения раскладки на alt-shift: заходим в Tweaks → KeyBoard&Mouse → Additional Layout Option → Switch to, меняем на нужную раскладку

### 1.3 - macOS Sierra
macOS Sierra - для тех, кто хочет понять, с какой OS мы будем работать в школе.
1) Образ macOS [Sierra v.10.12.5 (16F73)](https://nnmclub.to/forum/viewtopic.php?t=1151080)
2) [Установка](https://youtu.be/WYkgtMEDUXQ) macOS Sierra VMWare Workstation 
3) У кого bootloop при старте, пишем в файле macOS 10.13.vmx
```
cpuid.1.eax = "0000:0000:0000:0001:0000:0110:1010:0101"
smc.version = "0"
```
4) [Настройка клавиатуры](https://o7planning.org/ru/11555/how-to-use-windows-like-shortcuts-in-mac-os-virtual-machine)

------------

### 2 - Переходим с bash на zsh
Почему? Читаем [habr](https://habr.com/ru/post/326580/)
1. Устанавливаем zsh ```sudo apt-get install zsh```
2. Скачиваем и устанавливаем oh-my-zsh ```sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"```
3. Сделать ZSH шеллом по умолчанию ```sudo usermod -s /usr/bin/zsh имя_юзера```, после установки нужно перезагрузить терминал.
4. Чтобы выбрать новую тему, исправьте значение переменной ```ZSH_THEME="agnoster"``` в файле ~/.zshrc и перезагрузите терминал.   
   * Тема agnoster: для нормальной работы требуется скачать шрифты [fonts-powerline](https://github.com/powerline/fonts) и перезагрузка терминал или самой машины. 
   * Не забудьте скачать и установить сами шрифты себе, (если используете терминал через Win10) [DejaVuSansMono](https://github.com/powerline/fonts/tree/master/DejaVuSansMono). Для Bash на Ubuntu на Windows: заходим в терминал → кликаем на значок слева сверху → Настройки → Шрифт → Выбираем DejaVu Sans Mono.    
   Для Visual Studio Code: ctrl+shift+p → Terminal → меняем Font Family и Font Size под (DejaVu Sans Mono for Powerline)
6. Добавить строчку в ~/.zshrc, чтобы были подсказки по установке пакетов ```. /etc/zsh_command_not_found```

------------

### 3 - Vim settings
#### 3.1 - [Vundle plugin manager](https://github.com/VundleVim/Vundle.vim)    
* Устанавливаем плагин согласно инструкции, в пункте, где надо прописывать в ~/.vimrc (если его нет, то создайте) - комментируем дефолтные плагины, которые показаны для иллюстрации.    
*	Если ставили zsh, то следуя одному из пункту установки – пишем в ~/.vimrc в конце файла, под всеми настройками.
```set shell=/bin/zsh```

#### 3.2 - [NERDTree + nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin)
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

#### 3.3 - [Monokai - цветовая тема](https://github.com/tomasr/molokai)
1. Создаем папку под настройки vim в домашнем каталоге, если ее там нет ```mkdir -p ~/.vim/colors```
2.	Скачиваем, устанавливаем и удаляем скачанную папку
```
git clone https://github.com/sickill/vim-monokai.git ~/vim-monokai && mv -v vim-monokai/colors/monokai.vim ~/.vim/colors/ && rm -Rf ~/vim-monokai
```
3.	[Airline: темы стрелок](https://github.com/vim-airline/vim-airline). Прописываем в ~/.vimrc в раздел bundle:
```
Plugin 'vim-airline/vim-airline'
Plugin 'Yavor-Ivanov/airline-monokai-subtle.vim'
```
4.	Прописываем в ~/.vimrc в конце дока
```
syntax enable
colorscheme monokai
let g:airline_theme = 'monokai_subtle'
"если стрелки не заработали
let g:airline_powerline_fonts = 1
```
5.	Для установки и обновления плагинов через Vundle в vim пишем ```:PluginInstall``` и перезагружаем терминал

#### 3.4 - 42header
Обязательный заголовок школы 42 в документ, без него Normanette будет ругаться, а Moulinette откажется проверять.    
Для visual studio code - [vsix ext](https://marketplace.visualstudio.com/items?itemName=kube.42header)    
Для vim:
1.	Создаем папку под vim плагины в домашнем каталоге, если ее там нет ```mkdir -p ~/.vim/after/plugin```
2.	Скачиваем, перемещаем и удаляем из дом.каталога
```
git clone https://github.com/pandark/42header.vim.git ~/42header && mv -v 42header.vim/plugin/42header.vim ~/.vim/after/plugin/ && rm -rf ~/42header
```
3.	Настраиваем $USER и $MAIL: заходим в ~/.zshrc (или ~/.bashrc) и прописываем строки
```
export USER=*username*
export MAIL=*usermail*
```
4.	Перезагружаем терминал и тестим командой ```:FortyTwoHeader``` в vim 
5.	Чтобы поменять с :FortyTwoHeader на :Stdheader - измените строку 187 в ~/.vim/after/plugin/42header.vim на ```command! Stdheader call s:fortytwoheader ()```.    
   Чтобы забиндить Хедер на f5, пропишите ```nmap <f5> :Stdheader<CR>``` в файле ~/.vimrc (если его нет, то создайте)

#### 3.5 - Стандартные настройки
Пропишите данные команды в конце файла vim ~/.vimrc:
```
set number
"показать нумерацию строк
set cursorline
"подсвечивает курсор
```

------------

### 4 - Прочее
#### 4.1 - norminette - проверка кода на нормы
Вне школы. Репозиторий [AzRunRCE](https://github.com/AzRunRCE/42-C-Norme)
   * Уже готовый .exe 42-C-Norme/bin/Debug/appRegex.exe. Код перемещаем в файл My_app.c и запускаем exe.
   * Установите wine mono, чтобы использовать .exe файлы на Linux    

В школе. Проверка файлов стандартной Norminette:
   * Для проверки использовать команду norminette -R CheckForbiddenSourceHeader в директ. с программой на с
   * Для проверки файлов типа *.h используется только norminette, без флагов
   * Альяс, который упрощает работу. В файле ~/.zshrc пропишите следующую строку (если файла ~/.zshrc нет то создайте его),:
   ```alias norm="norminette -R CheckForbiddenSourceHeader"```. Затем перезапустите iTerm или Terminal и набирайте norm

#### 4.2 - 42Stupidity
Компилирует, тестит (~Moulinette) и проверяет Norminette (только на территории школы).
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
./spawn.pl day02 config_d02.pl
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
#### 4.3 - Towel
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

#### 4.4 - 42 Homebrew
https://github.com/kube/42homebrew    
Moves temporary Homebrew data (Temp and Cache) to /tmp, leaving your home directory cleaner.
