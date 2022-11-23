# git-Shortcut
> Custom git command to save/execute shortcuts on a per repo basis.

## Table of Contents

1. [Install Instructions](#install-instructions)
2. [Usage](#usage)
    1. [Help](#help)
    2. [Create Shortcuts](#create-shortcuts)
    3. [Run Shortcuts](#run-shortcuts)
    4. [Edit/Delete/List](#edit-shortcuts)
3. [Contributing](#contributing)
4. [License](#license)

## Install Instructions

To ensure this script functions for each new bash shell:
1. Save git-shortcut to (for example) /your-directory/git-custom-commands
2. cd ~/
3. touch .bash_profile
4. Edit .bash_profile and add "export PATH=$PATH:/your-directory/git-custom-commands"

## Usage

#### Help
```bash
$ git shortuct ?
```

#### Create Shortcuts
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

#### Run Shortcuts
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

#### Edit Shortcuts
```bash
# List and select shortcut to edit
$ git shortcut -e
```

#### Delete Shortcuts
```bash
# List and select shortcut to delete
$ git shortcut -d
```

#### List Shortcuts
```bash
# Only list shortcuts
$ git shortcut -l
```

## Contributing

Pull requests are welcome! For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to check your modifications with [ShellCheck](https://github.com/koalaman/shellcheck).

## License

[MIT](https://choosealicense.com/licenses/mit/)
