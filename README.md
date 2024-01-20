# 13-pic-git
great!
git clone http:// download project
git remote remove origin
git remote add origin http:// your project
------------copy-----------------------
git filter-branch -f --env-filter '
NEW_NAME="kimotoatsumi"
NEW_EMAIL="atsumi000105@gmail.com"

if [ "$GIT_COMMITTER_EMAIL" != "$NEW_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$NEW_NAME"
    export GIT_COMMITTER_EMAIL="$NEW_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" != "$NEW_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$NEW_NAME"
    export GIT_AUTHOR_EMAIL="$NEW_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags
---------------------------------------------------
git push --all    or   git  push -f origin main
git tag --all
git push --tags
![Uploading image.png…]()
