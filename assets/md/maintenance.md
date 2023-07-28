---
layout: page
title: Maintenance of Jekyll
modified: 2020-07-26
---

The following notes are used to update any parts of Jekyll's Technology Stack on a Mac OS.  

[Jekyll](https://jekyllrb.com/docs/ruby-101/) is written in [Ruby](https://www.ruby-lang.org/en/) and uses the [Liquid](https://shopify.dev/api/liquid) template language created by [Shopify](https://www.shopify.co.uk/partners/blog/115244038-an-overview-of-liquid-shopifys-templating-language). Liquid is also written in Ruby.

[cloudcannon](https://cloudcannon.com/) have a produced a step-by-step [tutorial](https://cloudcannon.com/tutorials/jekyll-tutorial/), with examples, that explains the Jekyll file structure and how to use Liquid.

For information about installing Jekyll then see [Jekyll on macOS](https://jekyllrb.com/docs/installation/macos/).


All of the following commands are used in a Terminal.

<b>Operating System</b>

Check the current version of the operating system. The information will be used to check which package versions can safely be used to update Jekyll.


<b>Xcode Command Tools</b>






<b>Development Tools</b>


<i>Check the difference between clang and gcc [How to install GCC on Mac](https://osxdaily.com/2023/05/02/how-install-gcc-mac/) - see also [Switch from “Apple clang” to “Homebrew clang” in VS code configuration](https://discourse.llvm.org/t/switch-from-apple-clang-to-homebrew-clang-in-vs-code-configuration/63314) to make sure that the latest version is being used. Also check the LLVM Compiler [How to check the LLVM compiler version Xcode is using?](https://stackoverflow.com/questions/14186490/how-to-check-the-llvm-compiler-version-xcode-is-using)</i>

<b>Ruby</b>

See [Installation Requirments](https://jekyllrb.com/docs/installation/)

```
ruby --version

```

Using rvm, install any new version of ruby using the following:

```

rvm list             #=> Check the installed versions of Ruby

rvm install 2.0.0-p0 #=> This will install Ruby 2.0.0

rvm --default use 2.0.0

```

* RubyGems

[RubyGem Commands](https://sourabhbajaj.com/mac-setup/Ruby/RubyGems.html)

```
gem --version
```

To update the system then:

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
