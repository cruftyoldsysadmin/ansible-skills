# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.1] - 2026-03-04

### Fixed
- Removed duplicate `version` field from `marketplace.json` (already in `plugin.json`)

### Added
- `argument-hint` frontmatter to `ansible-convert` and `ansible-debug` skills for better autocomplete UX
- `disable-model-invocation: true` to `ansible-interactive` skill to prevent unintended auto-triggering
- `.pluginignore` to exclude example content (`my-ansible/`, Vagrant files) from plugin cache
- This `CHANGELOG.md`

### Changed
- Updated README with `--plugin-dir` development testing instructions
- Updated repository structure diagram in README

## [1.0.0] - 2024-01-01

### Added
- Initial release with 4 Ansible skills
- `ansible-playbook`: Core playbook development reference
- `ansible-debug`: Troubleshooting guide for Ansible errors
- `ansible-convert`: Shell script to Ansible conversion
- `ansible-interactive`: Step-by-step guided development
- Example Ansible project with tutorials in `my-ansible/`
