---
layout: page
title: Maintenance of Jekyll
modified: 2020-07-26
---

The following notes are used to update any parts of Jekyll's [technology stack](https://www.mongodb.com/basics/technology-stack) on a Mac OS.  

[Jekyll](https://jekyllrb.com/docs/ruby-101/) is written in [Ruby](https://www.ruby-lang.org/en/) and uses the [Liquid](https://shopify.dev/api/liquid) template language created by [Shopify](https://www.shopify.co.uk/partners/blog/115244038-an-overview-of-liquid-shopifys-templating-language). Liquid is also written in Ruby.

[cloudcannon](https://cloudcannon.com/) have a produced a step-by-step [tutorial](https://cloudcannon.com/tutorials/jekyll-tutorial/), with examples, that explains the Jekyll file structure and how to use Liquid.

The notes assume that Jekyll has been installed and is running ( for information about installing Jekyll then see [Jekyll on macOS](https://jekyllrb.com/docs/installation/macos/) ).

All of the following commands are used in a Terminal.

<b>Operating System</b>

Get the current version of the operating system. In this case it is Mac OS. The information will be used to check the package versions that can safely be used to update Jekyll.

<b>Xcode Command Tools</b>

Check the version of [Xcode Command Tools that are available](https://developer.apple.com/xcode/resources/) then check the installed version:

```
/Applications/Xcode.app/Contents/Developer/usr/bin/xcodebuild -version #=> Check Xcode version


pkgutil --pkg-info=com.apple.pkg.CLTools_Executables  #=> Check installed version

```

If the Xcode Command Tools need to be updated then the best way is to delete the old version and then install the latest version:

```
softwareupdate --list                             #=> Check what software is available

xcode-select -p                                   #=> Find the CommandLineTools folder

sudo rm -rf /Library/Developer/CommandLineTools   #=> Delete the old version

xcode-select --install

```

<b>[Homebrew](https://brew.sh/)</b>

Check the installed version agains the latest [version of Homebrew](https://github.com/Homebrew/brew/releases/tag/4.1.2):

```
brew --version    #=> Check the installed versions of Homebrew

brew update

brew upgrade       #=> Upgrade packages


brew doctor       #=> Check the status of the installed version

```


<b>[Ruby](https://www.ruby-lang.org/en/about/)</b>

[Chruby](https://formulae.brew.sh/formula/chruby) is a Ruby version manager used with tjis installation. To check the latest version of Ruby:

```
ruby-install ruby

```

Check the installed version of Ruby:

```
ruby --version

ruby-install 3.1.4       #=> Install a specific version

```

If upgrading the version of Ruby check the that appropriate sections of the shell are updated ( in this case ~/.zrhc ).

<b>[RubyGem](https://jekyllrb.com/docs/ruby-101/#gems)</b>

RubyGems are part of the Ruby installation.


[RubyGem Commands](https://sourabhbajaj.com/mac-setup/Ruby/RubyGems.html)

```
gem --version
```

To update the system then:

```
gem update --system
```

<b>[Bundler](https://rubygems.org/gems/bundler/versions/2.0.2)</b>

Check the installed version of Bundler with the [latest version](https://rubygems.org/gems/bundler/versions/2.0.2):

```
bundle --version


bundle update --bundler   #=> Upgrade to the latest version of Bundler

```

Check the gem files and if required update them:

```
bundle check

bundle update jekyll       #=> Update a specific gem

bundle update

```
