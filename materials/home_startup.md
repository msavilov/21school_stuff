# Linux settings

------------

### 1 - Linux Ubuntu
1. Скачиваем VMware (https://nnmclub.to/forum/viewtopic.php?t=1338267)    
Сразу оговорюсь, VMware очень хорошо оптимизирована, а VirtualBox - имеет много косяков. 
2. Скачиваем Ubuntu Desktop 18.04.3 (64-bit) (https://ubuntu.ru/get) 
3. Устанавливаем виртуалку на VMware, ничего сложного нету, главное выделите 20 гб свободного места 
4. После установки заходим в терминал и учимся    
5. В терминале прописываем sudo apt install  
6. Сразу смело ставьте эти пакеты.
```
sudo apt install gcc && git && make && vim && gnome-tweak-tool
```
gnome-tweak-tool нужна для изменения раскладки на alt-shift: заходим в Tweaks → KeyBoard&Mouse → Additional Layout Option → Switch to, меняем на нужную раскладку

### 1.1 - macOS Sierra
macOS Sierra - для тех, кто хочет понять, что такое макось (для тестов сойдет и Linux)
1) образ https://nnmclub.to/forum/viewtopic.php?t=1151080
2) инструкция https://youtu.be/WYkgtMEDUXQ
3) у кого bootloop при старте пишем в файле macOS 10.13.vmx 
cpuid.1.eax = "0000:0000:0000:0001:0000:0110:1010:0101"
smc.version = "0"

------------

### 2 - Переходим с bash на zsh
Почему? Читаем habr https://habr.com/ru/post/326580/
1. Устанавливаем ZSH $ sudo apt-get install zsh
2. Скачиваем и устанавливаем oh-my-zsh $ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
3. Сделать ZSH шеллом по умолчанию $ sudo usermod -s /usr/bin/zsh имя_юзера. 
4. После установки на дефолт нужно перезагрузить машину
5. Чтобы выбрать новую тему, исправьте значение переменной ZSH_THEME в файле ~/.zshrc (ZSH_THEME="agnoster") и перезагрузите терминал    
• Тема agnoster: для нормальной работы требуется скачать шрифты и перезагрузка терминал или самой машины    
• Добавить строчку в ~/.zshrc, чтобы были подсказки по установке пакетов – (. /etc/zsh_command_not_found)

------------

### 3 - Vim settings
#### 3.1 - Vundle plugin manager (https://github.com/VundleVim/Vundle.vim)    
•	Устанавливаем плагин согласно инструкции, в пункте, где надо прописывать в ~/.vimrc (если его нет, то создайте) - комментируем дефолтные плагины, которые показаны для иллюстрации (комм. - значит убираем в кавычки " ).    
•	Если ставили zsh, то следуя одному из пункту установки – пишем в ~/.vimrc в конце файла, под всеми настройками.
```set shell=/bin/zsh```

#### 3.2 - NERDTree + nerdtree-git-plugin (https://github.com/Xuyuanp/nerdtree-git-plugin)
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
3. Для установки и обновления плагином в vim пишем :PluginInstall, чтобы открыть дерево используем ctrl+n, переключаться между окон в vim ctrl+w

#### 3.3 - Monokai - цветовая тема (https://github.com/tomasr/molokai)
1. Создаем папку под настройки vim в домашнем каталоге, если ее там нет
```
mkdir -p ~/.vim/colors
```
2.	Скачиваем, устанавливаем и удаляем скачанную папку
```
git clone https://github.com/sickill/vim-monokai.git ~/vim-monokai && mv -v vim-monokai/colors/monokai.vim ~/.vim/colors/ && rm -Rf ~/vim-monokai
```
3.	Airline: темы стрелок https://github.com/vim-airline/vim-airline. Прописываем в ~/.vimrc в раздел bundle:
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
5.	Для установки и обновления плагинов через Vundle в vim пишем :PluginInstall и перезагружаем терминал

#### 3.4 - Стандартные настройки
Пропишите данные команды в конце файла vim ~/.vimrc:
```
set number
"показать нумерацию строк
set cursorline
"подсвечивает курсор
```
