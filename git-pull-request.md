Here are a few steps to create a pull request.

# 1. Fork a repo

First, you'll need to fork the repo. This is not mandatory, though. See how to [fork a repo](https://help.github.com/articles/fork-a-repo/).

# Clone a forked repo locally
```
cd /your-git-folder
git clone git@github.com:<your_username>/<repo_title>.git --recursive
cd <repo_title>
```

# 2. Link to upstream

```
git remote add upstream git@github.com:<original_username>/<repo_title>.git
git remote
```

# 3. Update fork

```
git fetch upstream
git merge upstream/master
git push origin master
```

# 4. Create a new branch

```
git checkout -b <branch_name>
```

# 5. Do your magic

Write your code, fix issue, do some magic stuff!

# 6. Send the fix

```
git add .
git commit -am 'message'
git push origin <branch_name>
```

# 7. Do the Pull Request on Github and delete branch

When PR is merged, delete remote branch on github directly and delete local branch using the following command:

```
git branch -D <branch_name>
```

# When NO Branch:

if needed (if changes made on GitHub directly and local isn’t updated):

```
git fetch origin
git pull origin
```
