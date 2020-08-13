# initial-github-laptop-configuration

Open a terminal/shell and type:
Open a terminal/shell and type:

```
$ git config --global user.name "Your name here"
$ git config --global user.email "your_email@example.com"
```
I also do:
```
$ git config --global color.ui true
$ git config --global core.editor emacs
```
## Generate a ssh-keygen

```
$ ssh-keygen -t rsa -C "your_email@example.com"

$ pbcopy < ~/.ssh/id_rsa.pub
Paste your ssh public key into your github account settings.
```

Go to your github Account Settings
Click “SSH Keys” on the left.
Click “Add SSH Key” on the right.
Add a label (like “My laptop”) and paste the public key into the big text box.
In a terminal/shell, type the following to test it:

```
$ ssh -T git@github.com
```
If it says something like the following, it worked:

```
Hi username! You've successfully authenticated, but Github does
not provide shell access.
```
If you're facing this error:

```
~ :> git push origin my-branch
Username for 'https://github.com': myusername
Password for 'https://myusername@github.com': mypassword
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/my-repository’
```

You're gonna need to configure a token on ```settings > developer settings > personal access token > generate new token```

Copy the Personal Access Token and paste it into the “Password” field when you authenticate via the command line.
