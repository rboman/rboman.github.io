---
layout: default
---

# Jekyll

This site is built with [github pages](https://pages.github.com/) which is based on [jekyll](https://jekyllrb.com/), a set of ruby modules ("gems") for the creation of static websites and blogs from templates ([liquid](https://github.com/Shopify/liquid/wiki)) and [markdown](https://daringfireball.net/projects/markdown/)/html5 files. 


## Ubuntu

```
sudo apt-get install ruby
sudo gem update
sudo gem install jekyll bundler 
sudo chmod -R a+rX /var/lib/gems/
sudo chmod -R a+rX /usr/local/bin/
cd ~/dev/rboman.github.io
sudo bundle install 
sudo chmod -R a+rX /var/lib/gems/
sudo chmod -R a+rX /usr/local/bin/
sudo rm Gemfile.lock
bundle exec jekyll serve
```
If `_config.yml` has changed, the site can be fully rebuit using:
```
bundle exec jekyll build
```


## Windows
I haven't used <https://jekyllrb.com/docs/windows/> but [MSYS2](https://www.msys2.org/). MYSYS provides me with a similar development environment as above:

- install [MSYS2](https://www.msys2.org/) 64 bits.
- start `msys2_shell.cmd` and run `pacman -Suy` which updates everything. I had to do it twice (?)
- start `mingw64.exe` and install those packages:
  ```
  pacman -S mingw64/mingw-w64-x86_64-ruby 
  pacman -S mingw64/mingw-w64-x86_64-gcc  
  pacman -S make                             
  ```
- install the `jekyll` and `bundler` gems:
  ```
  gem install jekyll bundler
  ```
- then go to the source folder of the website and use bundler to install all the gems that are required for the site (listed in `Gemfile`)
  ```
  cd /f/dev/rboman.github.io/
  bundle install  
  ```
- generate the site and serve it at <http://localhost:4000>
  ```
  bundle exec jekyll serve
  ```

It seems that `ctrl-c` does not kill the webserver. Use the taskmanager to kill it.


## Tutorials
* <https://24ways.org/2013/get-started-with-github-pages/>
* <https://jekyllrb.com/>
* <http://jmcglone.com/guides/github-pages/>
* <https://jekyllrb.com/docs/github-pages/>
* <https://github.com/vicrucann/vicrucann.github.io>
* <http://pixelcog.com/blog/2013/jekyll-from-scratch-introduction/>
* <http://pixelcog.com/blog/2013/jekyll-from-scratch-core-architecture/>
* <http://pixelcog.com/blog/2013/jekyll-from-scratch-extending-jekyll/>
* <https://jekyllrb.com/tutorials/orderofinterpretation/>


## Github pages

* <https://help.github.com/articles/using-jekyll-as-a-static-site-generator-with-github-pages/>

## Sites
* <http://lea.verou.me/>
* <https://github.com/adam-p/adam-p.github.com>
* <http://blog.davidebbo.com/2014/11/using-issues-for-github-pages-screenshots.html>
* <http://dirk.eddelbuettel.com/blog/>

## Themes
* <https://github.com/pages-themes/hacker>
* <https://mmistakes.github.io/so-simple-theme/>

## Markdown/YAML
* <https://guides.github.com/features/mastering-markdown/>
* [Markdown syntax](http://packetlife.net/media/library/16/Markdown.pdf)
* [YAML](https://en.wikipedia.org/wiki/YAML#Basic_components)
* [Learn YAML](https://learnxinyminutes.com/docs/yaml/)
* [SASS](https://sass-lang.com/guide)
