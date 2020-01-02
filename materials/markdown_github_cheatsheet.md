markdown.md cheatsheet
```
TODO:    
https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf    
https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md    
```

https://github.com/tchapi/markdown-cheatsheet    
https://github.com/sandino/Markdown-Cheatsheet    
https://www.markdownguide.org/basic-syntax    
https://assemble.io/docs/Cheatsheet-Markdown.html

------------

### 1. заголовки / headers ###

# h1 #
## h2 ##
### h3 ###
#### h4 ####
##### h5 #####
###### h6 ######

Alt-H1
======

Alt-H2
------

```
# h1 #
## h2 ##
### h3 ###
#### h4 ####
##### h5 #####
###### h6 ######

Alt-H1
======

Alt-H2
------
```
------------

### 2. игнорирование синтаксиса md / syntax ignore md ###
\*literal asterisks\*

```
\*literal asterisks\*

Markdown provides backslash escapes for the following characters:
\ backslash
` backtick
* asterisk
_ underscore
{} curly braces
[] square brackets
() parentheses
# hash mark
+ plus sign
- minus sign (hyphen)
. dot
! exclamation mark
```

------------

### 3.1 ссылки / links ###
[Обычная ссылка в строке](https://www.google.com)    
[Обычная ссылка с title](https://www.google.com "Сайт Google")    
[Относительная ссылка на документ](../blob/master/LICENSE)
```
[Ссылка в строке](https://www.google.com)
[Ссылка с title](https://www.google.com "Сайт Google")
[Относительная ссылка на документ](../blob/master/LICENSE)
```

### 3.2 изображения / images ###
![](https://github.com/zanydazanydnaya/cheatsheets/blob/master/materials/finn_example.png "Title is optional")
```
![](https://github.com/zanydazanydnaya/cheatsheets/blob/master/materials/finn_example.png "Title is optional")
```

------------

### 4. линии / lines ###

---
***
___
```
---
***
___
```

------------

### 5.1 ненумерованный список / unsorted list ###

* Можно размечать звездочками
  * Item 2a
    * Item 3b
- Или минусами
+ Или плюсами
```
* Ненумерованный список можно размечать звездочками
  * Item 2a
    * Item 3b
- Или минусами
+ Или плюсами
```

### 5.2 нумерованный список / sorted list ###
1. Первый пункт нумерованного списка
2. Второй пункт
   * Ненумерованный вложенный список.
1. Сами числа не имеют значения, лишь бы это были цифры
   1. Нумерованный вложенный список
4. И еще один пункт.

   Внутри пунктов списка можно вставить абзацы с таким же отступом. Обратите внимание на пустую строку выше и на пробелы в начале (нужен по меньшей мере один, но здесь мы добавили три, чтобы также выровнять необработанный Markdown).

   Чтобы вставить разрыв строки, но не начинать новый параграф, нужно добавить два пробела перед новой строкой.  
   Этот текст начинается с новой строки, но находится в том же абзаце.  
   (В некоторых обработчиках, например на Github, пробелы в начале новой строки не нужны.)
```
1. Первый пункт нумерованного списка
2. Второй пункт
   * Ненумерованный вложенный список.
1. Сами числа не имеют значения, лишь бы это были цифры
   1. Нумерованный вложенный список
4. И еще один пункт.

   Внутри пунктов списка можно вставить абзацы с таким же отступом. Обратите внимание на пустую строку выше и на пробелы в начале (нужен по меньшей мере один, но здесь мы добавили три, чтобы также выровнять необработанный Markdown).

   Чтобы вставить разрыв строки, но не начинать новый параграф, нужно добавить два пробела перед новой строкой.  
   Этот текст начинается с новой строки, но находится в том же абзаце.  
   (В некоторых обработчиках, например на Github, пробелы в начале новой строки не нужны.)
```

------------

### 6. text formatting ###
_italic text_ or *italic text*    
__bold text__ or **bold text**    
___bold italic text___ or ***bold italic text***    
~~Strikethrough text~~    
_You **can** combine ~~them~~_

```
_italic text_ or *italic text*  
__bold text__ or **bold text**    
___bold italic text___ or ***bold italic text ***
~~Strikethrough text~~
_You **can** combine ~~them~~_
```
