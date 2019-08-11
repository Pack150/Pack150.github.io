Pack 379, Arlington, TX
============

## Development
**tldr:** Run a current version of Ruby with `rbenv`, use the `bundler` gem to install
dependencies and run `jekyll serve`.

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
$ jekyll serve
```
## Upstream Projects

This is based on the [Scoutpack Wordpress Theme](http://handsomeweb.com/cubscouts/),
converted to a [Jekyll](http://jekyllrb.com/) site by [Thaddeus Quintin](http://github.com/quiddle)
for [Pack 150](http://pack150.org).

Fork [this repository](https://github.com/pack379/pack379.github.io/fork) 
or the [original Pack 150 repository](https://github.com/Pack150/Pack150.github.io/fork) if you like!

## Author

**Thaddeus Quintin**
- <https://github.com/Pack150/Pack150.github.io>
- <https://github.com/quiddle>

**Cameron King**
- <https://github.com/pack379/pack379.github.io>
- <https://github.com/ckxng>

and others, see changelog.

## License

Unless specified otherwise, this project is licensed under the [Creative Commons Attribution 4.0 International License](LICENSE.md).
