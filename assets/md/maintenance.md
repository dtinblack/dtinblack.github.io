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

- update the bundles used by the application

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
