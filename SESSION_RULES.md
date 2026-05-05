# Session Workflow Rules

## Branch Management
- **Always create a new branch** for each new workflow implementation
- Never commit/push directly to the main branch
- Branch naming convention: `feature/workflow-[workflow-name]` or `chore/workflow-[workflow-name]`

## Development Process
1. Create new branch: `git checkout -b feature/workflow-[name]`
2. Make changes in the branch
3. Stage and commit changes with descriptive messages
4. Push branch to remote: `git push -u origin feature/workflow-[name]`
5. Create Pull Request from branch to main
6. Wait for review/approval before merging

## Workflow Implementation
Each workflow should be implemented as a GitHub Actions workflow file in `.github/workflows/` directory
- Use descriptive filenames: `[purpose].yml` or `[purpose].yaml`
- Follow GitHub Actions best practices
- Include proper triggers, jobs, and steps

## Commit Messages
- Use conventional commit messages when appropriate
- Be descriptive about what was changed
- Reference related issues if applicable

## Examples
- `git checkout -b feature/workflow-ci-cd-pipeline`
- `git checkout -b chore/workflow-security-scanning`
- `git checkout -b feature/workflow-dependency-management`