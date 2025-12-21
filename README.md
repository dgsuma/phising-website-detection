# Project Setup and Commands

## 1. Initializing the Project

```bash
# Initialize project with uv (fast Python project manager)
uv init

# Rename default branch to main (recommended)
git branch -m master main

# Verify uv version
uv --version

# List available Python versions
uv python list

# Create virtual environment using specific Python version
uv venv env --python cpython-3.11.13-windows-x86_64-none