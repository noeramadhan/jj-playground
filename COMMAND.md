# Init
```
jj i
jj c URL

jj config set --user user.name "Your Name"
jj config set --user user.email "your@email.com"
```

# Changes
```
jj d "MESSAGE"
jj n
jj n BASE
jj e TARGET
```

# Create and Push Branch
```
jj p BRANCH
```

# Rebase
```
jj f
jj r SOURCE DESTINATION 
jj p DESTINATION --force
```

# Alias (~/.config/jj/config.toml)
```
n = ["new"]
e = ["edit"]
i = ["git", "init"]
c = ["git", "clone"]
f = ["git", "fetch"]
d = ["desc", "-m"]
p = ["util", "exec", "--", "bash", "-c", "jj b s $1 && jj git push -b $1 $2", ""]
r = ["util", "exec", "--", "bash", "-c", "jj b s $2 && jj rebase -o $1@origin", ""]
```
