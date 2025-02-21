### Git Workflow
#### There are 4 stages in git workflow
1. Working directory
2. Staging area
3. Local repo
4. Central repo
#### We move to the next stage after these actions correspondingly
```bash
1->2: git add -> filter only changes that you want to commit
2->3: git commit -m "msg" -> commit the change to local repo
3->4: git push -> push the local's change to central repo
```
#### How to revert the action
```bash
git checkout -- <file_name> -> revert code that not added to latest version in staging area
git reset HEAD <file_name> = git restore --staged <file_name> -> move the file out the staging area
git reset -> remove the commit

#amend the last commit (adds changes or edits msg)
touch hello2.txt
git add hello2.txt
git commit --amend -m "New file has been added"


#reset (unrecommended)
git reset --soft HEAD^ # Reset to staging
git reset --hard HEAD^ --> Undo last commit and all the changes
git reset --hard HEAD^^ --> Undo last two commits

# revert to a specified commit id (recommend)
git revert <commit id>
```
