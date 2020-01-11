# 3. Visual Studio Code #

### 3.1 - Extensions ###
Easy Code
   * [Тема one-monokai](https://marketplace.visualstudio.com/items?itemName=azemoh.one-monokai)
   * [Color Highlight / #RGB](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
   * [Trailling spaces](https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces)
   * [SirTori / Выделяет текущую глубину отступа](https://marketplace.visualstudio.com/items?itemName=SirTori.indenticator)
   * [Умное выравнивание колонок](https://marketplace.visualstudio.com/items?itemName=lmcarreiro.vscode-smart-column-indenter)
   * [MultiColorHighlighter](https://marketplace.visualstudio.com/items?itemName=456ken.multicolorhighlighter)
   * [Great Icons](https://marketplace.visualstudio.com/items?itemName=emmanuelbeziat.vscode-great-icons)

Comment
   * [42 Header bind](https://marketplace.visualstudio.com/items?itemName=kube.42header)
   * [Comment Anchors](https://marketplace.visualstudio.com/items?itemName=ExodiusStudios.comment-anchors)
   * [Better Comment / через Ctrl+/](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.bettercomment)

GitHub Markdown
   * [Markdown All in One / для работы с .md](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
   * [Markdown table from CSV/TSV](https://marketplace.visualstudio.com/items?itemName=jojoco.markdownfromcsv)
   * [Github Markdown Preview](https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview)

Other
   * [pdf preview](https://marketplace.visualstudio.com/items?itemName=tomoki1207.pdf)

### 3.2 - Notes ###
Disable mini-map (settings.json): `"editor.minimap.enabled": false     // disable mini-map`

### 3.3 - Windows 10: WSL + Code Debug with mingw64(incide MSYS2) ###
Установка MSYS2:
1. Скачиваем msys2-x86_64 и устанавливаем согласно [инструкции](http://www.msys2.org/)
2. `pacman -Ss gcc` // ищем пакеты связанные с gcc и выбираем нужный нам для компиляции
3. `pacman -S mingw-w64-x86_64-toolchain` // устанавливаем нужным пакет
4. Открываем Пуск / MSYS2 MinGW 64-bit и пишем `gcc -v`, чтобы проверить их наличие, если не работает то перезапустите терминал и попробуйте еще раз
5. Для возможности использования инструментов в cmd.exe (таких как ls -l, или rm): перейдите в Мой компьютер / Свойства / Дополнительные параметры системы / Дополнительно / Переменные среды / Переменные среды для пользователя Username / Path → Изменить → Создать `C:\msys64\mingw64\bin` и `C:\msys64\usr\bin`
6. Да, как вариант, вы можете не использовать WSL на MSYS2, но вы должны понимать в чем их различия.

Настройка VSCode / debug:
1. Устанавливаем recommended расширения по типу [С++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
2. Меняем настройки терминала Ctrl+Shift+P / Preferences: Open Settings (JSON) / settings.json
```
{
    // Terminal settings
    "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\wsl.exe",
    "terminal.integrated.env.windows": { "CHERE_INVOKING": "1" }, // Use this to keep bash from doing a 'cd ${HOME}'
    "terminal.integrated.automationShell.windows": "powershell.exe", // prevent fails of build task when integrated shell https://github.com/microsoft/vscode/issues/43588
}
```
3. Переходим к коду, который будем debug'ить: File / Open Workspace / *ваш проект* / main.c
4. Создаем `tasks.json`: Terminal / Configure Tasks:
```
{
    "tasks": 
    [
      {
        "type": "shell",
        "label": "gcc.exe build active file",
        "command": "C:\\msys64\\mingw64\\bin\\gcc.exe",
        "args": 
        [
          "-Wall",
          "-Wextra",
          "-Werror",
          "-g",
          "${file}",
          "-o",
          "${fileDirname}\\${fileBasenameNoExtension}.exe"
        ],
        "options": {
          "cwd": "C:\\msys64\\mingw64\\bin\\bin"
        }
      }
    ],
    "version": "2.0.0"
  }
```
5. Переходим опять к main.c и создаем `launch.json`: Debug / Add Configuration:
```
{
    "version": "0.2.0",
    "configurations": 
    [
        {
            "name": "Build (gcc) and debug (gdb) active file",
            "type": "cppdbg",
            "request": "launch",
            "program": "${fileDirname}\\${fileBasenameNoExtension}.exe",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "gdb",
            "miDebuggerPath": "C:\\msys64\\mingw64\\bin\\gdb.exe",
            "setupCommands": [
                {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ],
            "preLaunchTask": "gcc.exe build active file"
        }
    ]
}
```
6. Переходим опять к main.c и Debug / Start Debugging