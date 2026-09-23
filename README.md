# Project Template

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stars][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

A reusable GitHub repository template providing a clean starting point for new projects, with repository scaffolding, automation and standard project documentation.

## Overview

`project-template` is designed to reduce the repetitive setup required when creating a new GitHub repository.

It provides a reusable baseline containing common repository files, GitHub Actions workflows and supporting automation that can be adapted to suit individual projects.

## Included

The template includes:

- Standard repository documentation and community files
- GitHub Actions workflow scaffolding
- Reusable project structure
- Issue and pull request configuration
- MIT licence

The supplied workflows are intended as a starting point. Review and adjust them for the requirements and permissions of each repository created from this template.

## Technologies

- GitHub Actions
- Markdown

## Using the template

### Create a repository

1. Select **Use this template** on GitHub, or use the [Create a new repository from this template][template-url] link.
2. Choose the repository owner.
3. Enter the new repository name and description.
4. Choose the required visibility.
5. Select **Create repository**.

GitHub creates a new repository containing the files from this template without carrying across the template repository's Git history.

### Review the generated repository

After creating a repository, review the included files and workflows before beginning development.

In particular:

- Update project-specific documentation and metadata.
- Remove files or automation that the project does not require.
- Review `.github/workflows/` and enable only the workflows that are needed.
- Review repository and environment secrets before enabling workflows that require them.
- Keep GitHub Actions permissions at the minimum required by each workflow.

Where a workflow needs additional GitHub permissions, declare them explicitly using the workflow or job-level `permissions` configuration rather than enabling blanket repository-wide write access.

## Repository structure

The exact structure may evolve, but the template is intended to provide the common files required for a well-maintained GitHub repository.

```text
.
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── workflows/
│   └── SECURITY.md
│   └── SUPPORT.md
│   └── PULL_REQUEST_TEMPLATE.md

├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE.md
└── README.md
```

Project-specific repositories created from this template can add, replace or remove files as required.

## GitHub Actions

Automation included with this repository should be treated as reusable scaffolding rather than a universal configuration.

Before enabling a workflow:

1. Review its triggers.
2. Review all third-party actions it uses.
3. Check the permissions granted to `GITHUB_TOKEN`.
4. Remove permissions that are not required.
5. Configure any required repository or environment secrets.
6. Test the workflow in the generated repository.

Prefer explicit least-privilege permissions, for example:

```yaml
permissions:
  contents: read
```

Grant additional permissions only to the jobs or workflows that require them.

## Contributing

Contributions, fixes and improvements are welcome.

For significant changes:

1. Fork the repository.
2. Create a branch for the change.
3. Make and test the changes.
4. Commit the changes with a clear commit message.
5. Push the branch to your fork.
6. Open a pull request.

See [CONTRIBUTING.md](CONTRIBUTING.md) for repository-specific contribution guidance.

## Support

For bugs, feature requests or other repository-related queries, use [GitHub Issues][issues-url].

See [SUPPORT.md](.github/SUPPORT.md) for further guidance.

## Security

Please do not report security vulnerabilities through a public GitHub issue.

See [SECURITY.md](.github/SECURITY.md) for the appropriate reporting process.

## Licence

This project is licensed under the [MIT License](LICENSE.md).

[contributors-shield]: https://img.shields.io/github/contributors/smcnab1/project-template.svg?style=flat-square
[contributors-url]: https://github.com/smcnab1/project-template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/smcnab1/project-template.svg?style=flat-square
[forks-url]: https://github.com/smcnab1/project-template/forks
[stars-shield]: https://img.shields.io/github/stars/smcnab1/project-template.svg?style=flat-square
[stars-url]: https://github.com/smcnab1/project-template/stargazers
[issues-shield]: https://img.shields.io/github/issues/smcnab1/project-template.svg?style=flat-square
[issues-url]: https://github.com/smcnab1/project-template/issues
[license-shield]: https://img.shields.io/github/license/smcnab1/project-template.svg?style=flat-square
[license-url]: https://github.com/smcnab1/project-template/blob/main/LICENSE.md
[template-url]: https://github.com/new?template_name=project-template&template_owner=smcnab1
