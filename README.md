---
title: codewatcher
emoji: 🐳
colorFrom: green
colorTo: yellow
sdk: static
pinned: false
tags:
  - deepsite
---

# CodeWatcher 🔍🛡️

[![GitHub Actions](https://github.com/your-org/CodeWatcher/workflows/CodeWatcher/badge.svg)](https://github.com/your-org/CodeWatcher/actions)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

CodeWatcher is a GitHub Actions bot that performs security-focused code reviews on pull requests using static analysis tools with a mentor/red-team approach.

## Features

- **Automated Security Reviews**: Runs pylint, bandit, and semgrep on every PR
- **In-line Comments**: Provides contextual feedback directly on code changes
- **Mentor Mode**: Offers constructive suggestions for code quality improvements
- **Red Team Mode**: Highlights security vulnerabilities with attack scenarios
- **SARIF Integration**: Uploads findings to GitHub's code scanning interface

## How It Works

CodeWatcher automatically:
1. Triggers on pull request events
2. Analyzes changed Python files using multiple static analysis tools
3. Posts in-line comments with security insights and improvement suggestions
4. Provides a summary of findings in the PR conversation

## Installation

1. Add the workflow file to your repository:
   ```bash
   mkdir -p .github/workflows
   curl -o .github/workflows/codewatcher.yml https://raw.githubusercontent.com/your-org/CodeWatcher/main/.github/workflows/codewatcher.yml
   ```

2. Create the scripts directory:
   ```bash
   mkdir -p .github/scripts
   curl -o .github/scripts/codewatcher.py https://raw.githubusercontent.com/your-org/CodeWatcher/main/.github/scripts/codewatcher.py
   ```

3. Commit and push these changes to your repository:
   ```bash
   git add .github
   git commit -m "Add CodeWatcher security review workflow"
   git push
   ```

## Configuration

Customize CodeWatcher by adding these files to your repository root:

- `.pylintrc` - Pylint configuration
- `.bandit` - Bandit configuration
- `.semgrep.yml` - Custom Semgrep rules

## Example Output

![CodeWatcher in action](https://github.com/your-org/CodeWatcher/raw/main/images/example-comment.png)
