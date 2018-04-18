---
layout: default
---

# Jekyll

## ubuntu

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


<https://guides.github.com/features/mastering-markdown/>

<https://jekyllrb.com/>