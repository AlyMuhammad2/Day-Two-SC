"# Day Tow " 

---- Create a New Project and Push to Remote Repo ----
>mkdir Day-Two-SC
>CD Day-Two-SC
>git init
>echo "# Day Tow " >README.md
>>git add .
>git commit -m "Initial commit"

---- Push to Remote Repository ---
>git remote add origin https://github.com/AlyMuhammad2/Day-Two-SC.git
>git push -u origin master

---- Create Two Branches (dev & test) and Make Changes ---
---- dev branch---
>git checkout -b dev
>echo "dev file in dev branch" > dev.html
>git add dev.html
>git commit -m "Add file in dev bransh"
>git push -u origin dev

---- test branch---
>git checkout master
>git checkout -b test
>echo "test branch" > test.html
>git add test.html
>git commit -m "test file in test branch"
>git push -u origin test

---- Merge Changes to the main Branch and Push ---
>git checkout master
>git merge dev
>git merge test
>git push origin master
---------------------------------------------------------------

---- Remove Branches Locally and Remotely ---
>git branch -d dev
>git branch -d test
>git push origin --delete dev
>git push origin --delete test

---- Checkout Another Branch Without Committing Changes ---
>git stash
>git checkout another-branch
>git stash pop


---------------------------------------------------------------------------------------------------------------------
---- Create an Annotated Tag ---
>git tag -a v1.7 -m "Release version 1.7"
>git push origin v1.7

---- List All Tags ---
>git tag

---- Delete Tag Locally and Remotely ---
>git tag -d v1.7
>git push origin --delete v1.7

---- Add img ---
>git add README.md imges/shika.jpg
>git commit -m "Add img"
>git pull 
>git push origin master
![.......](imges/shika.jpg)
