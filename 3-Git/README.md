# Git

## Commands

> `git` version check

```bash
$ git --verison
```

> start a new git repository

```bash
$ git init
```

> copy or clone an existing git repository

```bash
$ git clone <repo URL>
```

> add all files i.e ` . ` in the current directory and all it's child directories to staging

```bash
$ git add .
```

> add a file to staging

```bash
$ git add </file-path/file-name>
```

> add a commit add files to the local branch

```bash
$ git commit -m "commit message"
```

> display the current status of the branch. New files, deleted files or updated files are listed

```bash
$ git status
```

> it displays the details of the committed files i.e date, author, commit message etc.


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
$ git log --decorate
```

```bash
$ git show <first 7 characters of SHA> --stat
```

```bash
$ git tag -a v1.0
```

```bash
$ git tag
```

```bash
$ git tag -d v1.0
```

```bash
$ git tag -a v1.0 <SHA>
```

```bash
$ git branch sidebar
```

```bash
$ git checkout sidebar
```

```bash
$ git checkout -b sidebar
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
