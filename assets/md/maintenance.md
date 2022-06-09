---
layout: page
title: Maintenance Steps
modified: 2020-07-26
---

Check the following software is current:

* Xcode and command tools

* Ruby

```
ruby --version

```

Using rvm, you can install any new version of ruby using the following :

```

rvm list             #=> Check the installed versions of Ruby
 
rvm install 2.0.0-p0 #=> This will install Ruby 2.0.0

rvm --default use 2.0.0

```

* RubyGems

```
gem --version
```

If it needs updating then:

```
gem update --system
```

* [Installing Bundler 2](https://bundler.io/guides/bundler_2_upgrade.html)

```
gem install bundler

bundle check

bundle update --bundler

```

- Update the bundles used by the application

```

bundle update

```

* [Git](https://medium.com/@katopz/how-to-upgrade-git-ff00ea12be18)

Assuming that Git is already installed.

```
git --version

brew update && brew upgrade

```

Update Grunt files in package.json ( check the version of npm )

```

npm outdated

npm update

```

Useful Git commands:

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
