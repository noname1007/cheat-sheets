# Github CLI

To use [Git](https://git-scm.com) on the command line, you need to download, install, and configure it on your computer.

## Setup Git

To setup Git, you have to set your Git username and your commit email address.
<br></br>

```bash
# set user

git config --global user.name "[USER]"

# set email

git config --global user.email "[EMAIL]"

```
## Github CLI
Next you have  to install [Github CLI](https://cli.github.com) and authenticate Github from Git and set your Git protocol (ssh/https).
<br></br>

```bash
gh auth login -p https
```