# Awesome Context Configs

This public repo holds TOML configuration files for tech stacks in the Awesome Context Platform. Each folder represents a tech stack (e.g., `python/`) and must contain a `config.toml` file defining sources.

## Contribution Guidelines

- Create a folder for your tech stack (e.g., `javascript/`).
- Add `config.toml` with sources (see examples below).
- Optionally, include local files like `custom-tips.md` referenced in the TOML.
- Submit a PR!

## Example config.toml

[tech_stack]
name = "Python"
description = "Core Python knowledge base"

[[sources]]
type = "github_folder"
repo = "python/cpython"
path = "Doc/tutorial"

[[sources]]
type = "github_file"
repo = "python/cpython"
path = "README.rst"

[[sources]]
type = "local_file"
path = "custom-tips.md"

[[sources]]
type = "inline"
content = """Custom note: Python is great for scripting."""
