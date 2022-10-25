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