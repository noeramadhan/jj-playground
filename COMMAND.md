# Init
```
jj gi
jj gc URL

jj config set --user user.name "Your Name"
jj config set --user user.email "your@email.com"
```

# Changes, Starts
```
jj n
jj n BASE
jj e TARGET
```

# Changes, Ends
```
jj d "MESSAGE"
jj c "MESSAGE"
```

# Changes, Gone
```
jj a TARGET
jj u
```

# Create and Push Branch
```
jj p BRANCH
```

# Rebase
```
jj r SOURCE DESTINATION 
```

# Alias & Some Config (~/.config/jj/config.toml)
```
[templates]
log = 'format_short_id(change_id) ++ " " ++ committer.email() ++ " " ++ committer.timestamp().format("%Y-%m-%d %H:%M") ++ " " ++ description.first_line() ++ " " ++ separate(" ", local_bookmarks, remote_bookmarks) ++ "\n"'

[aliases]
a = ["abandon"]
u = ["undo"]
n = ["new"]
e = ["edit"]
d = ["desc", "-m"]
c = ["ci", "-m"]
gi = ["git", "init"]
gc = ["git", "clone"]
gf = ["git", "fetch"]
gp = ["git", "push", "-b"]
p = ["util", "exec", "--", "bash", "-c", "jj b s $1 && jj git push -b $1", ""]
r = ["util", "exec", "--", "bash", "-c", "jj git fetch && jj b s $2 && jj rebase -o $1@origin && jj git push -b $2", ""]
```
