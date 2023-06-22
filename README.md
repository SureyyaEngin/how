# How to solve this problem of "! [rejected] master -> master (fetch first)"

First Do this ...

git fetch origin main
git merge  main

Then, do this ...

git fetch origin main:tmp
git rebase tmp
git push origin HEAD:main
git branch -D tmp

Now everything works well.
