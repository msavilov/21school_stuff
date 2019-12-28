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
