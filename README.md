Pack 150, Chagrin Falls, Ohio
============

## Development
**tldr:** Run a current version of Ruby, install the `bundler` gem and run `jekyll` via `bundle exec`.

This site runs on Github Pages, which uses [Jekyll](http://jekyllrb.com). Jekyll is a Ruby gem.
Best way to start installing things on a Mac is with [Homebrew](http://brew.sh). Once homebrew
is installed, install `rbenv` and `ruby-build` to manage your version of Ruby.
```
$ brew update
$ brew install rbenv ruby-build
```
This installs `rbenv`. To setup your shell to use `rbenv`'s Ruby, place
`eval "$(rbenv init -)"` in your shell files. Check the (instructions)[https://github.com/sstephenson/rbenv#homebrew-on-mac-os-x]
for more info.

Now, you need to install the correct version of Ruby. From the site directory, run the following.
```
$ rbenv install `cat .ruby-version`
$ rbenv rehash
```
You can double check the version by doing one of the following:
```
$ ruby -v
$ rvenv versions
```

Now, install `bundler`, a ruby gem/package manager. Install `bundler` and the necessary gems, including `jekyll` by doing:
```
$ gem install bundler
$ bundle install
```

Bundler uses the `Gemfile` and `Gemfile.lock` files to list dependencies.

Done! You can run the site locally with the following command:
```
$ bundle exec jekyll serve
```


This is is based on [Solid-Jekyll](https://github.com/st4ple/solid-jekyll), a [Jekyll](http://jekyllrb.com/) port of the [Solid theme](http://www.blacktie.co/2014/05/solid-multipurpose-theme/) by [blacktie.co](http://www.blacktie.co/).

[Fork this repository](https://github.com/Pack150/Pack150.github.io/fork) if you like!

####Customize
Most general settings and data like site name, colors, address, etc. can be configured and changed right in the main config file: `/_config.yml`
The content of the Home page can be changed here: `/home.html`
The content of the About page can be changed here: `/about.html`
The content of the Portfolio page can be changed here:`/portfolio.html`
The content of the Contact page can be changed here:`/contact.html`
####Add content
Delete the demo content and publish your own content.
#####Blog post
Create a Blog post by creating a file called `yyyy-mm-dd-name-of-post-like-this.markdown` in the `/_posts/blog/` directory with the following template:
```markdown
---
layout: post          #important: don't change this
title: "Name of post like this"
date: yyyy-mm-dd hh:mm:ss
author: Name
categories:
- blog                #important: leave this here
- category1
- category2
- ...
img: post01.jpg       #place image (850x450) with this name in /assets/img/blog/
thumb: thumb01.jpg    #place thumbnail (70x70) with this name in /assets/img/blog/thumbs/
---
This text will appear in the excerpt "post preview" on the Blog page that lists all the posts.
<!--more-->
This text will not be shown in the excerpt because it is after the excerpt separator.
```
#####Project post
Create a Project post to go in your Portfolio by creating a file called `yyyy-mm-dd-name-of-the-project.markdown` in the `/_posts/project/` directory with the following template:
```markdown
---
layout: project       #important: don't change this
title:  "Name of the project"
date: yyyy-mm-dd hh:mm:ss
author: Name
categories:
- project             #important: leave this here
img: portfolio_10.jpg #place image (600x450) with this name in /assets/img/project/
thumb: thumb02.jpg
carousel:
- single01.jpg        #place image (1280x600) with this name in /assets/img/project/carousel/
- single02.jpg
- ...
client: Company XY
website: http://www.internet.com
---
####This is a heading
This is a regular paragraph. Write as much as you like.
```
#####Question entry
Create a Question entry (that is listed in the Frequently Asked section on the Home page) in this directory by creating a file called `yyyy-mm-dd-do-i-have-a-question.markdown` in the `/_posts/project/` directory with the following template:
```markdown
---
layout: question
title:  "Do I have a question?"
date: yyyy-mm-dd hh:mm:ss
author: First Last
categories:
- question            #important: leave this here
---
####Can I use this theme for my website?
Of course you can!
```
####Publish
To publish with [GitHub Pages](https://pages.github.com/), simply create a branch called `gh-pages`in your repository. GitHub will build your site automatically and publish it at `http://yourusername.github.io/repositoryname/`.
If there are problems with loading assets like CSS files and images, make sure that the `baseurl` in the `_config.yml`is set correctly (it should say `/repositoryname`).

If you want to host your website somewhere else than GitHub (or just would like to customize and build your site locally), please check out the [Jekyll documentation](http://jekyllrb.com/).
