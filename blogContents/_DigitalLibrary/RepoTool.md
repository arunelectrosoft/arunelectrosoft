---
title: RepoTool
layout: post
categories: DigitalLibrary
published: true
---

# Repo Tool: Complete Guide for Managing Multiple Git Repositories

Google created the repo tool to simplify working with several open source git repositories.
It's primarily used for managing large projects like Android AOSP (Android Open Source Project) that consist of hundreds of individual Git repositories.

[Android Source code tools](https://source.android.com/setup/develop)

## Overview

The Repo tool is essential for projects that span multiple Git repositories. Instead of manually cloning and managing dozens or hundreds of repositories, Repo provides a unified interface to:
- Initialize and sync multiple repositories at once
- Manage branches across all repositories
- Submit changes for review
- Track project dependencies

### Source Tools used for Android
- [x] **Repo** - Multi-repository management tool
- [x] **Git** - Version control system for individual repositories
- [x] **Gerrit** - Web-based code review system
- [x] **Android code search** (https://cs.android.com/)
- [x] **Android code search and Referencing system** (https://developers.google.com/code-search)

## What is Repo?

> Repo is a Python script-based tool created by Google to manage the complexities of working with multiple Git repositories as a single project.

### Key Benefits:
- **Simplified Management**: Handle hundreds of repositories with single commands
- **Consistent State**: Ensure all repositories are at compatible versions
- **Parallel Operations**: Perform operations across multiple repos simultaneously
- **Unified Workflow**: Single interface for complex multi-repo operations

## Installation and Setup

### Prerequisites
- Python 3.6 or later
- Git 2.0 or later
- Linux, macOS, or Windows with WSL

### Installing Repo

```bash
# Create a directory for repo tool
mkdir -p ~/.local/bin

# Download repo tool
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.local/bin/repo

# Make it executable
chmod a+rx ~/.local/bin/repo

# Add to PATH (add this to your .bashrc or .zshrc)
export PATH=~/.local/bin:$PATH
```

### Alternative Installation (via package manager)
```bash
# Ubuntu/Debian
sudo apt-get install repo

# macOS with Homebrew
brew install repo
```

## Repo Manifest XML Format

Repo tool works with XML Manifest files that describe the structure of a project.

> Complete repo manifest documentation: [Repo Manifest Format](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/manifest-format.md)

### Basic Manifest Structure

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <remote name="origin"
          fetch="https://github.com/company/"
          review="https://gerrit.company.com/" />
  
  <default revision="main"
           remote="origin"
           sync-j="4" />
  
  <project path="frameworks/base"
           name="platform/frameworks/base"
           groups="pdk,frameworks_base" />
  
  <project path="system/core"
           name="platform/system/core"
           groups="pdk" />
</manifest>
```

### Key Manifest Elements:
- **`<remote>`**: Defines Git remote servers
- **`<default>`**: Sets default values for projects
- **`<project>`**: Individual Git repository definition
- **`<include>`**: Include other manifest files
- **`<linkfile>`**: Create symbolic links

## Common Repo Commands

### Basic Commands

#### Initialize a Repo Project
```bash
# Initialize repo with manifest URL
repo init -u <manifest_url> -b <branch>

# Example: Android AOSP
repo init -u https://android.googlesource.com/platform/manifest -b android-14.0.0_r1
```

#### Sync Repositories
```bash
# Sync all repositories
repo sync

# Sync with multiple parallel jobs (faster)
repo sync -j8

# Sync specific projects only
repo sync project1 project2

# Force sync (ignore local changes)
repo sync --force-sync
```

#### Check Status
```bash
# Show status of all repositories
repo status

# Show status in brief format
repo status -j8
```

#### Branch Management
```bash
# Start a new topic branch
repo start <branch_name> <project_list>

# Example: Start feature branch in specific projects
repo start new-feature frameworks/base system/core

# List all branches
repo branches

# Abandon a branch
repo abandon <branch_name> <project_list>
```

### Advanced Commands

#### Upload Changes for Review
```bash
# Upload current branch for review
repo upload

# Upload specific projects
repo upload frameworks/base system/core

# Upload with reviewers
repo upload --re=reviewer@company.com
```

#### Download Changes from Review
```bash
# Download a specific change
repo download <project> <change_number/patch_set>

# Example
repo download frameworks/base 12345/2
```

#### Manifest Operations
```bash
# Show current manifest
repo manifest

# Save current state to manifest
repo manifest -r -o snapshot.xml

# Show differences from manifest
repo diff
```

## Practical Workflow Examples

### Starting Development on AOSP

```bash
# 1. Create workspace directory
mkdir ~/android-aosp
cd ~/android-aosp

# 2. Initialize repo with specific Android version
repo init -u https://android.googlesource.com/platform/manifest -b android-14.0.0_r1

# 3. Sync all repositories (this will take time!)
repo sync -j$(nproc)

# 4. Start a new feature branch
repo start my-feature frameworks/base

# 5. Make changes in frameworks/base
cd frameworks/base
# ... make your changes ...

# 6. Check status
repo status

# 7. Upload for review (if using Gerrit)
repo upload
```

### Working with Custom Manifests

```bash
# 1. Create custom manifest repository
git init manifest-repo
cd manifest-repo

# 2. Create default.xml
cat > default.xml << EOF
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <remote name="github" fetch="https://github.com/" />
  <default revision="main" remote="github" />
  
  <project path="project-a" name="company/project-a" />
  <project path="project-b" name="company/project-b" />
</manifest>
EOF

# 3. Commit and push manifest
git add default.xml
git commit -m "Initial manifest"
git push origin main

# 4. Use custom manifest
repo init -u https://github.com/company/manifest-repo
repo sync
```

## Repo Configuration

### Global Configuration
```bash
# Set up Git identity (required)
git config --global user.name "Your Name"
git config --global user.email "your.email@company.com"

# Configure repo-specific settings
repo config user.name "Your Name"
repo config user.email "your.email@company.com"
```

### Local Configuration (.repo/local_manifests/)
Create local manifest files to override or extend the main manifest:

```xml
<!-- .repo/local_manifests/local.xml -->
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
  <!-- Add additional projects -->
  <project path="tools/custom-tool"
           name="company/custom-tool"
           remote="github" />
  
  <!-- Override project revision -->
  <project path="frameworks/base"
           revision="refs/heads/development" />
</manifest>
```

## Troubleshooting Common Issues

### Sync Failures

```bash
# Clean up and retry sync
repo sync --force-broken

# Reset to clean state
repo forall -c 'git reset --hard ; git clean -fdx'
repo sync
```

### Corrupted Repositories
```bash
# Re-initialize specific project
rm -rf <project_path>
repo sync <project_name>

# Force sync all projects
repo sync --force-sync
```

### Branch Issues
```bash
# Check which projects have changes
repo status

# Abandon all local branches and start fresh
repo abandon <branch_name>
repo start <new_branch_name>
```

### Network Issues
```bash
# Sync with retry on failure
repo sync --retry-fetches=3

# Use different number of parallel jobs
repo sync -j1  # Single threaded for unstable connections
```

## Best Practices

### 1. Repository Management
- Always use topic branches for development
- Keep manifest repositories well-documented
- Use meaningful branch and tag names
- Regularly update your repo tool installation

### 2. Collaboration
- Use descriptive commit messages
- Keep changes atomic and focused
- Test changes across affected repositories
- Follow project-specific contribution guidelines

### 3. Performance Optimization
- Use `repo sync -j<n>` with appropriate job count
- Consider partial checkouts for large projects
- Use `--depth=1` for shallow clones when possible
- Cache repositories locally when working with multiple workspaces

## Advanced Topics

### Repo Hooks
Customize repo behavior with hooks in `.repo/repo/hooks/`:

```python
# pre-upload hook example
#!/usr/bin/env python3
import sys

def main():
    # Custom validation logic
    print("Running pre-upload checks...")
    return 0

if __name__ == '__main__':
    sys.exit(main())
```

### Custom Repo Commands
Extend repo functionality by adding commands to `.repo/repo/subcmds/`:

```python
# my_command.py
import command

class MyCommand(command.Command):
    common = True
    helpSummary = "Custom command description"
    
    def Execute(self, opt, args):
        print("Executing custom command")
```

## Resources and References

### Official Documentation
- [Repo Command Reference](https://source.android.com/setup/develop/repo) - Complete command reference
- [Repo Manifest Format](https://gerrit.googlesource.com/git-repo/+/refs/heads/master/docs/manifest-format.md) - XML manifest specification
- [Android Source Tools](https://source.android.com/setup/develop) - AOSP development tools

### Tutorials and Guides
- [Bootlin Android and Repo Tutorial](https://bootlin.com/doc/legacy/android/android-slides.pdf) - Comprehensive training materials
- [Android Code Search](https://cs.android.com/) - Browse AOSP code online
- [Google Code Search](https://developers.google.com/code-search) - Advanced code search and referencing

### Community Resources
- [repo-discuss Google Group](https://groups.google.com/g/repo-discuss) - Community discussions
- [Android Open Source Project](https://source.android.com/) - Primary use case for repo tool
- [Gerrit Code Review](https://www.gerritcodereview.com/) - Integration with repo workflows

## Quick Reference

### Essential Commands
```bash
# Initialize project
repo init -u <manifest_url> -b <branch>

# Sync repositories
repo sync -j8

# Start new branch
repo start <branch> <projects>

# Check status
repo status

# Upload for review
repo upload

# Get help
repo help
repo help <command>
```

### Useful Aliases
```bash
# Add to your shell configuration
alias rs='repo sync -j8'
alias rst='repo status'
alias rstart='repo start'
alias rup='repo upload'
```

---

*Last updated: July 2025*