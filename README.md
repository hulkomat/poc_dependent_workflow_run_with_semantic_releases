# poc_dependent_workflow_run
This repository demonstrates how to run multiple dependent workflows in a project.

The example workflows trigger on a push to the main branch. If a commit follows the [conventional commit](https://www.conventionalcommits.org/en/v1.0.0/) format and updates the version, it creates a release after the [GitHub Actions demo workflow](https://docs.github.com/en/actions/writing-workflows/quickstart#creating-your-first-workflow) completes successfully.

## Try it yourself
You can test this by pushing a commit to the main branch with a conventional commit message:

```
| Commit Type | Description                            | Version Update Example |
|-------------|----------------------------------------|------------------------|
| `feat:`     | New feature                            | 1.2.3 -> 1.3.0         |
| `fix:`      | Bug fix                                | 1.2.3 -> 1.2.4         |
| `feat!:`    | Breaking change                        | 1.2.3 -> 2.0.0         |
| `chore:`    | Maintenance tasks                      | 1.2.3 -> 1.2.3         |
| `docs:`     | Documentation changes                  | 1.2.3 -> 1.2.3         |
| `style:`    | Code style changes (formatting, etc.)  | 1.2.3 -> 1.2.3         |
| `refactor:` | Code refactoring without changing behavior | 1.2.3 -> 1.2.3     |
| `perf:`     | Performance improvements               | 1.2.3 -> 1.2.3         |
| `test:`     | Adding or updating tests               | 1.2.3 -> 1.2.3         |
| `build:`    | Changes to build process or dependencies | 1.2.3 -> 1.2.3       |
| `ci:`       | Changes to CI configuration files and scripts | 1.2.3 -> 1.2.3   |
| `revert:`   | Reverts a previous commit              | 1.2.3 -> 1.2.3         |
```


Remember:
- `feat:` indicates a new feature that changes the application's behavior.
- `feat!:` indicates a breaking change that might not be backward compatible.

Conventional commits help in automating the versioning and release process.
