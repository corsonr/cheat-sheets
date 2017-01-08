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
| `$ git diff --staged` | Shows file differences between staging and the last file version |
| `$ git reset [file]` | Unstages the file, but preserve its contents |
| `$ git commit -m "[descriptive message]"` | Records file snapshots permanently in version history |
