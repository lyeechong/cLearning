#Do you even C?
==
###Due Sat Dec 21st at 11:59pm

##Before you start

Read the K&R book enough so that you can get a little taste of C. We'll be doing Hello World in C for this assignment, so at least read that far.

##Starting off

Now that you know how to do basic git and unix commands, we can start diving into C.

Fire up VMWare Player and create a new file called
<code>hello.c</code>
inside your local repository.

Now edit the file and write a program which will print
<code>Hello world!</code>
to standard output.

Hint: K&R includes a great example of hello world in C. Use K&R for all your C needs!

##So you think you got it?

Great! Now that you've written the program, you need to see if it works!

Not so fast though! In C, you need to compile the program before you can run it. :P

##Compiling in C

To compile your program, fire up a terminal and navigate to where your hello.c file is.

You'll be using gcc, one of the C compilers (there are many). Run this command to compile it:

<code>gcc hello.c</code>

If it complains about something, you did something wrong and you should feel bad and go read the K&R book again.
Otherwise, good job!

Now take a look at what it did! Use <code>ls</code> to see the new file it created, called <code>a.out</code> (It usually is called a.out, except in some cases.)

##Making stuff executable

This usually isn't needed since by default, stuff which is compiled by gcc is marked as executable, but this is something you should definitely know for later assignments and in general.

This is the compiled version of your program, and now you need to make it have executable permissions, since in Unix, you can't just execute any file since that's a security risk.

To give it executable permissions so you can run it, run the change mode command like so:
<code>chmod +x a.out</code>
chmod is the change mode command, which changes the permission bits on a file so Unix knows what it can/should not do. The <code>+x</code> flag indicates you're making it eXecutable, and <code>a.out</code> is the file you're modifying.

And as like most commands in unix, don't worry if there's not output; most people who program unix commands tend to make them as lightweight as possible.

##Running your program

The fun starts here.

You can run your program with:
<code>./a.out</code>

And you should see <code>Hello world!</code> in your terminal!

If it looks a bit strange, maybe you derped and forgot the newline at the end.

To explain a little bit about what the command does, the "." in "./" is your current directory (so if you do <code>cd .</code>, it changes directory into your current directory). This is telling unix the thing you want to run is in your current directory.

##Good job, young Skywalker, but there's a little more...

Great! You programmed your first C program, now you need to commit to github.

Since you're still new to git, I'll walk you through again. I'll be too lazy to do this with other assignments though (and you should know how to do this by then).

Do <code>git add hello.c</code> to add your hello.c file to git's tracking system.

Then you need to commit your changes, so do <code>git commit -am 'Yay my first C program'</code> (feel free to change the commit message).

Great, you committed, but your changes are only reflected in your local repository, not the remote one yet. Now you need to push:
<code>git push</code>

And if you go to the github repository (online, in your browser), you should be able to see your hello.c file there. See you next time bro!
