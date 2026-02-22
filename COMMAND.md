# Init
```
jj git init
jj git clone URL

jj config set --user user.name "Your Name"
jj config set --user user.email "your@email.com"
```

# Changes
```
jj desc -m "MESSAGE"
jj new
jj new BASE
jj edit TARGET
```

# Create and Push Branch, Step-by-Step
```
jj b s BRANCH
jj git push -b BRANCH
```

# Create and Push Branch, for New Branch
```
jj git push --named BRANCH=@
```

# Merge, Well, It's a Rebase, Everywhere
```
jj rebase -s SOURCE -d DESTINATION
jj b s DESTINATION -r SOURCE
jj git push -b DESTINATION
```

# Rebase. Current Branch
```
jj rebase -o SOURCE
jj b s BRANCH
jj git push -b BRANCH
```

# Rebase after PR, Everywhere
```
jj git fetch
jj rebase -s SOURCE@REMOTE -d DESTINATION
jj b s DESTINATION
jj git push -b DESTINATION --force
```

# Rebase after PR, Current Branch
```
jj git fetch
jj rebase -o SOURCE@REMOTE
jj b s DESTINATION
jj git push -b DESTINATION --force
```
