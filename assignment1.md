Getting how to Git.
Due Thur 19th at 11:59pm.
==
You'll be using this repo:
https://github.com/lyeechong/cLearningTurnin

Navigate to https://github.com/lyeechong/cLearningTurnin in your browser and notice that it's pretty empty.

To get started, fire up Ubuntu on your VMWare Player.
Run this command:

<code>
git clone https://github.com/lyeechong/cLearningTurnin.git
</code>

This will clone the repo where you specify it.

Then you check how things are with

<code>
git status
</code>

git status is a useful command to see what isn't committed, what files are new, modified, etc.

Create a new file in your local git repo called "test.md"

Hints/tips:
You can run the command
<code>
gedit test.md
</code>
to fire up gedit (unix's equivalent of notepad more or less) and it'll create a file called test.md

Write a short hello message in test.md

Now you have a file with a message.

Run

<code>
git status
</code>

and notice git has realized you have a new file. You need to tell git that you want to keep track of this new file.

To do so, you run:
<code>
git add <filename>
</code>

so in your case, it would be
<code>
git add test.md
</code>

you can also run git add with regex, like
<code>
git add *
</code>

Which, in this example, adds everything which is in this directory or in a subdirectory.

Now you need to commit your changes.

Think of committing like making a milestone. The great thing about git is that you can always go back in time to one of these milestones if you mess up or accidentally delete/change something.

To commit, run
<code>
git commit -am 'my first commit'
</code>

To explain what the command does, -am means you're adding a comment to the commit, and in this case, the comment is "my first commit". You can also use double quotes with commit messages.

I'll tell you how to properly style commit messages later.

run
<code>
git status
</code>
again and see that you're now ready to push! (Since the new file has been added and you have committed)

It's time to push.
Pushing means you're uploading your local changes (on your computer) to the remote repository (which in this case, is on Github). This saves your work online.

to push, run
<code>
git push
</code>

It will ask for your credentials, type them in.

Tip: unix doesn't do ******* when you type a password, since people peering over your shoulder can count how long your password is. Instead it doesn't show anything as you type your password, so don't worry about not seeing anything as you type your password in.

It should say something along the lines of:
<code>
Username for 'https://github.com': lyeechong
Password for 'https://lyeechong@github.com': 
To https://github.com/lyeechong/cLearning.git
   499d7a4..680d2b8  master -> master
</code>

of course, your username is different, the repo address is different and the commit number (the strange hex number) would be different too.

Now to see that it worked!

Check 
https://github.com/lyeechong/cLearningTurnin

And you should see your test.md file there in github!
You can click on it to open it.

Let me know when you're done. :)
