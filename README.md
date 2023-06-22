# How to solve this problem of "! [rejected] main -> main (fetch first)"

First Do this ...

```bash
git fetch origin main
git merge  main
```
Then, do this ...

```bash
git fetch origin main:tmp
git rebase tmp
git push origin HEAD:main
git branch -D tmp
```
Now everything works well.
