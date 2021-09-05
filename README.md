# Practice using git and GitHub

## Summary of Steps to Complete (See corresponding sections below.)
- [ ] 1. Create a GitHub repository, link it to your computer, push your local changes to your GitHub repository.
- [ ] 2. Fork a repository so you can work on your own copy.
- [ ] 3. Create a "Pull Request" so your changes can be added to the original project.

## 1. Starting a GitHub repository.

### Creating the repository on GitHub

* [ ] Sign in to GitHub: https://github.com/
* [ ] On the right side of the page, click on the `New repository` button.
* [ ] Give your repository any name you like and make sure that the repository is public.
* [ ] You can go ahead and check the option to initialize the repository with a README.md file.

### Link your local repository to the GitHub repository

* [ ] Create a folder in the place you keep material for this class called `myProject`.
* [ ] Go into that folder.
* [ ] Create a file called `myName.txt` and add your name to that file.
  * [ ] Windows open command line: https://www.youtube.com/watch?v=2KOFRYDMv4A&list=PLYmfkjWhXgi6bdFbdOpXIpW1LQuFOgCkQ&index=3
  * [ ] Windows navigate directories from command line: https://www.youtube.com/watch?v=rfgH2lN6MzE&list=PLYmfkjWhXgi6bdFbdOpXIpW1LQuFOgCkQ&index=4
  * [ ] Windows create empty file from command line: https://www.youtube.com/watch?v=rd2O_Kr3GGI
  * [ ] Mac open a terminal window: https://www.youtube.com/watch?v=QROX039ckO8
  * [ ] Mac navigate directories from terminal windows: https://www.youtube.com/watch?v=j6vKLJxAKfw
  * [ ] Mac create empty file from command line: https://www.youtube.com/watch?v=P2iDTBsh4ho or https://www.youtube.com/watch?v=RWLT_9l76Bc or https://www.youtube.com/watch?v=J1goN2FVoIo
* [ ] Save the file and open a terminal window.
* [ ] In your terminal window, `cd` to your `myProject` folder.
* [ ] Run `git init`. (Initializes your folder for tracking changes with git.)
* [ ] Go to your new repository on GitHub and copy the address shown when you click the 'Clone or download' button. (Instead it may be the address in the Quick setup window. The address should be the same either way. It should look something like https://github.com/yourusername/yourrepositoryname.git .)
* [ ] Run `git remote add origin [Repository URL goes here]`. (This stores the address for your GitHub repository with your local repository.)
  * (If you DID initialize your repository with a README, you must do a `git pull origin main --allow-unrelated-histories` first - to get the README file on your computer - before you'll be able to push.) 

### Push your local code to GitHub

2021 update: GitHub has changed the default name for the main repository from "master" to "main". I'm trying to replace all instances of "master" with "main" in instructions for this course. If I miss any, use the word "main" instead of "master". It's possible you'll see older screen shots with old terminology. There may be some errors with these changes. Here's a resource on StackOverflow which explains some of it. https://stackoverflow.com/questions/65173291/git-push-error-src-refspec-main-does-not-match-any-on-linux
* [ ] Open a terminal window and make sure it is in the directory of `myProject`.
* [ ] Run `git add nameOfMyFile.fileExtension`. (This tells git you want to track changes on that file and adds it to the staging area.) or you can run `git add .` to add all files.
* [ ] Run `git status`. (This will show what has changed in git.)
* [ ] Run `git diff`. (This shows what code has changed in the file.)
* [ ] Run `git commit -m "The sentence I want associated with this commit message"`. (This prepares the changes to be pushed to GitHub and logs the message you specify.)
* [ ] Run `git push origin main` (Your code is now pushed to GitHub. Be sure to include `origin main`, as this tells GitHub which branch you want to push to, and creates the branch if it doesn't exist yet.) If you get an error, it could be because the `git init` statement you ran earlier gave your repository the default name of "master". You can rename your local repository by running the command `git branch -m master main` then try the command `git push -u origin main`
* [ ] Go to your repository on GitHub and see your updates.
![Commands Screenshot](https://github.com/cmcntsh/exerGitPractice/blob/master/gitPracticeSample.png?raw=true)
* (You can also see the pdf instruction sheets with screenshots included in this repository.)

Here's a short summary of the steps to successfully clone your repository. If you encounter a problem check if you missed any of these steps.

1. Sign in to GitHub
1. Create a new repository with a README.md file
1. Create a folder on your computer where you want to put this assignment. (I called mine createTest)
1. Create a file in that folder called myName.txt
1. Open a terminal in that folder
1. git init
1. Copy the address for your repository on GitHub
1. git remote add origin [Repository URL goes here]
1. git pull origin main --allow-unrelated-histories
1. git add .
1. git commit -m "First commit sentence."
1. git branch -m master main
1. git push -u origin main
1. Refresh the window for your repository on GitHub and see your updates. You should now see your .txt file in your repository.

## 2. Fork a repository

### Fork the repository into your own account on GitHub

* [ ] On this current GitHub repository, scroll to the top and look for a button that says `fork`.
* [ ] Click the `fork` button. (This copies all the code from the original repository into a new repository on your own GitHub account.)

### Clone the forked repository to your computer.

* [ ] Go to your forked repository on GitHub. It should appear under `Your repositories` which is next to the `New repository` button.
* [ ] Click on the green `clone or download` button and copy the URL.
* [ ] Open a terminal window and navigate to the folder where you keep work for this class.
* [ ] Run `git clone [the url you copied]`. (That copies the repository from your account on GitHub to your computer so you can make changes.)

### Make a change in your file and push it to GitHub

* [ ] Open the folder in your coding IDE.
* [ ] Make a change in a file.
* [ ] Run through the steps to push your changes to your remote repository ( status, diff, add, commit, push ).
  * Since you've cloned this repository, it is already pointing to your forked version. Therefore, you don't need to tell your computer where to push the code.

## 3. Creating a pull request (and some extra practice cloning a repository to your computer) (Statistics students can skip this part.)

### Delete and re-clone

* [ ] Delete the folder on your computer for the forked repository.
* [ ] Re-clone the fork to your folder where you keep work for this class.
* [ ] Make a change to any file.
* [ ] Run through the process of pushing to GitHub ( status, diff, add, commit, push ).

### Background - Why fork a repository?

If groups of individuals are working on the same project and everyone pushes code to one repo without verifying the quality of the code, things can get messy pretty quick. GitHub fixed this solution with 'Pull Requests.' Basically, you fork a project, make changes to your fork, then you make a Pull Request (PR) back into the original project requesting that some piece of code be added to the original repo. This is how the vast majority of open source code projects work. In this step, we will make a pull-request.

### Create a pull request (optional)

This part is optional. I'm leaving these instructions here so you are aware about pull requests. But we won't be working with this functionality this semester. Feel free to try it out if you want.

* [ ] Go to your forked repo on GitHub.
* [ ] Locate the button that says `Pull Request` and click it.
* [ ] Locate the green button that says `New pull request` and click it.
  * You should now see the file changes you've made and how they differ from the original repo.
* [ ] Click on the `Create pull request` button to submit your PR.
* [ ] Now if you navigate to the <a href="https://github.com/DevMountain/learn-git/pulls">original repository</a> and take a look at the `Pull Requests` your new pull request should be there.

## Original material
https://github.com/wlh18/learn-git
