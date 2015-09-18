---
layout: post
title:  "Install Ruby/RVM/Jekyll and more"
date:   2015-07-07 20:11:00 -0400
categories: ruby, ubuntu, jekyll
---

## To install rvm and Ruby

# 1. Get the public key

	gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3

Note: In Fedora 22 for some reason this was throwing an error, But fortunately it also shows some fix in that error message.

# 2. Install ruby 2.0.0
 
	curl -sSL https://get.rvm.io | bash -s stable --ruby

	rvm get stable
	rvm install 2.0.0
	rvm use 2.0.0
	rvm rubygems latest
	ruby --version

# 3. Install Jekyll

	sudo gem install jekyll

# 4. Install NodeJS (if you get the error)

	sudo apt-get install nodejs

# 5. Lauch jekyll server

	jekyll serve --watch -baseurl ""


# Reference: [https://rvm.io/rvm/install](https://rvm.io/rvm/install)
