# Save and exit
```sh
:wq
```

# Exit without saving
```sh
:q!
```

# Send to background and return from terminal
```sh
:suspend
```
to return back to vim
```sh
fg
```

# Delete lines
```sh
dd
#dd
```
*#* - count of lines to delete

# Enable line numbers
```sh
:set number
```

# Go to first line
```sh
gg
```

# Go to end of the file
```sh
G
```

# Copy
```sh
y
```

# Cut
```sh
d
```

# Paste
```sh
P
```

# Undo
```sh
u
```

# Redo
```sh
ctrl+r
```

# Search
```sh
/yourtext + Enter
```
*n* - Next
*N* - Previous

# Replace
```sh
:%s/yourtext/replacement/g(c)
```
*c* is optional, used to enable confirmation

# Add/remove tabs 
```sh
> or <
```

# Comment lines
1. *v* to enter Visual mode
2. Select by arrows
```sh
:norm i#
```

# Uncomment lines
1. *v* to enter Visual mode
2. Select by arrows
```sh
:norm x
```