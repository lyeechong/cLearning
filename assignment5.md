Malloc, Free and Functions
==
###Due Thur 26th at 11:59pm.

##Functions?

Soooo do you know what the difference is between a function and a method?

Functions - don't return things (eg: void return type)
Methods - return things (eg: not a void return type)

In Java, everything is called a method regardless of whether or not it returns something.
In C, everything is called a function regarless of whether or not it doesn't return something.

Ohhhh welll. At least you have been enlightened.

##Malloc and Free?

In Java, memory is allocated for you automatically whenever you require it (eg: a new Object).
In C, you need to allocate your own memory other you segfault all over the place (the executable poops itself and doesn't know how to clean up).

To allocate memory, you use the <code>malloc</code> function. This allocates a specified amount of memory on the heap (you specify how much) for you to use for... stuff.

To deallocate memory, you use the <code>free</code> function. This marks that spot of memory in the heap as "free" memory which can be reused later.

##Memory leaks

Why do you need to call free? If you don't call free, that piece of memory will be marked as allocated forever (until you shutdown the computer). This leads to what's called memory leaking, where you have memory which isn't actually being used, but is marked as used.

What's the big deal? Eventually you'll run out of memory and your computer will derp. Always free otherwise other programmers will hate you.

##Malloc example

malloc takes one parameter, which is how much memory you want in terms of bytes. It returns a pointer to the allocated space in memory, or a null pointer if you ran out of memory (downloadmoreram.com).

You can calculate how many bytes an int is by hand, but it gets harder for structs and stuff, so usually you use the <code>sizeof</code> function in C. The sizeof function returns how large that variable type is in bytes for that specific machine (since in C, the size of ints, etc vary based on machine architecture).

<code>int * array = malloc(10 * sizeof(int));</code>

The code example above will allocate an integer array of size 10 and point the array pointer to it.
Super simple right? Now how to free that memory...

##Free example

free takes one parameter, a pointer. It will free the memory at this pointer.
To continue our example with the array pointer, we can do:

<code>free(array);</code>

Simple!

##Note on functions

Functions in C are just like Java. You know how to write them from the K&R book. Just remember they need to be declared before the call statement!

##Your turn

Write a program which allocates some memory for a buffer, asks a user to type a word, store that word in the buffer and print it out.
Then free the buffer.

Don't forget to upload to github!
