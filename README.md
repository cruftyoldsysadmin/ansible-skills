# Ansible Skills for Claude Code

Ansible automation skills for Claude Code: playbook development, debugging, shell conversion, and interactive workflows.

## Installation

### From GitHub (recommended)

```bash
# Add the marketplace
/plugin marketplace add sigridjineth/hello-ansible-skills

# Install the plugin
/plugin install ansible-skills@hello-ansible-skills
```

### Development / Local Testing

Clone the repository and use `--plugin-dir` to load it directly:

```bash
git clone https://github.com/sigridjineth/hello-ansible-skills.git
claude --plugin-dir ./hello-ansible-skills
```

### Verify Installation

Run `/help` in Claude Code. You should see skills like:
- `ansible-skills:ansible-playbook`
- `ansible-skills:ansible-debug`
- `ansible-skills:ansible-convert`
- `ansible-skills:ansible-interactive`

## Skills Included

### ansible-playbook

Core playbook development reference. Use when creating playbooks, roles, or inventory files.

**Covers:**
- Project structure and ansible.cfg configuration
- Module patterns with FQCN (Fully Qualified Collection Names)
- Variable precedence rules
- Handlers and error handling
- Common mistakes and fixes

### ansible-debug

Troubleshooting guide for Ansible errors. Use when playbooks fail with connection, authentication, or module errors.

**Covers:**
- Error category diagnosis (connection, auth, module, syntax)
- Verbosity levels and debugging commands
- Common error patterns and solutions
- Performance debugging

### ansible-convert

Shell script to Ansible conversion. Use when migrating bash automation to idempotent playbooks.

**Covers:**
- Command-to-module mapping table
- Control flow conversion (conditionals, loops)
- When to use shell module
- Variable extraction patterns

### ansible-interactive

Step-by-step guided development. Use when starting a new Ansible project from scratch.

**Covers:**
- Environment analysis questions
- Project setup workflow
- Connectivity testing before playbooks
- Incremental development with validation

## Usage Examples

**Create a playbook:**
```
Create a playbook that installs nginx and configures it as a reverse proxy
```

**Convert a shell script:**
```
Convert this deployment script to Ansible: [paste script]
```

**Debug an error:**
```
My playbook fails with "UNREACHABLE" - help me debug
```

**Start from scratch:**
```
Help me set up Ansible for my 5 Ubuntu servers step by step
```

## Repository Structure

```
hello-ansible-skills/
├── .claude-plugin/
│   ├── plugin.json          # Plugin metadata
│   └── marketplace.json     # Marketplace configuration
├── skills/
│   ├── ansible-playbook/
│   │   └── SKILL.md
│   ├── ansible-debug/
│   │   └── SKILL.md
│   ├── ansible-convert/
│   │   └── SKILL.md
│   └── ansible-interactive/
│       └── SKILL.md
├── my-ansible/              # Example Ansible project (excluded from plugin cache)
│   ├── ansible.cfg
│   ├── inventory
│   ├── roles/
│   └── docs/                # Ansible tutorial (12 sections)
├── .pluginignore            # Excludes examples from plugin cache
├── CHANGELOG.md
├── README.md
└── LICENSE
```

## Contributing

Contributions welcome. If you find patterns that work well in your Ansible projects, consider adding them to the skills. Open an issue or submit a PR.

## License

MIT
