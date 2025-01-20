# Git Scripts

This repository contains a collection of git utility scripts designed to simplify and automate common version control tasks.

## Script Descriptions

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
