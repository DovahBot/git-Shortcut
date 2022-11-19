# git-Shortcut

Custom git command to save/execute shortcuts.<br>
Shortcuts are saved on a per repo basis.

<br>

## 'Install' Instructions

To ensure this script functions for each new bash shell:
1. Save git-shortcut to (for example) /your-directory/git-custom-commands
2. cd ~/
3. touch .bash_profile
4. Edit .bash_profile and add "export PATH=$PATH:/your-directory/git-custom-commands"

<br>

## How To Use

### Help
```bash
$ git shortuct ?
```

### Create Shortcuts
```bash
# Create a simple shortcut
$ git shortuct -n "git status"
Shortcut added as #1

# Create and instantly run any shortcut
$ git shortuct -n -r "git status"
Shortcut added as #1
... git status runs

# Create shortcut with runtime parameters
# When running this shortcut, you can provide any value for <msg>
$ git shortuct -n "git commit -m <msg>"
Shortcut added as #2
```

### Run Shortcuts
```bash
# List shortcuts first
$ git shortcut
Saved shortcuts:

1: git status
2: git commit -m <msg>

Enter shortcut number(s) to run (space delimited) [or nothing to cancel]:

# Run shortcut(s) immediately
$ git shortcut 1 2
... git status runs
... git commit -m <msg> runs

# Running a shortcut with runtime params
$ git shortcut 2
git commit -m <msg>          [Ctrl+C to cancel | nothing to exclude param]
Enter value for param <msg>:  Init commit
... git commit -m "Init commit" runs
```

### Edit Shortcuts
```bash
# List and select shortcut to edit
$ git shortcut -e
```

### Delete Shortcuts
```bash
# List and select shortcut to delete
$ git shortcut -d
```

### List Shortcuts
```bash
# Only list shortcuts
$ git shortcut -l
```