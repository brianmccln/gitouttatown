# Open Terminal and make a project folder with some files

For practice with the Terminal, make your local project using CLI:

    cd ~/Documents // go to Documents by way of ~ (the Desktop root)

    pwd - print working directory: tells you you are in Documents

    ls // see all the visible files and folders in Documents

    cd Brian // go into Brian folder that already exists in Documents (or go into any folder you want to use; this step is optional)

    mkdir = gitouttatown // make a directory called gitouttatown

    cd gitouttatown // go into the new gitouttatown folder

    ls // list the contents of the gitouttatown folder (it's empty)

    touch README.md // make a new empty file called README.md inside the gitouttatown folder 

    ls // list the contents of the gitouttatown folder (README.md)

    echo '<h1>Welcome to my Website</h1>' >> index.html // make an html file inside gitouttatown folder

    ls // list contents of gitouttatown (README.md  index.html)

    touch mission-and-vision.txt // make a new empty text file

    ls // contents (README.md  index.html  mission-vision.txt)

    mkdir text // make a new folder called text (inside gitouttatown)

    ls //  README.md   index.html   mission-vision.txt    text

    // move .txt file inside text folder
    mv mission-vision.txt text/mission-vision.txt 

    cd text // go inside the text folder

    ls // what's inside text folder: mission-vision.txt

    // rename text file (mv = move but not moving it anywhere, so it just renames it -- BUT you could rename AND move in same command)
    mv mission-vision.txt mission-vision-values.txt

    ls // what's inside text folder: mission-vision-values.txt

    cd .. // go back up a level to the the gitouttatown directory

    ls // README.md   index.html    text

    // in VSCode: File > Open Folder and browse to gitouttatown
       to open the thegitouttatown directory in Explorer 

    // Open README.md and add a little markdown:
       # About this Project
       This project exists solely for practicing git and github. 
       For extra terminal practice, all folders and files were made using the Terminal CLI (Command Line Interface).
       This README file was made using Terminal commands, 
       but this README content was typed in the VSCode editor.

     // Save README.md and thee open index.html in VSCode
        Currently, index.html contains only the h1 tag: <h1>Welcome to my Website</h1>
        This tag was made when the html file was created in the Terminal
     // On line 1, type ! and hit Enter. 
        This gives the basic.html required tags.
        Move the h1 tag into the body and copy the h1 text to the title
        Save the index.html file.

     // open the mission-vision-values.txt file and add this markdown:

        # Vision vs. Mission

        Similar to a mission statement, a vision statement provides a concrete way for stakeholders, especially employees, to understand the meaning and purpose of your business. However, unlike a mission statement – which describes the who, what and why of your business – a vision statement describes the desired long-term results of your company's efforts. For example, an early Microsoft vision statement was "a computer on every desk and in every home."\

        Before determining your vision statement, you need to understand what it is not. It should not be confused with a mission statement. Those statements are based in the present and designed to convey why the business exists to both members of the company and the external community.\

        Vision statements, on the other hand, are future-based and meant to inspire and give direction to employees of the company rather than customers.\

        https://www.businessnewsdaily.com/3882-vision-statement.html
  
# Make new repo at GitHub

Log into GitHub and go to your profile page
    From + plus-sign drop-down menu, choose New Repository

Give the new repo a Name:
     gitouttatown
     Give the new repo a Description (optional):
     Just a repo for practicing git-github moves

     Leave Public radio button selected.
     Leave the checkboxes unchecked for create README file, etc.
     To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub.

Click the green "Create repository" button. 
     This takes you to the repo's own screen:

Copy the HTTPS URL: https://github.com/brianmccln/gitouttatown.git


