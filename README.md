<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,14,16,18,20&height=120&section=header" width="100%" alt="Header" />

# JuanVilla424

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=22&duration=2800&pause=2000&color=00D9FF&center=true&vCenter=true&width=500&lines=DevOps+Engineer;Cloud+Architect" alt="Typing SVG" />

<br>

[![Followers](https://img.shields.io/github/followers/JuanVilla424?style=flat-square&color=00d9ff&labelColor=1a1b27)](https://github.com/JuanVilla424?tab=followers)
[![Stars](https://img.shields.io/github/stars/JuanVilla424?style=flat-square&color=00d9ff&labelColor=1a1b27)](https://github.com/JuanVilla424)
[![License](https://img.shields.io/badge/License-GPLv3-blue?style=flat-square&color=00d9ff&labelColor=1a1b27)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.18-00d9ff?style=flat-square&labelColor=1a1b27)](CHANGELOG.md)

</div>

<br>

## Description

JuanVilla424 is the GitHub profile repository for a DevOps Engineer and Cloud Architect. It serves as a central hub showcasing projects, tech stack, activity, and professional contact information. The repository also acts as a template baseline for CI/CD tooling, versioning automation, and security policy enforcement across all managed repositories.

<br>

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Setup](#environment-setup)
  - [Pre-Commit Hooks](#pre-commit-hooks)
- [Scripts](#scripts)
- [Contributing](#contributing)
- [Contact](#contact)
- [License](#license)

<br>

## Features

- Automated versioning with bump2version following Semantic Versioning
- Pre-commit hooks for code quality: formatting, linting, YAML validation, changelog generation
- Branch-based release workflow: dev → test → prod → main
- Security policy with responsible disclosure process
- Submodule-based CI/CD scripts for reuse across repositories
- Commit message validation and automatic changelog generation

<br>

## Getting Started

### Prerequisites

- Python 3.12+
- Git
- Node.js (for Prettier markdown formatting)
- Docker (optional, for container-based workflows)

### Installation

1. **Clone the repository**

   ```bash
   git clone git@github.com:JuanVilla424/JuanVilla424.git
   cd JuanVilla424
   ```

2. **Initialize submodules**

   ```bash
   git submodule init && git submodule update --remote
   ```

3. **Create and activate a virtual environment**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

4. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

### Environment Setup

No `.env` file is required for the base profile repository. For CI/CD workflows, the following GitHub Actions secrets must be configured in repository settings:

| Secret              | Description                                 |
| ------------------- | ------------------------------------------- |
| `GITHUB_TOKEN`      | Auto-provided by GitHub Actions             |
| `BUMP_VERSION_USER` | Username for automated version bump commits |
| `BUMP_VERSION_PAT`  | Personal access token for version bump push |

### Pre-Commit Hooks

Install the pre-commit hooks after setting up your environment:

```bash
pip install pre-commit
pre-commit install
pre-commit install --hook-type pre-push
```

Run hooks against all files manually:

```bash
pre-commit run --all-files
```

The following hooks are configured:

| Hook                       | Stage    | Description                                  |
| -------------------------- | -------- | -------------------------------------------- |
| `trailing-whitespace`      | commit   | Remove trailing whitespace                   |
| `end-of-file-fixer`        | commit   | Ensure files end with a newline              |
| `check-yaml`               | commit   | Validate YAML syntax                         |
| `black`                    | commit   | Python code formatter                        |
| `pylint`                   | commit   | Python linter                                |
| `yaml-format`              | commit   | Format YAML files                            |
| `bump-year`                | commit   | Update copyright year in license headers     |
| `generate-changelog`       | commit   | Auto-generate CHANGELOG from commit messages |
| `validate-commit`          | pre-push | Validate commit messages against conventions |
| `commit-msg-version-check` | pre-push | Ensure versioning keyword is present         |
| `prettier`                 | commit   | Format Markdown files                        |

<br>

## Scripts

All CI/CD scripts are managed as a git submodule under `scripts/`. Each script is a self-contained Python module.

| Script                    | Description                                            |
| ------------------------- | ------------------------------------------------------ |
| `bump_year`               | Updates copyright year across license headers          |
| `commit_msg_version_bump` | Validates and bumps version based on commit message    |
| `control_commit`          | Enforces commit message format and versioning keywords |
| `crypto_controller`       | Manages cryptographic key initialization               |
| `format_yaml`             | Formats YAML files to a consistent style               |
| `generate_changelog`      | Generates CHANGELOG.md from git commit history         |
| `init_security_config`    | Initializes security configuration baseline            |
| `init_template`           | Bootstraps new repositories from this template         |
| `validate_docker_compose` | Validates docker-compose file syntax and structure     |

<br>

## Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) and [Code of Conduct](CODE_OF_CONDUCT.md) before submitting pull requests.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes following the [commit conventions](VERSIONING.md)
4. Push and open a pull request

<br>

## Contact

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/[are-you-ok?]/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:r6ty5r296it6tl4eg5m.constant214@passinbox.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/JuanVilla424)

</div>

<br>

## Projects

<div align="center">

| Project                                                                    | Description                                |
| -------------------------------------------------------------------------- | ------------------------------------------ |
| [**Anisakys**](https://github.com/JuanVilla424/anisakys)                   | Open Phishing Monitor & Threat Hunt Daemon |
| [**Langding**](https://github.com/JuanVilla424/langding)                   | AI-driven landing page auto-translate      |
| [**AbuseIPDB IOC**](https://github.com/JuanVilla424/abuseipdb-ioc)         | TAXII2 Processor with REST API for ELK     |
| [**CI/CD Template**](https://github.com/JuanVilla424/github-cicd-template) | Complete CI/CD Template Repository         |
| [**Scripts**](https://github.com/JuanVilla424/scripts)                     | CI/CD Core Scripts                         |
| [**Open ELK Admin**](https://github.com/JuanVilla424/open-elk-adm)         | Elasticsearch Admin Stack                  |
| [**SMTP Relay**](https://github.com/JuanVilla424/smtp-relay)               | SMTP Relay Docker                          |

</div>

<br>

## Stats

<div align="center">
  <picture>
    <img src="https://github-readme-stats.vercel.app/api?username=JuanVilla424&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=00d9ff&icon_color=00d9ff&text_color=c9d1d9" height="165" alt="Stats"/>
  </picture>
  <picture>
    <img src="https://github-readme-streak-stats-eight.vercel.app/?user=JuanVilla424&theme=tokyonight&hide_border=true&background=0d1117&ring=00d9ff&fire=00d9ff&currStreakLabel=c9d1d9" height="165" alt="Streak"/>
  </picture>
</div>

<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=JuanVilla424&theme=react-dark&hide_border=true&bg_color=0d1117&color=00d9ff&line=00d9ff&point=ffffff&area=true&area_color=00d9ff" width="95%" alt="Activity"/>
</div>

<br>

## License

2026 - This project is licensed under the [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html). You are free to use, modify, and distribute this software under the terms of the GPL-3.0 license. This license ensures that all derivatives of this software remain open source. Any modifications or distributions must include the original license and make source code available. For more details, please refer to the [LICENSE](LICENSE) file included in this repository.

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,14,16,18,20&height=120&section=footer" width="100%" alt="Footer" />
</div>
