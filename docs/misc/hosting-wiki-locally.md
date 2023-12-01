---
layout: default
title: Hosting Wiki locally
parent: Misc
nav_order: 7
---

# Requirements #   
The following list has to be done only once.  

1. Install the newest version of Ruby. Needs to have "devkit" in the asset name: [Ruby releases](https://github.com/oneclick/rubyinstaller2/releases)
2. Clone Wiki-Repo somewhere and open visual studio code
3. Run in the terminal: `gem install jekyll bundler`
4. (Check that your terminal is in the folder path of the wiki)  
Run in the terminal: `bundle install`

# Each run #  
The following list has to be done each time.  

1. (Check that your terminal is in the folder path of the wiki)   
Run in the terminal: `bundle exec jekyll serve`
2. After some preparation time (up to 30 minutes) it will start locally

# Result # 
Now the wiki can be accessed locally via [http://127.0.0.1:4000/riftbreaker-wiki/](http://127.0.0.1:4000/riftbreaker-wiki/)