# Initialize Local Git Repo, Stage and Commit files, Push to remote GitHut repository

  // In VSCode, choose File > Open Folder and navigate to the gitouttatown folder and click Open.

  // Click any button that makes you approve the folder (I Trust the Authors blah blah).
     The gitouttatown folder and its contents will appear in Explorer, at left in VSCode.
  
  // In VSCode, you can do all your git commands using the GUI, starting by clicking the
     Source Control button, but for this exercise, we are practicing git-github via the CLI,
     so from the VSCode menu, choose: View > Terminal
  
  // see where you are -- you should be in gitouttatown folder -- if not, navigate there:
     pwd 
     // cd ~/Documents/Brian/gitouttatown // navigat to gitouttatown folder

  // make extra-sure the gitouttatown folder has the expected files:
     ls // you should see the contents of the gitouttatown folder

  // Initialize the local directory as a Git repository. It will make a default branch called master:
     git init

   // see that git is not yet tracking this folder 
     git status // "Not a git repository"

   // tell git to start tracking changes to gitouttatown
      git init  // "Initialized empty Git repository" (empty in that no files committed yet)

  // or override default branch name (master) and call it something else, like main:
     git init -b main // overrides default name of master branch, renames it main

  // now that git has been initialized, check the status again
  git status // all files show up in RED meaning "Untracked" -- git knows these files exist, but
  you haven't told git to track them (yet)

  // show the contents -- they are the same as the untracked files in red
  ls

  // see the new invisible .git folder which contains the meta data for tracking changes
  ls -la  // shows all files PLUS invisible .git folder that plain "ls" does not reveal

  // Stages all files for the first commit:
  git add .

  git status // "Changes to be committed" all files are green (staged and ready to commit)

  git commit -m 'first commit' // don't forget to add message in quotes

  // tell git the location of the remote repo -- nothing happens yet
  git remote add origin 'https://github.com/brianmccln/gitouttatown.git'

  // push the gitoutoftown contents up to GitHub -- you get a ton of Terminal feedback
  git push -u origin master // next time you just need to say git push
  
  // go to GitHub and refresh the gitoutoftown repo screen to see if our pages made it..!

  # Make local changes and push them to GitHub again

  // Make some changes to the README.md file
  Such as: # Some more info about this project
         The local git repo has already been pushed successfully to GitHub.
         But now the local repo is being changed with updates to this README file.
         So, the changes will have to be pushed up to GitHub again.

   // git status to see README.md in red, meaning it's been changed but not staged yet
   git status

   // stage everything that has been changed
   git add .  
   // or to just stage the one file that has had changes made to it:
   git add README.md 

   // git status to see README.md in greening, meaning it's staged
   git status

   // commit the staged README.md file:
   git commit -m 'readme file updated'

   // push the changed README.md file up to GitHub, so that local and remote are in sync:
   git push

   // go to GitHub and refresh gitouttatown repo. The README.md should have the new content.

  # Make remote changes at GitHub and pull them down to local repo

  // the reverse of making changes locally and pushing them to GitHub is to make changes  
  // remotely at GitHub and then pulling them down to the local repo

  // go to GitHub gitouttatown repo and copy-paste the code in index.html

  // make a new file called about.html and paste the content into it.

  // change the Welcome title and h1 to say About Us or something appropriate for an about page

  // go back to local repo at VSCode and in the terminal type:
  git pull // the about.html page appears in the gitouttatown folder.
  
  # Make a new local branch, add content to it

  // We want to work on a new section of the website, but keep it separate from the main branch until it is ready./// suppose we are making a gallery page for the website, with slideshows and videos.
  // we make a new branch, say, gallery, or, to allow for expansion, named for the developer working on it
  // the new branch will automatically receive all the contents of the master branch
  // then inside that new branch we make the gallery.html page or whatever else.
  // then we push the new branch to GitHub where it appears as a new branch.

  // make a new branch
  git branch brian-branch

  // switch to the new branch
  git checkout brian-branch  // notice as you work that the result of all CLI commands is reflected in VSCode GUI
  // so, after switching to brian-branch, it has switched from master to brain-branch in the lower left corner
  
  // see what's in brian-branch -- so far it should be an exact copy of master branch
  
  // make a new file in brian-branch
  touch gallery.html // just a blank file instead of echoing a tag
  // in VSCode, open gallery.html and type ! to add basic tags.
  // add some minimalist content:
   <title>Multimedia Gallery</title>
    <h1>Welcome to Our Multimedia Gallery!</h1>
    <h2>Slideshows</h2>
    <h2>Videos</h2>
    <h2>Audio Interviews</h2>
    <h2>Animation</h2>

  // stage and commit gallery.html
  git add gallery.html    // or just git add .
  git commit -m 'add multimedia gallery page'

  # Push the new branch up to GitHub
  // push while simultaneously instructing GitHub to make a new brian-branch for this:
  git push --set-upstream origin brian-branch

  // the next push is just "git push" since it already knows to go to brian-branch

  // make another file: games.html
  touch games.html

  // Open games.html in VSCode and type ! to add basic tags.

  // add some minimalist content:
  <title>Games</title>
    <h1>Blackjack</h1>
   <h2>Memory Matching Game</h2>
   <h2>Fun Quiz</h2>

  // see the unstaged new file in red:
  git status

  // stage and commit the new file
  git add games.html
  git commit -m 'add games page with blackjack, memory matching game and fun quiz'

  // ?!?!?!? When I ran git push it said that I had already done it..
  // make some changes to games.html and try add-commit-push again
  // this is because this file Git-GitHub-Procedure.md was changed and not staged

  // change games.html and take it from the top with add-commit-push, this time adding all:
  git add .

  git commit -m 'Chinese Zodiac Animals Educational Game added'

  git push

  // go back to GitHub and refresh repo to see that games.html has the new content:
  <h2>Chinese Zodiac Animals Educational Game</h2>
  
# -- MERGE BRANCH --
// make a new branch called branch-to-merge and switch to it
git branch branch-to-merge
git checkout branch-to-merge

// add an html page to branch-to-merge
touch privacy.html

// open privacy.html in VSCode and type ! on line 1
// make a title and h1 called Privacy Policy
// add a p tag with a sentence of gibberish about privacy policy

// make another html page to branch-to-merge
touch faq.html

// open faq.html in VSCode and type ! on line 1
// make a title and h1 called Frequently Asked Questions
// add a p tag with a question: Why should I buy your widgets?
// add a p tag with an answer: Because our widgets are the best!

// stage and commit the new files
git add .
git commit -m 'add privacy and fag pages'

// tell GitHub that we are switching to new brach

# merge branch-to-merge with master branch






# Clone a Remote Repo: Make a Remote Repository and pull it down to local project folder (local repo)


# Resolve Conflicts: Make Remote and Local changes to the same file and merge when pulling
