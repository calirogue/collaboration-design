# Instructions for the project

Fork
Clone
Create an upstream to my original - i can send you the git command if you need help with that
create a branch
do some work
git push branch
do a pull request
ping me
ill merge

0. On the project: https://github.com/bellagrunt/collaboration-design on the top right of the github page. 
Press "Fork" and allow the project to be forked into your github. Then on terminal or powershell do these commands:
1. Go to the directory you want to make the project in.. 
$ mkdir git-demo

2. $ cd git-demo

3. Then go back to the page where it was forked and click on the green button that says, "git clone or down".
$ git clone https://github.com/bellagrunt/collaboration-design.git
enter username and password

4. $ cd collaboration-design

5. $ git remote -v
It should say:
origin	git@github.com:yourgithubname/new-game.git (fetch)
origin	git@github.com:yourgithubname/new-game.git (push)

6. Now add upstream in order to get the latest changes:
$ git remote add upstream git@github.com:bellagrunt/collaboration-design.git

Verify that origin and upstream are correct:
$ git remote -v
output: ..
origin	git@github.com:yourgithubname/new-game.git (fetch)
origin	git@github.com:yourgithubname/new-game.git (push)
upstream git@github.com/bellagrunt/collaboration-design (fetch)
upstream git@github.com/bellagrunt/collaboration-design (push)

7. Create a new branch:
$ git checkout -b yourusername

- Go to index.html and read the html file and answer the question or add a question. 
(Make changes to the repo)

8. Add the changes you want to local:
$ git add .

9. Commit
$ git commit -m "some changes"

10. Push to origin
$ git push origin branchname

11. Go to github and create pull request

12. Merge with master

