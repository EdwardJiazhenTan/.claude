# Cleanup Codebase

Analyze the codebase and identify redundant files for cleanup.

## Tasks

### 1. Find Redundant Files

Scan the entire codebase and identify:

- **Expired tests**: Test files for removed features, outdated test patterns, or tests that no longer run
- **Redundant code files**: Duplicate implementations, unused modules, deprecated utilities
- **Unnecessary markdown files**: Outdated documentation, duplicate READMEs, stale notes

For each file found, provide:

- File path
- Reason for removal
- Estimated safety level (safe/review needed/risky)

### 2. Review .gitignore

Check `.gitignore` file and ensure these patterns are included:

- `node_modules/` or equivalent dependency directories
- Build artifacts (`dist/`, `build/`, `.next/`, etc.)
- IDE files (`.vscode/`, `.idea/`, etc.)
- OS files (`.DS_Store`, `Thumbs.db`)
- Environment files (`.env*`)
- Log files (`*.log`)
- Cache directories
- Package lock files if not needed in repo

Flag any missing patterns that could lead to unwanted commits.

## Output Format

```
## Redundant Files Found
- [ ] path/to/file.ext - Reason (Safety: level)

## .gitignore Issues
- Missing pattern: `pattern/` - Prevents: description
```

## Instructions

Do NOT delete files automatically. Only identify and report for manual review.
