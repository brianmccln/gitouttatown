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

  // make extra-sure you are in that folder
     ls // you should see the contents of the gitouttatown folder

  
  // Initialize the local directory as a Git repository. It will make a default branch called master:
     git init


  // or keep it simple and let git set default branch to master
      git init -b main // overrides default name of master branch, renames it main


  // check status
  git status
  // see the new invisible .git folder which contains the meta data for tracking changes
  git ls -la 

  // Stages all files for the first commit:
  git add .

  git status // see that the files are all green, meaning staged and ready for commit

  git commit -m 'first commit' // don't forget to add message

  // tell git the location of the remote repo
  git remote add origin 'https://github.com/brianmccln/gitouttatown.git'

  // push the gitoutoftown contents up to GitHub
  git push -u origin master // next time you just need to say git push
  
  // go to GitHub and refresh the gitoutoftown page and see if the pages made it there!