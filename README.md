# ghinit
A simple way to perform your initial commit to github

## What is ghinit?
ghinit is a small bashscript created out of the frustration when you have to perform you initial commit, but you are in a hurry.

## Usage
Before using ghinit you need to setup a `Personal access tokens` with the repo access level for your github account and then define the following environment variables:

```
export GH_USERNAME=MyUsername
export GH_ACCESS_TOKEN=1234mytoken123
```

You can now use ghinit simply by running `ghinit` in your project directory.

```
Usage:
ghinit [-cp] [-n reponame] [-d description] [-m commitmsg] [--push]
```