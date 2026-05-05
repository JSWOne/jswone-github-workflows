# Agent Instructions for JSWOne GitHub Workflows Repository

## Session Workflow Rules
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

## Pre-commit Workflow Validation
Before committing any workflow changes:
1. **YAML Lint Check** — Run `yamllint` or similar tool to validate YAML syntax and catch indentation errors
2. **Dry-run in test-playground** — Copy the workflow to `test-playground/` and trigger it manually to encounter and solve edge cases before committing
3. **Workflow must pass linting and dry-run** before staging and committing

## Commit Messages
- Use conventional commit messages when appropriate
- Be descriptive about what was changed
- Reference related issues if applicable

## test-playground Directory
- The `test-playground/` directory is a sandbox for testing workflow changes
- It must **never be committed to the main branch**
- Always add `test-playground/` to `.gitignore`

## Examples
- `git checkout -b feature/workflow-ci-cd-pipeline`
- `git checkout -b chore/workflow-security-scanning`
- `git checkout -b feature/workflow-dependency-management`