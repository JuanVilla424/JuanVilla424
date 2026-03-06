# Project Context

## What This Repository Does

JuanVilla424 is a GitHub profile repository that doubles as a CI/CD template baseline. It serves two purposes:

1. **GitHub Profile Page**: The `README.md` renders on the GitHub profile page for user `JuanVilla424`, displaying tech stack, project portfolio, stats, and contact information.

2. **CI/CD Template Baseline**: The repository contains the foundational infrastructure for automated versioning, pre-commit quality gates, security policies, and branch-based release workflows. Other repositories (`github-cicd-template`, `langding`, `anisakys`, etc.) are derived from or reference this baseline.

## Current State

- Version: `1.0.18` (tracked in `pyproject.toml` and `.bumpversion.cfg`)
- Branch: `dev` is the active development branch
- Submodules: `scripts/` (CI/CD scripts), `langding/` (AI landing page project)
- Pre-commit hooks: configured and operational
- CI/CD: GitHub Actions workflows manage branch promotions (dev → test → prod → main)

## Key Entry Points

| Entry Point               | Description                                                       |
| ------------------------- | ----------------------------------------------------------------- |
| `README.md`               | GitHub profile display page; also serves as project documentation |
| `.pre-commit-config.yaml` | Defines all local quality gates executed on commit/push           |
| `pyproject.toml`          | Project configuration: version, dependencies, tool settings       |
| `.bumpversion.cfg`        | Version bump targets; drives automated semantic versioning        |
| `scripts/`                | All CI/CD automation scripts (submodule)                          |
| `.github/workflows/`      | GitHub Actions workflows for branch promotions and releases       |

## Environment Requirements

| Requirement   | Version  | Purpose                                      |
| ------------- | -------- | -------------------------------------------- |
| Python        | >=3.12   | Runtime for all scripts and pre-commit hooks |
| pip / Poetry  | latest   | Dependency management                        |
| pre-commit    | >=4.0.0  | Hook runner                                  |
| Node.js / npm | >=18     | Prettier for Markdown formatting             |
| Git           | >=2.30   | Submodule support, hook installation         |
| bump2version  | >=1.0.0  | Semantic version management                  |
| black         | >=26.1.0 | Python code formatter                        |
| pylint        | >=4.0.2  | Python linter                                |
| isort         | >=8.0.0  | Python import sorter                         |

## Conventions

- Commit format: `type(scope): description [versioning keyword]`
- Versioning keywords: `[major candidate]`, `[minor candidate]`, `[patch candidate]`
- All Python files formatted with black (line-length: 100) and sorted with isort
- YAML files formatted by `scripts/format_yaml`
- Changelog auto-generated from git history by `scripts/generate_changelog`
