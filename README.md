# NPM on Termux

A guide and toolkit for setting up and running Node.js and NPM on Termux (Android terminal emulator).

## Overview

This project helps users install and configure Node Package Manager (NPM) and related development tools on Termux, enabling JavaScript/Node.js development on Android devices.

## Prerequisites

- Termux installed on Android device
- Basic command-line knowledge
- Sufficient storage space (~500MB)

## Installation

### 1. Update Termux Packages

First, update and upgrade your Termux package manager:

```bash
pkg update && pkg upgrade
```

### 2. Install Node.js and NPM

```bash
pkg install nodejs
```

This will install both Node.js and NPM together.

### 3. Install Additional Development Tools

Depending on your needs, you may want to install:

```bash
# Python (useful for many npm packages with native dependencies)
pkg install python3

# Git (for version control and cloning repositories)
pkg install git

# Ruby (optional, if needed by your project)
pkg install ruby
```

## Verification

Verify that NPM is installed correctly:

```bash
npm --version
node --version
```

## Usage

### Create a New Project

```bash
mkdir my-project
cd my-project
npm init -y
```

### Install Dependencies

```bash
npm install package-name
```

### Clone a Repository

```bash
git clone https://github.com/username/repository.git
cd repository
npm install
npm start
```

## Troubleshooting

**Issue**: `npm: command not found`
- **Solution**: Ensure Node.js was installed correctly. Try: `pkg install nodejs --reinstall`

**Issue**: Permission denied when running scripts
- **Solution**: Make scripts executable: `chmod +x script-name.js`

**Issue**: Native module compilation fails
- **Solution**: Install build tools: `pkg install build-essential python3`

## Common Commands

| Command | Description |
|---------|-------------|
| `npm install` | Install dependencies from package.json |
| `npm start` | Run the start script |
| `npm run build` | Run the build script |
| `npm test` | Run tests |
| `npm list` | List installed packages |

## Tips for Development on Termux

- Use `nano` or `vim` for editing files, or install `nano-full` for a better editor
- Consider installing `openssh` for remote development: `pkg install openssh`
- Termux storage is limited, so keep projects organized
- For better terminal experience, use a Termux styling package

## Resources

- [Termux Documentation](https://termux.com)
- [Node.js Documentation](https://nodejs.org/docs/)
- [NPM Documentation](https://docs.npmjs.com/)

## License

This project is provided as-is for educational purposes.

## Contributing

Feel free to submit issues or improvements!
