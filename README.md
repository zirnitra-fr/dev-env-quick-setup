# Dev Environment Quick Setup

A streamlined tool for quickly setting up development environments across different platforms and technologies.

## 🎯 Overview

Dev Environment Quick Setup is an open-source project designed to simplify and automate the process of setting up development environments. Whether you're onboarding new team members, switching between projects, or setting up a fresh machine, this tool helps you get up and running quickly.

## ✨ Features

- **Automated Setup**: Quick installation of common development tools and dependencies
- **Cross-Platform Support**: Works on Linux, macOS, and Windows
- **Customizable Configurations**: Easily adapt setup scripts to your project's needs
- **Version Management**: Support for multiple versions of languages and tools
- **Reproducible Environments**: Ensure consistency across team members
- **Modular Design**: Pick and choose only the tools you need

## 📋 Prerequisites

Before using this tool, ensure you have:

- Git installed on your system
- Bash shell (or WSL on Windows)
- Administrative/sudo privileges for installing system packages
- Internet connection for downloading dependencies

## 🚀 Quick Start

### Installation

```bash
# Clone the repository
git clone https://github.com/zirnitra-fr/dev-env-quick-setup.git
cd dev-env-quick-setup

# Make the setup script executable
chmod +x setup.sh

# Run the setup
./setup.sh
```

### Basic Usage

```bash
# Setup a basic development environment
./setup.sh --basic

# Setup for specific technologies
./setup.sh --node --python --docker

# View all available options
./setup.sh --help
```

## 🔧 Configuration

You can customize the setup by editing the configuration file:

```bash
# Copy the example configuration
cp config.example.json config.json

# Edit the configuration file
nano config.json
```

### Configuration Options

- `tools`: List of tools to install
- `versions`: Specific versions for each tool
- `paths`: Custom installation paths
- `environment`: Environment variables to set

## 📚 Documentation

### Installation Guide

**System Requirements:**
- Linux, macOS, or Windows (with WSL)
- Git 2.0+
- Bash shell
- Sudo/admin privileges

**Installation Steps:**
1. Clone: `git clone https://github.com/zirnitra-fr/dev-env-quick-setup.git`
2. Navigate: `cd dev-env-quick-setup`
3. Make executable: `chmod +x setup.sh`
4. Run: `./setup.sh`

### Configuration Reference

The configuration file supports the following structure:

```json
{
  "tools": ["git", "curl", "wget"],
  "versions": {
    "node": "20.x",
    "python": "3.11"
  },
  "paths": {
    "install_dir": "/usr/local"
  },
  "environment": {
    "EDITOR": "vim"
  }
}
```

### Troubleshooting

**Common Issues:**

- **Permission Denied**: Run with sudo: `sudo ./setup.sh`
- **Command Not Found**: Ensure script is executable: `chmod +x setup.sh`
- **Network Issues**: Check internet connection and proxy settings

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
