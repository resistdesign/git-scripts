# Git Scripts

This repository contains a collection of git utility scripts designed to simplify and automate common version control tasks.

## Quick start for a new project

Requires Git and Yarn. Publishing also requires the [GitHub CLI](https://cli.github.com/) authenticated with `gh auth login`.

```sh
gitnew my-project
cd my-project
gitpublish --public
```

To initialize the current directory instead, run `gitnew` without arguments. The initializer creates a `main` branch, a minimal `package.json` using `yarn init -y`, a README, a standard MIT license for Resist Design, and a practical Node/TypeScript `.gitignore`. It makes an initial commit so `gitpublish` can push immediately. Existing project files are not overwritten. It refuses to initialize inside an existing Git repository.

`gitpublish` creates a new GitHub repository, adds `origin`, and pushes existing commits. It defaults to the current folder name and **private** visibility. To override those defaults:

```sh
gitpublish --public
gitpublish --private --name another-name
gitpublish --public --name resistdesign/another-name
```

Uncommitted changes are not pushed. The script refuses to replace an existing `origin` remote.

## Script Descriptions

### `gitnew`
Initializes a new Git/Yarn project in the current directory or an optional named directory and creates a starter commit. Requires Git and Yarn.

### `gitpublish`
Creates a GitHub repository from the current Git project using `gh`, adds the `origin` remote, and pushes commits. Supports `-n`/`--name`, `--public`, and `--private` (default). Requires an existing commit.

### `gitapply`
Stages all changes, generates a commit message based on the first removed TODO comment in the staged files (if present), and commits and pushes the changes. Defaults to a generic commit message if no TODOs are detected or no message is provided.

### `gitback`
Switches to the `master` branch and updates it by fetching from the remote repository.

### `gitcom`
Stages all changes, commits with an empty message, pushes the changes, and clears the terminal before displaying the repository status.

### `gitgo`
Prompts the user for a commit type, subject, and message, then stages all changes, commits with the provided message, pushes the changes, and clears the terminal before showing the status.

### `githome`
Switches to the `main` branch and updates it by fetching from the remote repository.

### `gitpush`
Stages all changes, creates a commit message based on the provided arguments or defaults to a generic message, commits the changes, pushes to the remote repository, and displays the status.

### `gittoit`
Creates a new branch with the specified name, switches to it, pushes it to the remote repository, and displays the repository status.

### `gs`
Clears the terminal and displays the current status of the repository.
