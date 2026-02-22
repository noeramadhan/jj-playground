# Init
```
jj init
jj clone URL

jj config set --user user.name "Your Name"
jj config set --user user.email "your@email.com"
```

# Changes
```
jj d "MESSAGE"
jj new
jj new BASE
jj edit TARGET
```

# Create and Push Branch, Step-by-Step
```
jj push BRANCH
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
jj push BRANCH
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

# Alias (~/.config/jj/config.toml)
```
init = ["git", "init"]
clone = ["git", "clone"]
fetch = ["git", "fetch"]
push = ["util", "exec", "--", "bash", "-c", "jj b s $1 && jj git push -b $1", ""]
d = ["desc", "-m"]
```
