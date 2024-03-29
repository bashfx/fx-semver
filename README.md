# FX-SEMVER(1) Script for Semantic Versioning and Git Operations

## Overview

The SEMV script is a comprehensive Bash tool designed for managing semantic versioning (FX-SEMVER) in Git repositories. It provides a range of functionalities to automate versioning tasks, handle Git tags, and streamline development workflows. This tool is ideal for projects that require precise version tracking and integration with Git operations!

## Features

- **Semantic Version Management**: Automate the creation and management of semantic versioning tags in your Git repository.
- **Build Information Tracking**: Generate and update build information, including build counts and version details.
- **Tag Management**: Create, update, and push tags in your Git repository, with support for annotated and lightweight tags.
- **Version Comparison**: Compare different versions within the repository to determine the order and precedence.
- **Uncommitted Changes Check**: Easily identify uncommitted changes in your working directory.
- **Branch Validation**: Ensure operations are performed on the correct branches, like the main branch.
- **Customizable Commit Messages**: Tailor commit messages to fit specific workflows or conventions.

## Commands

The script provides a set of commands accessible through a `dispatch` function. These commands include:

- **`test`**: Test if the provided argument is a valid semantic version.
- **`bc`**: Get the build count since the last version tag.
- **`can`**: Check if the repository can be semantically versioned.
- **`latest`**: Retrieve the latest version tag from the repository.
- **`mark1`**: Initialize the repository with the first semantic version tag (`v0.0.1`).
- **`tags`**: List all tags in the repository.
- **`pend`**: Show pending commits since the last version tag.
- **`file (filename)`**: Create or update a build information file.
- **`insp`**: Inspect available functions in the script.
- **`auto (path)`**: Will attempt to find a semver for the dir or file passed.
- **`dry`**:  Dry run the bump version command.
- **`bump`**: Bump the version to the next level and retag.

## Flags

The script supports various flags for customizing its behavior:

- **`--debug` or `-d`**: Enable console messages, true by default.
- **`--yes` or `-y`**: Enable automatic 'yes' for confirmations.
- **`--dev` or `-N`**: Enable dev note `-build1234 or -dev1` tail on tags.
- **`--dist` or `-B`**: Enable build directory creation with the `file` command.
- **`--trace` or `-t`**: Enable trace mode for detailed operation logs.


## Dev Note

If a label `dev:...` is set then this marks the commit chain for a particular version as buggy, unfinished or dirty.

If you do a feature or fix bump with a prior dev label, you will be prompted to confirm the dirty version bump into a clean version. 

To generate a -devXXX or -buildXXX version, the `--dev` flag will automatically pick -buildXXX if there are no dev labels on the current chain of commits.


