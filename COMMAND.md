# Basic
```
jj git clone URL
jj desc -m "MESSAGE"
jj new
jj new BASE
jj edit TARGET
```

# Existing Branch
```
jj bookmark set BRANCH
jj bookmark track BRANCH --remote=origin
jj git push -b BRANCH
```

# New Branch
```
jj git push --named BRANCH=@
```

# Merge, Well, It's a Rebase
```
jj rebase -s SOURCE -d DESTINATION
jj bookmark set DESTINATION -r SOURCE
jj git push -b DESTINATION
```

# Rebase after PR
```
jj git fetch
jj rebase -d SOURCE@REMOTE -d DESTINATION
jj git push -b DESTINATION --force
```
