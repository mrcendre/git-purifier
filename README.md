# `git-purifier`

*A straightforward Bash tool to rewrite commit information from a Git history, using `git-filter-repo`.*

> Note that this tool perform sensitive operations that may lead to data loss or corruption if not used carefully.
**It is recommended to create backups of your repository before using this tool.** Use at your own risks!

Just `cd` into the repository's directory, and run `git-purifier <action> <args>` to rewrite the repository.

`git-purifier` automates the process of rewriting commit information such as author and committer's name and email in a Git repository's history.

- Simple syntax
- Automatically manages remotes, unlike `git filter-repo`
- (TODO) Interactive commit message rewriting

## Usage

`git-purifier [author | committer] <author_name> <author_email>`
`git-purifier [messages] <author_email>`

**Important**: All of these commands must be invoked from the directory where the Git repository is located.

### Commands

- **`author`**: Rewrites the author information in all commits from the history to the given name and email.

- **`committer`**: Rewrites the committer information in all commits from the history to the given name and email.

- **`messages`**: (TODO) Starts interactively rewriting all commit messages whose author has the given email.


## Installation

To install this tool, make the program executable, then move (or link) to `usr/local/bin`:

   ```bash
   chmod +x ./git-purifier

   mv ./git-purifier /usr/local/bin/git-purifier
   # or
   ln $(pwd)/git-purifier /usr/local/bin/git-purifier
   ```

## Side notes

Made with ♥ by [mrcendre](https://cendre.me).

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.