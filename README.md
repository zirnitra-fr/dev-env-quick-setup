# Dev Environment Quick Setup (deqs)

A streamlined binary tool for quickly setting up development environments across different platforms and technologies.

## 🎯 Overview

**deqs** (Development Environment Quick Setup) is an open-source binary tool that reads configuration files and executes commands to automate the setup of development environments. Whether you're onboarding new team members, switching between projects, or setting up a fresh machine, deqs helps you get up and running quickly by executing predefined setup commands from your configuration.

## ✨ Features

- **Configuration-Driven**: Define your environment setup in TOML, YAML, or other configuration formats
- **Command Execution**: Execute setup commands automatically from configuration files
- **Cross-Platform Support**: Binary available for Linux, macOS, and Windows
- **Flexible Configuration**: Easily adapt configuration files to your project's needs
- **Version Management**: Support for multiple versions of languages and tools
- **Reproducible Environments**: Ensure consistency across team members with shared configuration files
- **Modular Design**: Pick and choose only the tools you need in your configuration

## 📋 Prerequisites

Before using deqs, ensure you have:

- The deqs binary installed on your system
- Administrative/sudo privileges for installing system packages (depending on your configuration)
- Internet connection for downloading dependencies (depending on your configuration)

## 🚀 Quick Start

### Installation

Download the deqs binary for your platform from the [releases page](https://github.com/zirnitra-fr/dev-env-quick-setup/releases) and add it to your PATH.

```bash
# Example for Linux (amd64)
curl -L https://github.com/zirnitra-fr/dev-env-quick-setup/releases/latest/download/deqs-linux-amd64 -o deqs
chmod +x deqs
sudo mv deqs /usr/local/bin/

# Example for macOS (amd64)
curl -L https://github.com/zirnitra-fr/dev-env-quick-setup/releases/latest/download/deqs-darwin-amd64 -o deqs
chmod +x deqs
sudo mv deqs /usr/local/bin/

# Example for Windows (amd64)
# Download deqs-windows-amd64.exe from the releases page and add to PATH
```

### Basic Usage

```bash
# Run deqs with a configuration file
deqs config.toml

# Or with a YAML configuration
deqs config.yaml

# Check version
deqs --version

# View all available options
deqs --help
```

## 🔧 Configuration

Create a configuration file (TOML, YAML, or other supported format) to define your environment setup:

### TOML Example

```toml
# config.toml
[[commands]]
name = "Install Node.js"
command = "curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -"

[[commands]]
name = "Install npm packages"
command = "npm install -g yarn pnpm"

[[commands]]
name = "Setup Git"
command = "git config --global user.name 'Your Name'"
```

### YAML Example

```yaml
# config.yaml
commands:
  - name: Install Python
    command: sudo apt-get install -y python3.11
  - name: Install pip packages
    command: pip install --user poetry black pytest
```

### Configuration Options

Configuration files define a series of commands that deqs will execute to set up your environment. Each command can include:
- `name`: Descriptive name for the setup step
- `command`: The command to execute
- Additional options (to be documented as features are implemented)

## 📚 Documentation

### Installation Guide

**System Requirements:**
- Linux, macOS, or Windows
- Administrative privileges (depending on your configuration)

**Installation Steps:**
1. Download the deqs binary for your platform from the releases page
2. Make it executable: `chmod +x deqs` (Linux/macOS)
3. Move to PATH: `sudo mv deqs /usr/local/bin/` (or add to your PATH)
4. Verify installation: `deqs --version`

### Configuration Reference

Create a configuration file defining the commands to execute for environment setup. Supported formats include TOML and YAML.

**Basic Structure:**
- Define a series of commands with descriptive names
- Each command is executed in sequence
- Commands can install tools, configure settings, or perform any shell operation

**Example Configuration:**
```toml
[[commands]]
name = "Update package manager"
command = "sudo apt-get update"

[[commands]]
name = "Install development tools"
command = "sudo apt-get install -y build-essential git curl"
```

### Troubleshooting

**Common Issues:**

- **Permission Denied**: Some commands may require sudo privileges
- **Command Not Found**: Ensure deqs is in your PATH
- **Configuration Parse Error**: Verify your configuration file syntax
- **Command Execution Failed**: Check individual command syntax and availability

For more help, open an issue on GitHub.

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

1. **Fork the Repository**: Create your own fork of the project
2. **Create a Branch**: Make a new branch for your feature or bugfix
3. **Make Changes**: Implement your changes with clear commit messages
4. **Test Thoroughly**: Ensure your changes work across platforms
5. **Submit a Pull Request**: Open a PR with a clear description of your changes

### Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR_USERNAME/dev-env-quick-setup.git
cd dev-env-quick-setup

# Create a new branch
git checkout -b feature/your-feature-name

# Make your changes and commit
git add .
git commit -m "Add: your feature description"

# Push to your fork
git push origin feature/your-feature-name
```

### Coding Standards

- Follow existing code style and conventions
- Add comments for complex logic
- Update documentation for new features
- Include tests where applicable

## 🐛 Reporting Issues

Found a bug or have a feature request? Please open an issue on our [GitHub Issues](https://github.com/zirnitra-fr/dev-env-quick-setup/issues) page.

When reporting issues, please include:

- Operating system and version
- Steps to reproduce the issue
- Expected vs actual behavior
- Any error messages or logs

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🌟 Acknowledgments

- Thanks to all our contributors who help improve this project
- Inspired by various dev environment setup tools in the community
- Built with ❤️ by the open-source community

## 📞 Support

- **GitHub Issues**: For bug reports and feature requests
- **Discussions**: For questions and community support

---

**Note**: This is an open-source project focused on providing tools for development environment setup. For enterprise or commercial support options, please contact us separately.
