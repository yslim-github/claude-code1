# CLAUDE.md

> Comprehensive guide for AI assistants working with this codebase

## Table of Contents
- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Development Workflow](#development-workflow)
- [Code Conventions](#code-conventions)
- [Testing Strategy](#testing-strategy)
- [Common Patterns](#common-patterns)
- [AI Assistant Guidelines](#ai-assistant-guidelines)
- [Troubleshooting](#troubleshooting)

## Overview

### Project Description
*This section will be populated as the project evolves*

### Technology Stack
*To be documented as technologies are added:*
- **Language(s)**:
- **Framework(s)**:
- **Build Tools**:
- **Testing**:
- **CI/CD**:

### Project Goals
*Key objectives and principles of this project*

## Repository Structure

```
.
├── src/              # Source code (to be created)
├── tests/            # Test files (to be created)
├── docs/             # Documentation (to be created)
├── scripts/          # Build and utility scripts (to be created)
├── config/           # Configuration files (to be created)
└── CLAUDE.md         # This file
```

### Key Directories
*Update this section as the structure develops:*

- **`src/`**: Main application source code
- **`tests/`**: Unit, integration, and e2e tests
- **`docs/`**: Additional documentation and guides
- **`scripts/`**: Development and deployment scripts
- **`config/`**: Environment and build configurations

## Development Workflow

### Branch Strategy

**Branch Naming Convention:**
- `main` or `master`: Production-ready code
- `develop`: Integration branch for features
- `feature/<name>`: New features
- `bugfix/<name>`: Bug fixes
- `hotfix/<name>`: Urgent production fixes
- `claude/<session-id>`: AI assistant working branches

**Current Branch:** `claude/claude-md-mhzmnf60k24acafu-01UNppfHdEBD8DgWd3QfWU6r`

### Commit Guidelines

**Commit Message Format:**
```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or updating tests
- `chore`: Maintenance tasks
- `perf`: Performance improvements

**Example:**
```
feat(auth): implement JWT authentication

- Add JWT token generation
- Implement token validation middleware
- Add refresh token logic

Closes #123
```

### Pull Request Process

1. **Create Feature Branch**: Branch from `develop` or `main`
2. **Implement Changes**: Follow code conventions
3. **Write Tests**: Ensure adequate test coverage
4. **Update Documentation**: Keep docs in sync with code
5. **Run Tests Locally**: Verify all tests pass
6. **Create PR**: With clear description and context
7. **Code Review**: Address feedback
8. **Merge**: Squash or merge commits as appropriate

## Code Conventions

### General Principles

1. **Readability First**: Code is read more often than written
2. **DRY (Don't Repeat Yourself)**: Avoid duplication
3. **SOLID Principles**: Follow object-oriented design principles
4. **KISS (Keep It Simple, Stupid)**: Favor simplicity over complexity
5. **YAGNI (You Aren't Gonna Need It)**: Don't add functionality speculatively

### Naming Conventions

*To be defined based on the primary language:*

**Variables:**
- Use descriptive names
- Follow language-specific casing (camelCase, snake_case, PascalCase)

**Functions/Methods:**
- Verb-based names describing action
- Clear intent and single responsibility

**Classes:**
- Noun-based names
- PascalCase convention

**Files:**
- Consistent naming pattern
- Reflect the primary export/class

### Code Style

*To be configured with linters/formatters:*
- Use a formatter (e.g., Prettier, Black, rustfmt)
- Configure linter (e.g., ESLint, Pylint, Clippy)
- Enforce style in CI/CD pipeline

### Documentation Standards

**Code Comments:**
- Explain "why", not "what"
- Document complex algorithms
- Use docstrings/JSDoc for public APIs

**README Files:**
- Each major directory should have context
- Include setup and usage instructions

## Testing Strategy

### Test Pyramid

```
       /\
      /  \     E2E Tests (Few)
     /----\
    /      \   Integration Tests (Some)
   /--------\
  /          \ Unit Tests (Many)
 /____________\
```

### Testing Guidelines

1. **Unit Tests**: Test individual functions/methods in isolation
2. **Integration Tests**: Test component interactions
3. **E2E Tests**: Test complete user workflows
4. **Test Coverage**: Aim for >80% code coverage
5. **Test Organization**: Mirror source structure in test directory

### Running Tests

```bash
# To be updated with actual commands
npm test          # Run all tests
npm run test:unit # Run unit tests
npm run test:e2e  # Run e2e tests
npm run coverage  # Generate coverage report
```

## Common Patterns

### Design Patterns in Use

*Document recurring patterns as they emerge:*

**Pattern Name**
- **When to Use**: Description of use case
- **Example Location**: `src/path/to/example.js:123`
- **Key Considerations**: Important notes

### Architectural Decisions

*Track important architectural choices:*

**Decision Title**
- **Date**: YYYY-MM-DD
- **Context**: What led to this decision
- **Decision**: What was decided
- **Consequences**: Impact and trade-offs

## AI Assistant Guidelines

### Best Practices for Claude

1. **Read Before Writing**
   - Always read existing files before editing
   - Understand context and patterns
   - Maintain consistency with existing code

2. **Use TodoWrite Tool**
   - Plan complex tasks with todos
   - Track progress transparently
   - Mark tasks complete incrementally

3. **Testing Requirements**
   - Write tests for new functionality
   - Update tests when modifying code
   - Verify tests pass before committing

4. **Documentation**
   - Update relevant docs with code changes
   - Keep CLAUDE.md current
   - Document non-obvious decisions

5. **Security Considerations**
   - Avoid hardcoded secrets
   - Validate and sanitize inputs
   - Follow OWASP guidelines
   - Watch for: SQL injection, XSS, CSRF, command injection

6. **Git Operations**
   - Commit with descriptive messages
   - Push to correct branch (claude/* branches)
   - Create PRs with comprehensive descriptions
   - Use retry logic for network failures (4 retries with exponential backoff)

### Preferred Tools

- **File Search**: Use `Glob` for pattern matching
- **Content Search**: Use `Grep` for code search
- **File Operations**: Use `Read`, `Edit`, `Write` (not bash commands)
- **Complex Exploration**: Use `Task` tool with `Explore` agent
- **Terminal Operations**: Use `Bash` only for git, npm, docker, etc.

### Common Workflows

**Adding a New Feature:**
```
1. Use TodoWrite to plan implementation
2. Create/switch to feature branch
3. Implement with tests
4. Update documentation
5. Run tests and verify
6. Commit and push
7. Create PR
```

**Fixing a Bug:**
```
1. Reproduce the bug
2. Write failing test
3. Implement fix
4. Verify test passes
5. Check for similar issues
6. Commit and push
```

**Refactoring:**
```
1. Ensure tests exist and pass
2. Make incremental changes
3. Run tests after each change
4. Update documentation
5. Commit logical chunks
```

## Troubleshooting

### Common Issues

**Issue: Tests Failing**
- Check test logs for specific failures
- Verify dependencies are installed
- Check for environment-specific issues
- Run tests individually to isolate problems

**Issue: Build Failures**
- Check for syntax errors
- Verify all dependencies are installed
- Check build configuration
- Review recent changes

**Issue: Git Push Failures**
- Ensure branch name follows convention (claude/* prefix)
- Check network connection
- Retry with exponential backoff (2s, 4s, 8s, 16s)
- Verify remote URL is correct

### Debug Commands

```bash
# To be populated with project-specific commands
git status              # Check git state
git log --oneline -10   # Recent commits
git diff                # See changes
```

## Maintenance

### Regular Updates

This file should be updated when:
- New patterns or conventions are established
- Architecture changes significantly
- New tools or frameworks are added
- Development workflows evolve
- Common issues and solutions are discovered

### Version History

**v1.0.0** - 2025-11-15
- Initial CLAUDE.md creation
- Established template structure
- Defined core guidelines for AI assistants

---

*Last Updated: 2025-11-15*
*Maintained by: AI Assistants working on this codebase*
