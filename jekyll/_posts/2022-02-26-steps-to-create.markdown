---
layout: post
title:  "Creating This Page"
date:   2022-02-26 14:32:27 -0800
categories: first
---


This is the first post to the website.
I'm going to explain the steps that I took to create this website. 

The code used to generate this website is available on [my github page][github]. It was written in markdown, built with [jekyll][jekyll], and hosted on [github][githubio].

# Github setup

1.  First, you'll need a github account. If you don't have one, create one. Make sure to keep track of your username and email.
1.  Create a new repository. Name the repo `username.github.io`, replacing `username` with your username. 
1.  Go to your github settings page and select the tab "SSH and GPG keys". To be able to make "push" changes to this repository from your local machine (using the command line) you'll need to generate an ssh key. If you've previously created an ssh key, you can use that one. Otherwise, run the command and click enter to select the defaults.

        ssh-keygen -t ed25519 -C "your_email@example.com"
 
1.  Run the commands (from your home directory).
         
        eval "$(ssh-agent -s)"
        ssh-add ~/.ssh/id_ed25519
1.  Run the command `cat ~/.ssh/id_ed25519.pub and copy the output. On github, add a new ssh key by clicking the button and pasting the output from the previous command. 
1.  Now, working in a convenient directory of your choosing, run the command

        git clone https://github.com

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




[jekyll]: https://jekyllrb.com/
[githubio]:   https://github.io
[github]: https://github.com/dcdc0/dcdc0.github.io
