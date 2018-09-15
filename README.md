# Getting started
## Installation
### The simplest way to install `git`, the fastest tool for working on the same code together in a team, visit:
- [https://git-scm.com/download/win](https://git-scm.com/download/win) for Windows
- [https://git-scm.com/download/mac](https://git-scm.com/download/mac) for MacOS

Once installed, open up your Powershell terminal on:
- Windows by pressing `Win`+`R` and typing `powershell`, then hit `Enter`
- Mac by opening `Terminal.app`, which is inside the Utilities folder of launchpad

You'll want to pin the terminal to your dock/taskbar so you can open it easily later.

Type in `git` and hit `Enter` (you always press `Enter` at the end of a command in your terminal). If you see a bunch of explanatory text - good job, you installed it correctly!

## Using git
With your terminal open, visit [this site](https://ndpsoftware.com/git-cheatsheet.html), it's an interactive git cheatsheet that will explain everything in depth.

In short, you start off with your workspace (the folder where all your code is) and make changes there, and then you add it to your index. Once you have all files you want to update or upload to github in your index so your team can download it, you commit the changes. When you have enough commits done, you push the code to github.

### Lets start!

Go to github and create a new repo by clicking on the `+` sign in the top right and picking "New repository". You'll be taken to a page where you can enter the name and description of the repo. 

Take a look at your url now - this is where your code will live. Next step is to copy the url of your repo, and then go into your terminal and type `cd Desktop` to change into your desktop. One you do that, you can type `ls` or `dir` on Windows to list all the files on your desktop. This is how to move around and look at files on your machine through the terminal.

Now that you have your reposity url copied, paste it after another command, `git clone`, like so:

```
git clone <your repository url>
```

You should have a new folder on your desktop, and since your repo should be empty, so should the folder. Type `cd <folder name>` to go into the folder, from your terminal.

Make a new file in the folder (use `touch <filename>` on mac), and then open it with your preferred editor.

As you make new files or make changes to existing ones, the code on your local repository will need to be synced with the code online in github.com.

Once you have changes or new files in your repo after coding, type in:
```
git status
```
This will show you a lot of useful information on the current changes and differences you have with the online repo, and `git diff` will be more in-depth.

However, you might not be up-to-date with the latest changes on the remote repo on github, so to keep your current work while also being able to update and see differences, use `git fetch`.

Next step is to add your changes to your **Index**, also known as the stage. This is where code goes when you modify it and want to make a new commit that will be visible on the repo.

Do this by typing:
```
git add <filename>
```
Or more often than not, if you want to add every file, you can use a dot, which meants **all files** in the folder:
```
git add .
```

To remove files and put them back, use:
