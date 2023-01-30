# Github Repositoty

## Create Repo

To create a public or private Github repository in your commandline, type
<br></br>

```bash
gh repo create

# or to skip prompts

gh repo create [NAME] --public --clone
```
## Commit changes
To stage and commit your changes to your repository, type
<br></br>

```bash
echo 'example' >> README.md

# view your changes

git status

# stage and commit

git add README.md && git commit -m "example"

git push --set-upstream origin HEAD
```