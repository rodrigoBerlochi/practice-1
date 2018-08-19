// CLONE
git clone URI 


// PUBLISHING
git add .
git commit -m "string"

git push 
git push --set-upstream origin "name"

explicit:
git push origin myBranch:remoteBranch

// GETTING NEW STUFF (MERGE)
git pull

git fetch origin
gitk origin/master 
git merge origin/master

on conflict:
resolve
git add .
git commit -m "merge ..."


// BRANCHING
git checkout -b "name"

git branch "name"
git checkout "name"

git merge "fromBranch" (to "name")

git branch
git branch -r

// TAGGING
git tag

git tag name

git --tag push 

git checkout -b tagName

// DELETING
git branch -d "name"


// REVIEWING
// BLAMING
git log
git log --pretty=oneline
git log --author=name

git whatchanged

git diff (wkg to HEAD)
git diff
git diff branchA branchB
git diff HEAD~3..HEAD~1



// REVERSING

single file
git checkout HEAD~4 file.name.ext

recommended
git revert HEAD~2 (better, is reversible)
git commit --ammend file1 (affect HEAD but not working copy)

git reset --hard HEAD~2 (irreversible, unless you..)
git reset --hard HEAD@{1}

// CHERRY PICKING

git checkout targetBranch
gitk sourceBranch (select sha1 ids)
git cherry-pick sha1-id


// STASHING
git stash save
git stash list
git stash apply
git stash clear
git stash branch bname stashid

// REPO MAINTENANCE
git repack
git prune

// BAD REVISIONS
git bisect start
git bisect bad
git bisect good
git bisect run ./test.sh
git bisect reset

// GIT FLOW
--FEATURES
git flow init (next release must be development branch)
git flow feature start name
git flow feature finish name

git flow feature publish name
git flow feature pull origin name

--RELEASES
git flow release start name
git flow release publish name
git flow release finish name (merge to master/develop, delete rel b and tag branch)
