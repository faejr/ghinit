# ghinit
A simple way to perform your initial commit to github

## What is ghinit?
ghinit is a small bashscript created out of the frustration when you have to perform you initial commit, but you are in a hurry.

## Usage
Before using ghinit you need to setup a [Personal access tokens](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/) with the repo access level for your github account and then define the following environment variables:

```
export GH_USERNAME=MyUsername
export GH_ACCESS_TOKEN=1234mytoken123
```

If you prefer not adding your token to your environment variables simply create a file called `.ghinit` in your home directory containing your information
```
GH_USERNAME=MyUsername
GH_ACCESS_TOKEN=1234mytoken123
```

You can now use ghinit simply by running `ghinit` in your project directory.

```
Usage:
ghinit [-cp] [-n reponame] [-d description] [-m commitmsg] [--push]
```

Example output:
```
ghinit ❯ ghinit -d "A simple way to perform your initial commit to github with a single terminal command" -c --push
Setting up github repo ghinit...
Initialized empty Git repository in /Users/daniel/dev/ghinit/.git/
.gitignore doesn't exist, would you still like to commit add all? [Y/n]y
Adding all files...
Commit message (Leave blank for default):
Creating initial commit...
[master (root-commit) 0991a9e] Init commit
 2 files changed, 150 insertions(+)
 create mode 100644 README.md
 create mode 100755 ghinit
Counting objects: 4, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 1.77 KiB | 1.77 MiB/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To github.com:LiljebergXYZ/ghinit.git
 * [new branch]      master -> master
Finished!
```
