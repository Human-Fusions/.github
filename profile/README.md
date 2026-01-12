# Human Fusions Institute GitHub Organization

Welcome to the Human Fusions Institute GitHub Organization! This guide outlines our best practices for collaborative development and repository management.

## Organization Philosophy

We use a **fork-and-pull-request workflow** to ensure code quality and keep our main branches stable and production-ready.

## Getting Started

### Teams

Members are organized into teams:
- **Faculty Team**
- **Staff Team**
- **Students Team**

Teams are granted repository access as a group.

### Accessing Repositories

1. **Fork** the repository to your personal GitHub account
2. **Clone** your fork locally: `git clone https://github.com/your-username/repo-name.git`
3. **Add upstream**: `git remote add upstream https://github.com/HumanFusionsInstitute/repo-name.git`

## Development Workflow

### Branching Strategy

Always create feature branches from `main`. The main branch must always be stable.

**Branch naming:**
- `feature/descriptive-name` - New features
- `bugfix/issue-description` - Bug fixes
- `docs/update-name` - Documentation
- `refactor/component-name` - Code refactoring

### Making Changes

1. Sync your fork:
```bash
   git fetch upstream
   git checkout main
   git merge upstream/main
```

2. Create a feature branch:
```bash
   git checkout -b feature/your-feature-name
```

3. Make changes and commit:
```bash
   git add .
   git commit -m "Add: Brief description of change"
```

4. Push to your fork:
```bash
   git push origin feature/your-feature-name
```

### Commit Messages

Format: `Type: Brief description`

**Types:** `Add`, `Fix`, `Update`, `Remove`, `Refactor`, `Docs`, `Test`, `Chore`

## Pull Request Process

1. Create PR from your fork to the main repository
2. Fill out the PR description:
   - What changed and why
   - Testing performed
   - Related issues (e.g., "Fixes #42")
3. Request review from team members
4. Address feedback and update PR
5. Merge after approval (requires at least one approval)
6. Delete feature branch after merge

**Keep PRs focused and under 400 lines when possible.**

## Issue Tracking

### When to Create Issues

- Bug reports
- Feature requests
- Documentation improvements
- Task tracking

Search existing issues before creating new ones to avoid duplicates.

### Bug Reports Should Include

- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Environment details (OS, versions, hardware)
- Error messages or screenshots

### Feature Requests Should Include

- Problem statement and use case
- Proposed solution
- Impact on existing functionality

### Issue Labels

**Type:** `bug`, `enhancement`, `documentation`, `task`, `question`

**Priority:** `priority: critical`, `priority: high`, `priority: medium`, `priority: low`

**Status:** `wip`, `blocked`, `ready`, `help wanted`, `good first issue`

### Best Practices

- Label issues promptly
- Assign ownership when work begins
- Reference issues in commits: "Fixes #123"
- Link PRs to issues in description
- Update status as work progresses
- Close with explanation when resolved

### Issue Templates

Repository owners should create templates in `.github/ISSUE_TEMPLATE/` for bug reports and feature requests.

## Documentation

### Repository README Requirements

- Project overview and purpose
- Prerequisites and dependencies
- Installation instructions
- Usage examples
- Architecture overview
- Contributing guidelines
- Team and contact information

**Use Wiki when:**
- README exceeds 500 lines
- Detailed architecture docs needed
- Multiple tutorials required

### Code Documentation

- Comment complex logic
- Use docstrings for functions and classes
- Document assumptions and edge cases
- Keep comments updated with code

## Code Quality

### Before Pushing

- Code follows project style
- All tests pass
- No debug statements
- No sensitive data committed
- Remove commented-out code

### Automated Checks

Include where applicable:
- Linting and formatting
- Unit tests (>80% coverage goal)
- CI/CD pipelines via GitHub Actions

## Security

**Never commit:**
- API keys or passwords
- SSH keys
- Database credentials
- Personal information

**Instead:**
- Use `.gitignore`
- Use environment variables
- Store secrets in GitHub Secrets

## Additional Guidelines

- **Dependency Management**: Pin versions, use virtual environments
- **Releases**: Use semantic versioning (MAJOR.MINOR.PATCH)
- **Communication**: Use GitHub issues and discussions for async communication
- **Stale Issues**: Inactive for 90+ days may be closed with notice

## Getting Help

- Create issues for technical problems
- Use discussions for questions
- Contact team leads for organization matters

---

**Goal:** Maintain high-quality, stable code while fostering collaboration. When in doubt, ask questions!

*Last Updated: January 2026*
