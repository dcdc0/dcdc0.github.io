---
layout: post
title:  "Creating your first page"
date:   2022-02-26 14:32:27 -0800
categories: first
usemathjax: true
---


This is the first post to a new website.
I'm going to explain the steps that I took to create this website. 

The code used to generate this website is available on [my github page][github]. It was written in markdown, built with [jekyll][jekyll], and hosted on [github][githubio].

## Setup

# Github

1.  First, you'll need a github account. If you don't have one, create one. Make sure to keep track of your username and email.
1.  Create a new repository. Name the repo `username.github.io`, replacing `username` with your username. 
1.  Go to your github settings page and select the tab "SSH and GPG keys". To be able to make "push" changes to this repository from your local machine (using the command line) you'll need to generate an ssh key. If you've previously created an ssh key, you can use that one. Otherwise, run the command and click enter to select the defaults.

        ssh-keygen -t ed25519 -C "your_email@example.com"
 
1.  Run the commands (from your home directory).
         
        eval "$(ssh-agent -s)"
        ssh-add ~/.ssh/id_ed25519
1.  Run the command `cat ~/.ssh/id_ed25519.pub` and copy the output. On github, add a new ssh key by clicking the button and pasting the output from the previous command. 
1. If you've just installed git, you'll need to set your identity. (This shows up in logs and is publicly available, so use a public-facing email address.)

        git config --global user.name "YOUR NAME"
        git config --global user.email "you_email@example.com"

1.  Now, working in a convenient directory of your choosing where you'll store the actual project, run the command

            git clone https://github.com/username/username.github.io

1. Enter that directory. Create a text file named `index.html` and give it the contents 'Hello, World.' 
1. You've now made a tiny website. To check it out, you'll need to push the changes to github. To do this, we'll first need to configure git to use your ssh key. To do so, run 

        git remote set-url origin git@github.com:<username>/<username>.github.io.git


1.  Now, we need to tell git that you want to publish the work you've done. First, tell git to track the file with the command 

        git add index.html

    then tell git that you're ready to publish with the command

        git commit -am "Initial commit."

1.  Now, you can push your changes with the command

        git push

1. Now, go to `username.github.io` and see your first webpage.


# Install Jekyll

Your webpage exists now, but it's not very interesting. A fairly simple way to generate more interesting websites is using Jekyll. 

1.  Jekyll requires the Ruby language. Check that Ruby is installed by running

        ruby -v

1.   If you already have Ruby, great! Otherwise, follow instructions for your operating system [here][ruby-install].
1.  After you have Ruby installed, you will also need Bundler to manage other dependencies. 

        gem install bundler jekyll

    The `gem` command should have come with your Ruby installation. If it's not there, try reopening your terminal.
If you don't have `sudo` privileges, you can try

        gem install --user-install bundler jekyll

1.  If you have trouble, you can then follow the guide [here][jekyll-install] for your operating system.

# Using Jekyll to make a website

Once you have Jekyll installed, use your terminal to navigate to your `username.github.io` repo. 
You can run the command

    jekyll new mysite

This will create the necessary files in the `mysite` directory. You can start exploring the files in the `mysite/_post` directory and the `mysite/_config.yml` files. From the mysite directory, you can run 

        bundle exec jekyll serve

and then visit the local site [127.0.0.1:4000][local]. 
Try adding new files to the `_post` folder, but try to follow the provided templates. When you want to inspect your changes, just run the previous command and visit the local page. This webpage isn't available on the internet yet, so feel free to make changes. 



[local]: 127.0.0.1:4000
[ruby-install]: https://www.ruby-lang.org/en/documentation/installation/
[jekyll]: https://jekyllrb.com/
[jekyll-install]: https://jekyllrb.com/docs/installation/
[githubio]:   https://github.io
[github]: https://github.com/dcdc0/dcdc0.github.io
