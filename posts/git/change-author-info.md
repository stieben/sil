# Change author info retroactively

_#unix_ _#bash_ _#git_

## Before pushing

1. Fix your information in the Git configuration of the project:

```bash
git config user.name "Your Correct Name"
git config user.email "your-correct-email@example.com"
```

2. Start rebase:

```bash
git rebase -i HEAD~1 # will bring up an editor
```

3. In the editor, mark the commit as `edit`, then save and exit the editor.

4. Do an amend that resets the author now that your information is updated:

```bash
git commit --amend --reset-author
```

5. Finish the rebase:

```bash
git rebase --continue
```

## After pushing

Open up a terminal:

```bash
git clone --bare https://github.com/<user>/<repo>.git
cd <repo>.git
nano git-author-rewrite.sh # create new script
```

Save the script like this:

```bash
#!/bin/sh

git filter-branch --env-filter '
OLD_EMAIL="<your-old-email@example.com>"
CORRECT_NAME="<Your Correct Name>"
CORRECT_EMAIL="<your-correct-email@example.com>"
if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$CORRECT_NAME"
    export GIT_COMMITTER_EMAIL="$CORRECT_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$CORRECT_NAME"
    export GIT_AUTHOR_EMAIL="$CORRECT_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
```

Back in the terminal:

```bash
chmod u+x git-author-rewrite.sh # make script executable
./git-author-rewrite.sh # run
git log # review Git history for errors
git push --force --tags origin 'refs/heads/*'
cd ..
rm -rf <repo>.git
```

## Sources

- [gist](https://gist.github.com/carlosmcevilly/2221249) by [carlosmcevilly](https://gist.github.com/carlosmcevilly)
- [GitHub Help](https://help.github.com/articles/changing-author-info/)
