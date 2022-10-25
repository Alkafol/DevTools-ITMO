### 2 task
git checkout ci  
git rebase -i HEAD~2  

*In text editor:*  
reword 1003a03  
fixup 4940a90

*New message:* "chore: add deployment settings"  

git checkout master  
git merge ci
git branch --delete ci  

### 3 task
git log --graph --decorate $(git rev-list -g --all)  
git checkout f95d  
git branch old-master 

### 4 task
git blame prisma/seed.ts  
Last change - commit 3c82, 20.12.2021 