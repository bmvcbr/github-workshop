# github-workshop
Repository for the KHE 2021 Github Workshop!

## Github - What Is It, and Why Use It?
If you already know what github is, skip this section.

Github is for project management! Here's some reasons to use Github:

- It allows you to share projects, either with a team or with the whole world, and set permissions on who can and can't contribute.
- If you don't have permission to edit a project, you can 'fork' it -- make a copy of it -- and edit it all you want Github uses Git, a version control system (like SVN, if you've used that) that lets you work on your projects from any computer, and lets you go between different saved versions anytime you want.
- When you have multiple people working on a project, Git also helps handle "merge conflicts" -- when two different users submit two different, conflicting submissions.
- A bunch of other neat organization tools, like issues, wikis, and readme files like this one!!

## Github Glossary
Some Github terms you might be confused by:
- Git Version control system. You install this on your computer to let you easily move things to and from Github
- Github The website hosting everything submitted by Git.
- Repository (or repo) Any github project. Basically just a set of files hosted on GitHub.
- Clone You can take a Github repo and clone it to your local computer so you can work on it.
- Commit Once you have a local clone of a repo, you can submit a commit of your changes back to the parent repo. Each commit is basically a 'version', when we talk about version control.
(Note that git commit won't submit your code to Github on its own. The full process for committing code is git add [whatever files were changed], git commit -m "your commit message", git push. We'll go over this later.)

## Github Setup
The first thing we need is to set up a GitHub account. If you already have a GitHub account, skip this portion.
1. Go to github.com and sign up with a unique username, and an email you can access.
2. Select the free account option and press continue.
3. You'll now need to confirm your email.

## Installing Git

### Mac/linux Git Install instructions:
If you're using a Mac or Linux OS, open up the terminal. On a mac, you should be able to find it by searching for "terminal", or looking in your Applications folder. To see if you have git, type

git --version

and press enter. If you don't have it yet, follow these instructions, and then restart your terminal to see if it worked.

### Windows Git Install Instructions:
If you're using a Windows computer, open up Windows Powershell. You should be able to find it by searching for it. (Command Prompt would also work.) To see if you have git, type:
git --version

and press enter.
If not, follow the install wizard here: https://git-scm.com/downloads

It's a suggestion to "use Git and optional Unix tools from the Windows Command Prompt." The rest of the options, the default settings will work. 

If you don't have it yet, follow these instructions, and then restart your powershell to see if it worked. For either setup, remember to do these commands too:

git config --global user.name "Your name" OR

git config --global user.email "your@email.com"

## Repo Setup through GitHub
Once you have a confirmed Github account, click on the + icon in the upper lefthand corner of GitHub, and select "New Repository". Name your repository whatever you want -- "My first site" or something. Add a description, decide whether you want it to be public or not, and check the box that says "initialize this repository with a README". Congrats, you just made your first Github repo!

## Cloning the Repo
Now that you have Git installed, we can finally clone our repo! But first, we need to learn how to use our terminal.

Your terminal always points to somewhere on your computer, and we can type different commands to navigate through our computer and interact with files. (Tip: Pressing 'tab' in the terminal will try to autocomplete whatever you're typing.)

Here are the terminal commands we'll be using: cd [somewhere] stands for "change directory". Replace [somewhere] with an existing folder.

cd ../ will take you back one folder (ex: if you're in ~/Files/myfolder/, cd .. takes you to ~/Files/)
ls is an abbreviation for "list", which doesn't make sense but whatever. It lists all the files and folders in your current directory.
mkdir [folder name] stands for "make directory". Will make a folder named [folder name] in the current directory.

Type cd Desktop you'll navigate straight to your desktop. From there, navigate to wherever you want to keep your project on your folder. You can also type: mkdir projects or something to make a folder named "projects" on your desktop (You would then type cd projects/ to go inside of that folder.)

Once you're in the folder you want to store your projects, go back to your github repo, and click the green Go to your repo page on Github and find the green button that says 'Clone or download', and copy the URL it shows. Go back to the terminal and the following command, replacing [ur] with the URL you copied:

git clone [url]
You just cloned your repo to your computer! You can now enter cd [repo name] to go into your repo.

## Making Our Website

### Installing a text editor
VS Code is a super cool text editor, but there are others to choose from, like Sublime or Atom! For this workshop, we will use VS Code. You can install it here: https://code.visualstudio.com/

### Create a new branch
Let's create and checkout a new branch. ```git checkout -b [branch name]``` See if it created your new branch by doing ```git branch``` We'll make the changes just on this branch.
In your local clone of your repo, make a new file and name it with the extension .html, like "index.html" or "website.html". In this file, we'll be writing HTML, our first language! Then, go to the file and double click it. It should open up in your browser, just like a normal website would!

<html>
 <head>
 
 <title>My first website, yo !</title>
 
 </head>
 <body>

  <h1>Best website ever</h2>
 
  <p>Here's some text in a 'paragraph' tag</p>
  <p>Here's some more text, with a <a href="https://youtu.be/zbc2LUAP6G4">link!</a>
  <img src="https://i.kym-cdn.com/entries/icons/mobile/000/025/999/Screen_Shot_2018-04-24_at_1.33.44_PM.jpg" height="200px" width="400px">

 <div class="myDiv"> This is a special divider.</div>
 
  <button onclick="alert('hello world')">Here's a button </button> 
 
  <!-- This is an HTML comment. It won't affect the actual content of the page -->
 
 </body>
</html>
Save these changes. If we do, git status, we'll see the file was changed.

Go to the file location in your file explorer/finder and double click it. It should open up in your browser and you can see the HTML code!


Note: HTML is used to format text, and tell the browser what each text is for. It works by surrounding text opening tags, like , and closing tags, like . The head tags surround information about the website, while the body tags show the actual content of the website. If any of these tags confuse you, turn to google to learn about them!

## Pushing to our Github Repo with Git
So, now we have a website! Let's save it to our Github repo, so the whole world can see it! Go back to your terminal and navigate to your repo folder. There's three steps to saving to Github: Add your files by typing:

git add [filename]

The astrisk is used to mean "everything in this folder." Alternatively, we could type git add index.html to only submit a single files.

Commit your files with:

git commit -m "initialized index"

Note that commiting your code creates a log of what has been added, and gets it ready to put onto Github, but it doesn't actually transfer it yet!

Entergit push to "push" all your local commits to your github repo.

If you didn't get any errors, go to Github and see if your code is all there!

## Further Steps
If you didn't like using the terminal during this lesson, Github Desktop is a fun alternative. It allows you to press buttons instead of having to remember commands! Here is a link to install it: https://desktop.github.com/
