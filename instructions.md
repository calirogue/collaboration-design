# Instructions for the project

0. On the project: https://github.com/bellagrunt/collaboration-design on the top right of the github page. 
Press "Fork" and allow the project to be forked into your github. Then on terminal or powershell do these commands:
1. Go to the directory you want to make the project in.. 
$ mkdir git-demo

2. $ cd git-demo

3. Then go back to the page where it was forked and click on the green button that says, "git clone or down".
$ git clone git@github.com:yourgithubname/collaboration-design.git

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

7. Get the latest changes from upsteam:
$ git fetch upstream

8. Create a new branch:
$ git checkout -b yourusername

- Go to index.html and read the html file and answer the question or add a question. 
(Make changes to the repo)

9. Add the changes you want to local:
$ git add .

10. Commit
$ git commit -m "some changes"

11. Push to origin
$ git push origin branchname

12. Go to github and create pull request

13. Merge with master
<!-- 
13. back to terminal and do:
$ git rebase upstream/master
$ git checkout master
$ git merge upstream/master -->

