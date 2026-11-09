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

To remove any gem not in the bundle:

```

bundle clean --force

```

<b>Solved Maintenance Problems</b>

[Git push failure while pushing a large respository code](https://stackoverflow.com/questions/62753648/git-push-failure-while-pushing-a-large-respository-of-code). Also, see [How To Fix A Stuck GitHub Push](https://dev.to/dev_neil_a/how-to-clear-a-stuck-github-push-h57).

[Ruby native extensions fail to build after macOS upgrade](https://stackoverflow.com/questions/80012616/ruby-native-extensions-fail-to-build-after-macos-upgrade):

The errors were from the CLT version of clang. In general, there were conflicts between various development tools installed via Homebrew and those provided by the CLT. I therefore installed llvm using Homebrew:

```
brew install llvm

```

The environment for interactive shells was modified, e.g. ~/.zshrc, to make sure that everything was pointing to the Homebrew directories:

```
if [ -d "/opt/homebrew/opt/ruby/bin" ]; then
  export PATH=/opt/homebrew/opt/ruby/bin:$PATH
  export PATH=`gem environment gemdir`/bin:$PATH
fi

export PATH="/opt/homebrew/bin:$PATH"

# LLVM installed by Homebrew

export PATH="/opt/homebrew/opt/llvm/bin:$PATH"

export LDFLAGS=-L/opt/homebrew/opt/llvm/lib

export CPPFLAGS=-I/opt/homebrew/opt/llvm/include

export CMAKE_PREFIX_PATH=/opt/homebrew/opt/llvm

```

After making these changes, the native extensions for the gems compiled successfully and were installed.
