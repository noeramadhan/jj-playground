# Init
```
jj i
jj cl URL

jj config set --user user.name "Your Name"
jj config set --user user.email "your@email.com"
```

# Changes
```
jj d "MESSAGE"
jj n
jj n BASE
jj e TARGET
jj c "MESSAGE"
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
d = ["desc", "-m"]
c = ["ci", "-m"]
i = ["git", "init"]
cl = ["git", "clone"]
f = ["git", "fetch"]
p = ["util", "exec", "--", "bash", "-c", "jj b s $1 && jj git push -b $1 $2", ""]
r = ["util", "exec", "--", "bash", "-c", "jj b s $2 && jj rebase -o $1@origin", ""]
```
