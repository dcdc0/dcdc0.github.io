# dcdc0.github.io

A basic personal website.

### Setup steps

1. Create a github account. Make sure to keep track of your username and email.
2. Create a new repository. Name the new repo username.github.io
3. Go to your github settings page -> Developer settings -> Personal access tokens and create a new token. You can give it a name like "mycomputer". Check the "repo" box to give it access to your repos. You can set it to expire after 90 days. After you create the token, it should display the token, a long sequence of letters and numbers. Copy this--- you will need it later.
4. On your latop, open terminal.
5. Type the command `git clone https://github.com/username/username.github.io`
6. Enter the repo with the command `cd username.github.io/`
7. Add a text file with the name `index.html` and contents `Hello world.`
8. Making sure that you're in the correct directory, enter the command ```git add index.html```
9. `git commit -am "Initial commit"`
10. `git push origin main`
11. You may need to specify your git user info following the prompts shown. Rerun the previous command if necessary. 
12. You'll have to type in your username. When it prompts for a password, paste your access token.
13. Check out your website at `https://username.github.io`
