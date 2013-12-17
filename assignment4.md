Strings aren't really strings.
==
###Due Thur 26th at 11:59pm.

##Strings in C

Strings aren't really strings, they're just char arrays. In C, that literally is true.

##Pointers

Ahhhh. We'll dive further into pointers in another assignment. I'll just talk about what is needed for now.

Pointers in C are variables which contain a memory address, so if you print a pointer without deferencing it, it'll give you the memory address of the thing it's pointing to.

A basic C variable:
<code>int k</code>

Variables in C are just like in Java, except C has a few more like unsigned ints and fixed width. Don't worry about those.

A basic C pointer:
<code>int* ptr</code>

The asterisk indicates that it is a pointer variable to something of type int. Nice!

Another C pointer:
<code>float* ptr</code>

This one points to something of type float. I think you get the point.

Let's say we have:
<code>int k = 5</code>

We can make a pointer to point to that memory address (where 5 is):
<code>int* ptr = &k<code>

The ampersand is just a way of getting the memory address of something, eg:
<code>&goose</code> gives me the memory address of goose
<code>&plane</code> gives me the memory address of plane
Etc.

So in this example, we're storing the memory address of k into ptr. Sounds good.

If you just do a <code>printf</code> on ptr, it'll print the memory address of k. You don't want that sometimes. Sometimes you want what's at that memory address (in this case, 5).
<code>printf("%d", ptr)</code> will try and print out the memory address of k (it'll throw a compile time exception first).

To do so, we deference the pointer with an asterisk:
<code>printf("%d", *ptr)</code> will print out what's at that memory address (5).

Awesome, we'll go into more complex pointer stuff later. Most programmers don't know how to use pointers in C for some reason.

##Too lazy

You should read up on how to use arrays with pointers. When you sub a pointer, you're just deferencing that location in memory. I'm too lazy to type about this.

##The assignment

Just a note, in C, printf will take a pointer as an argument if you specify the format as <code>"%s"</code>.

Your task is to reverse a string in-place. (Yay! Since you can't do this in Java.)

Here's the skeleton code:

<code>
#include <stdio.h>

void reverse(char *cstr);

int main()
{
	char buf[20]; //buffer which stores the user input
	char *ptr = buf;

	printf("Type in a word less than 20 characters: ");

	scanf("%s", ptr); //reads in a string and stores it in ptr

	reverse(ptr);

	printf("%s\n", ptr);
}


void reverse(char *p)
{
	//your code here
}
</code>

So it should print out:
<code>
Type in a string less than 20 characters: hello
olleh
</code>

You don't know enough about C to know that strings are (usually) null-terminated, so I included a length variable you can use.

Once you're done, git add, commit and push and check that it's on github!

##Bonus brownie points
Reverse the string using XOR swapping on the pointers! (You can do this since pointers are basically just integers).

##Hints if you're stuck
See what this does when you use it in reverse()
<code>p[0] = p[1];</code>
