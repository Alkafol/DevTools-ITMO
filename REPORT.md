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

### 5 task
git checkout {commit name}  
3c82 - commit with regress  

### 6 task
.env appear in commit "add Game model and its migration"  
git filter-branch --index-filter "git rm -rf --cached --ignore-unmatch .env" -- --all  
echo '.env' >> .gitignore  
git add .gitignore  
git commit -m "chore: update .gitignore"  

### 7 task
git checkout feature  
git filter-branch -f --env-filter "GIT_COMMITTER_NAME='Semenov Roman'; GIT_COMMITTER_EMAIL='semenovroman8@gmail.com';" 4cac..HEAD  

### 8 task
git config rerere.enabled true  
git checkout master  
git merge feature  

*Fix conflict in editor*

git add README.md  
git commit -m "feat: add feature"  

*Undo merge*  
$ git reset --hard HEAD~1  

git merge feature  
git add README.md  
git commit -m "feat: add feature"  

### 9 task
git fsck

### 10 task
du -hs .git  
git gc --prune=now --aggressive  
du -hs .git  