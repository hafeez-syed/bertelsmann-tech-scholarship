# Git

## Commands

```bash
$ git --verison
```


```bash
$ git init
```

```bash
$ git clone <repo URL>
```

```bash
$ git add .
```

```bash
$ git add <file-name>
```

```bash
$ git commit -m "commit message"
```

```bash
$ git status
```

```bash
$ git log
```

```bash
$ git log --oneline
```

```bash
$ git log --stat
```

```bash
$ git log -p
```

```bash
$ git log -p --stat
```

```bash
$ git log -p -w
```

```bash
$ git log -p <SHA>
```

```bash
$ git show <first 7 characters of SHA> --stat
```
## Good commit messages

### Do
+ do keep the message short (less than 60-ish characters)
+ do explain what the commit does (not how or why!)

### Do not
+ do not explain why the changes are made (more on this below)
+ do not explain how the changes are made (that's what git log -p is for!)
+ do not use the word "and"
    - if you have to use "and", your commit message is probably doing too many changes - break the changes into separate commits
    - e.g. "make the background color pink and increase the size of the sidebar"

### Globbing Crash Course
Let's say that you add 50 images to your project, but want Git to ignore all of them. Does this mean you have to list each and every filename in the .gitignore file? Oh gosh no, that would be crazy! Instead, you can use a concept called globbing.

Globbing lets you use special characters to match patterns/characters. In the .gitignore file, you can use the following:

+ blank lines can be used for spacing
+ ` # ` - marks line as a comment
+ ` * ` - matches 0 or more characters
+ ` ? ` - matches 1 character
+ ` [abc] ` - matches a, b, _or_ c
+ ` ** ` - matches nested directories - ` a/**/z ` matches
    - a/z
    - a/b/z
    - a/b/c/z
