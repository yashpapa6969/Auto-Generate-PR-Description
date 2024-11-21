# Auto-Generate-PR-Description

A GitHub Action that automatically generates and updates pull request descriptions with commit logs and version tracking. This action helps maintain consistent and informative PR documentation by automatically generating change logs from commit messages.

## Features

- 🔄 Automatically generates PR descriptions from commit logs
- 📝 Updates PR descriptions when new commits are pushed
- 🏷️ Tracks version numbers across releases
- 🚀 Automatically updates PR titles for merged PRs with version numbers
- 💬 Maintains change logs in PR comments

## Usage

To use this action in your repository, create a workflow file (e.g., `.github/workflows/pr-description.yml`) with the following configuration:

## Inputs

| Input | Description | Required | Default |
|-------|-------------|----------|---------|
| `github_token` | GitHub token for API access | Yes | `${{ github.token }}` |
| `base_branch` | Base branch to track PRs against | No | `dev` |
| `team_branch` | Team branch name to filter PRs | No | `Team` |

## Output Format

The action generates PR descriptions in the following format:

## Change Logs

- [abc1234](https://github.com/owner/repo/commit/abc1234): Commit message 1
- [def5678](https://github.com/owner/repo/commit/def5678): Commit message 2
...

## Version Tracking

The action automatically manages version numbers following these rules:
- Retrieves the latest version from GitHub releases
- Increments the patch version for each new release
- Updates PR titles with the new version number when merged

## Permissions

This action requires the following permissions:
- `contents: read` - For accessing repository content
- `pull-requests: write` - For updating PR descriptions and comments

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

Created by [@yashpapa6969](https://github.com/yashpapa6969)