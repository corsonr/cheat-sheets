# Git Cheat Sheet

Sources:
- https://www.git-tower.com/blog/git-cheat-sheet/
- https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf

## CONFIGURE TOOLING
Configure user information for all local repositories

| Command | Description |
| --- | --- |
| `$ git config --global user.name "[name]"` | Sets the name you want atached to your commit transactions |
| `$ git config --global user.email "[email address]"` | Sets the email you want atached to your commit transactions |
| `$ git config --global color.ui auto` | Enables helpful colorization of command line output |

## Create Repositories
Start a new repository or obtain one from an existing URL

| Command | Description |
| --- | --- |
| `$ git init [project-name]` | Creates a new local repository with the specified name |
| `$ git clone [url]` | Downloads a project and its entire version history |

## Make Changes
Review edits and craf a commit transaction

| Command | Description |
| --- | --- |
| `$ git status` | Lists all new or modified files to be commited |
| `$ git diff` | Shows file differences not yet staged |
| `$ git add [file]` | Snapshots the file in preparation for versioning |
| `$ git add .` | Add all curent changes to the next commit |
| `$ git diff --staged` | Shows file differences between staging and the last file version |
| `$ git reset [file]` | Unstages the file, but preserve its contents |
| `$ git commit -m "[descriptive message]"` | Records file snapshots permanently in version history |
| `$ git commit -am "[descriptive message]"` | Snapshot all new files and records file snapshots permanently in version history |

Create a git patch from uncommitted changes in the current working directory

| Command | Description |
| --- | --- |
| `git diff > mypatch.txt` | Creates a diff file with the changes |
| `git apply mypatch.txt` | Applies the changes |

## Group Changes
Name a series of commits and combine completed efforts

| Command | Description |
| --- | --- |
| `$ git branch` | Lists all local branches in the current repository |
| `$ git branch [branch-name]` | Creates a new branch |
| `$ git checkout [branch-name]` | Switches to the specified branch and updates the working directory |
| `$ git merge [branch]` | Combines the specified branch’s history into the current branch |
| `$ git branch -d [branch-name]` | Deletes the specified branch |

## Refactor Filenames
Relocate and remove versioned files

| Command | Description |
| --- | --- |
| `$ git rm [file]` | Deletes the file from the working directory and stages the deletion |
| `$ git rm --cached [file]` | Removes the file from version control but preserves the file locally |
| `$ git mv [file-original] [file-renamed]` | Changes the file name and prepares it for commit |

## Suppress Tracking
Exclude temporary files and paths

| Command | Description |
| --- | --- |
| `temp-*` | A text file named .gitignore suppresses accidental versioning of files and paths matching the specified paterns |
| `$ git ls-files --other --ignored --exclude-standard` | Lists all ignored files in this project |

## Save Fragments
Shelve and restore incomplete changes

| Command | Description |
| --- | --- |
| `$ git stash` | Temporarily stores all modified tracked files |
| `$ git stash pop` | Restores the most recently stashed files |
| `$ git stash list` | Lists all stashed changesets |
| `$ git stash drop` | Discards the most recently stashed changeset |

## Review History
Browse and inspect the evolution of project files

| Command | Description |
| --- | --- |
| `$ git log` | Lists version history for the current branch |
| `$ git log --follow [file]` | Lists version history for a file, including renames |
| `$ git diff [first-branch]...[second-branch]` | Shows content differences between two branches |
| `$ git show [commit]` | Outputs metadata and content changes of the specified commit |

## Redo Commits
Erase mistakes and craf replacement history

| Command | Description |
| --- | --- |
| `$ git reset [commit]` | Undoes all commits afer [commit], preserving changes locally |
| `$ git reset --hard [commit]` | Discards all history and changes back to the specified commit |

## Synchronize Changes
Register a repository bookmark and exchange version history

| Command | Description |
| --- | --- |
| `$ git fetch [bookmark]` | Downloads all history from the repository bookmark |
| `$ git merge [bookmark]/[branch]` | Combines bookmark’s branch into current local branch |
| `$ git push [alias] [branch]` | Uploads all local branch commits to GitHub |
| `$ git pull` | Downloads bookmark history and incorporates changes |
