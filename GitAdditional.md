# Git additional commands

Contains some very specific and rarely used commands.

## Update commits email

```git
git filter-branch --env-filter '
OLD_EMAIL="old-email@example.com"
CORRECT_NAME="Your Correct Name"
CORRECT_EMAIL="new-email@example.com"

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

After rewriting the commit history, force-push the changes to the remote repository.

```git
git push --force --tags origin 'refs/heads/*'
```

Check the commit history to ensure the email addresses have been updated correctly.

```git
git log
```
