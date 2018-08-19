// CLONE
git clone URI 


// PUBLISHING
git add .
git commit -m "string"

git push 
git push --set-upstream origin "name"


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

git diff (wkg to HEAD)
git diff
git diff branchA branchB
git diff HEAD~3..HEAD~1



// REVERSING
single file
git checkout HEAD~4 file.name.ext


// CHERRY PICKING
