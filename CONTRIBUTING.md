# Contributing to .github

This repository contains organization-wide configuration. Changes affect all
repositories in the `jolarca-dev` organization.

## Change Process

1. **Fork** (or branch) this repository
2. **Make changes** following the guidelines below
3. **Open a pull request** with the required template
4. **Wait for review** — two reviewers required for workflow changes
5. **Merge** after CI passes and approvals

## Commit Message Format

We follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**Types:**
- `feat` — New reusable workflow or feature
- `fix` — Bug fix in existing workflow
- `docs` — Documentation changes
- `chore` — Maintenance tasks

**Examples:**
```
feat(workflows): add Python linting to ci-base
fix(templates): correct PR template checkbox
docs(readme): update usage examples
```

## Workflow Development

### Testing Reusable Workflows

Before merging workflow changes:

1. Test in a fork or test repository
2. Verify all inputs/outputs work correctly
3. Ensure backwards compatibility (or document breaking changes)

### Adding New Workflows

New reusable workflows must:

- Include comprehensive comments
- Document all inputs with descriptions
- Follow the existing naming convention (`*-base.yml`)
- Include usage examples in README.md

## Review Requirements

| Change Type | Required Reviewers |
|-------------|-------------------|
| Workflow changes | 2 |
| Template changes | 1 |
| Documentation | 1 |

## Compliance

Changes to this repository must maintain:

- SOC 2 CC8.1 (change management)
- ISO 27001 A.8.25 (secure SDLC)

All workflow changes are logged in the CHANGELOG.md.
