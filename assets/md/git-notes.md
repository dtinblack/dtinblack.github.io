---
layout: page
title: Git Notes
modified: 2020-07-26
---

The following notes assume that Git is installed.

Check the version of Git against the [latest version](https://git-scm.com/downloads)

```
git --version

brew update && brew upgrade

```

The following Git commands are useful:


List the files that are bing tracked

```

git ls-tree -r master --name-only

```


Delete files that are being tracked ( and remove from the repo )

```
git rm my-file.txt

git rm -r my-folder

```

Update the website ( and upload to repo )

```
git add .

git commit -m "some text describing the change"

git push -u origin master

```

Check the information stored in the osxkeychain used by github ( security )

```
git config -l

```
