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

After an update of git sometimes the system asks for verification of the key chain on each upload to the repos. To solve the problem:

1. Open <b>Keychain Access</b> ( <i>Applications/Utilities/Keychain Access</i>)

2. Select <b>Keychains -> login<b> and <b>Category -> Passwords</b>

3. Type <b>github.com</b> in the search box and find <b>Internet Password</b>. Right click and Delete. If there are more than one then check them before deleting.

4. Go back to the Terminal and type:

```
git config --global credential.helper osxkeychain

```

On the next upload the system will ask for the git username and the git password.
