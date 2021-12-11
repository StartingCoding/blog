---
title:  "Ruby Local Install"
layout: post
categories: media
---

![Homebrew, Ruby and RubyGems logo]({{ site.baseurl }}/assets/img/ruby-local-install/ruby-hero.png)

<!-- ruby system-wide vs local-install -->
# TL;DR

Using something system-wide when it's not necessary or when you don't really know what's going on it's not great. `sudo` should be used carefully.


<!-- homebrew install -->
## Homebrew Install

Homebrew is a package manager for macOS.
You can install it going to [brew.sh](https://brew.sh)

<!-- ruby install with homebrew -->
## Install Ruby

Use Homebrew to install Ruby locally

{% highlight terminal %}
brew install ruby
{% endhighlight %}

<!-- shell setup -->
## Shell Setup

In order to use use Ruby locally, the shell needs to have the environment configured to point to the right path and not using the pre-installed Ruby.

Set up a `~/.zshrc` (on zsh shell of course) file on your user folder.

{% highlight terminal %}
export PATH=/usr/local/opt/ruby/bin:$PATH
export PATH=/usr/local/lib/ruby/gems/X.X.0/bin:$PATH
{% endhighlight %}

The first line is for Ruby, the second one is for RubyGems and at the end of it you need to replace the X.X. with the Ruby version you installed before.

<!-- check everything works  -->
## Last Checks

Check if you're running the right Ruby with `which ruby` check with `gem env` if all of your paths are correct.

<!-- jekyll install -->
## Install Jekyll

Now installing Jekyll is just as easy as installing a RubyGems with the local Ruby using `gem install bundler jekyll`.

# > Other Resources:
- / Homebrew / [https://brew.sh](https://brew.sh)
- / Ruby / [https://www.ruby-lang.org/en/](https://www.ruby-lang.org/en/)
- / RubyGems / [https://rubygems.org](https://rubygems.org)
- / Jekyll-Docs-Installation / [https://jekyllrb.com/docs/installation/macos/](https://jekyllrb.com/docs/installation/macos/)
- / RubyGems-Docs-Basics / [https://guides.rubygems.org/rubygems-basics/](https://guides.rubygems.org/rubygems-basics/)
- / Ruby-Local-Installation-Guide / [https://mac.install.guide/ruby/index.html](https://mac.install.guide/ruby/index.html)
- / RubyGems-Local-Installation-Guide / [https://www.moncefbelyamani.com/the-definitive-guide-to-installing-ruby-gems-on-a-mac/#homebrew-ruby](https://www.moncefbelyamani.com/the-definitive-guide-to-installing-ruby-gems-on-a-mac/#homebrew-ruby)
- / Ruby-Local-Uninstall-Guide / [https://mac.install.guide/ruby/9.html](https://mac.install.guide/ruby/9.html)