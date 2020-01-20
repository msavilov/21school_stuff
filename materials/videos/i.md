Let's get started with libraries.

I've prepared two files, function "ft_putchar.c" and "ft_putstr.c".

I'am sure you'll all know what these do.

Syntax may be a little different, but I'am sure you'll understand how I did it.

But that's not our main focus right now.

I simply get back to creating a basic program.

So, you know that if I wanted to write "bonjour les gens\n" (Hello people), thanks to our function "ft_putstr", I should write a "main", that calls this function and then compile.

We agree, that if I only compiled my main.c, the compilers gonna have it go at me and tell me, thanks for calling function "ft_putstr" but as I don't know what it is I can't do what you're asking.

So let's add function "ft_putstr.c" and now it tells me "I can't find function "ft_putchar" you're calling in function "ft_putstr.c".

So let's add function "ft_putchar.c" and now it should compile, and display my "bonjour les gens\n".

I'm telling you all of this again, because in order to create libraries, well first need to compile the functions you want to put in it.

if I compile just my function "ft_putstr.c", it will tell me that it still isn't a function "ft_putchar", but most importantly we need a "main", in order to create an executable, as we've learned earlier on in the bootcamp.

But I need to add my function "ft_putstr" to my library and I dont need my "main".

For that "gcc" as an option "-c". Check out the "man" for more info.

But look, it's created a ".o", function "ft_putstr.o". It's an object, it's computer language.

As you can see, if you try to display it, it's nonsensical. Our new computer can read it.

But in order to do anything, we'll need a main.
As I sad earlier, in order to create a library we'll need ".o" files.

Just imagine your program is a wall and your ".o" file is a brick, a brick that's ready and that you'll be able to place in more than one more.

In the sense that's once you've made your brick, you won't need to make it again and each time you'll be able to use it everywhere.

Thats actually quite practical. "gcc" knows about it, you could simply just use our ".o" line this.