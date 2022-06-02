---
layout: page
title: Jekyll Notes
modified: 2020-07-26
---

### Technology Stack

[Jekyll](https://jekyllrb.com/docs/ruby-101/) is written in [Ruby](https://www.ruby-lang.org/en/) and uses the [Liquid](https://shopify.dev/api/liquid) template language created by [Shopify](https://www.shopify.co.uk/partners/blog/115244038-an-overview-of-liquid-shopifys-templating-language). Liquid is written in Ruby.

[Grunt](https://gruntjs.com/) is a task runner that automates repetitive tasks. It is written in [Nodejs](https://nodejs.org/en/) and utilises Node packages. Nodejs is written in C++.  It can be used as a wrapper around a Jekyll website during its development to automate many tasks ip particular rebuilding the site after editing.


### Tutorials

[cloudcannon](https://cloudcannon.com/) have a produced a step-by-step [tutorial](https://cloudcannon.com/community/learn/jekyll-tutorial/), with examples, that explains the Jekyll file structure and how to use Liquid.


### Footnotes

Small pieces of code used to understand some of the underlying technology used by Jekyll.

##### YAML

Although only a few lines of code it shows how to read a YAML file. 

some.yaml - file containing some data in YAML format.

{% highlight YAML %}
---
javascripts:
- fo_global:
  - lazyload-min
  - holla-min

{% endhighlight %}

read_yaml.rb  - reading the YAML file written in Ruby.

{% highlight YAML %}
require 'yaml'

stuff = YAML.load_file('some.ymal')

puts stuff.inspect

#=> prints '{"javascripts"=>[{"fo_global"=>["lazyload-min", "holla-min"]}]}' to STDOUT.

{% endhighlight %}
