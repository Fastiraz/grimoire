---
sidebar_position: 3
title: Installation
description: How to install and run the Neko platform using pipx or from source
---

# Installation

Neko is built using the Python package and project manager [uv](https://docs.astral.sh/uv/). You can choose between a **pipx installation (recommended)** or install from source if you want full control.

---

## Prerequisites

Neko use Ollama as a LLM provider by default so make sure it's installed.

- [Ollama](https://ollama.com/)

You can install Ollama using:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

You can also install Ollama on a different machine and edit the `llm_provider_base_url` object in the config file at `~/.neko/settings.json`.

## Installation with pipx (recommended)

The fastest way to get started is with `pipx`.

```bash
# Install pipx
apt install pipx # On Linux
brew install pipx # On macOS

# Ensure pipx is in PATH and reload the shell
pipx ensurepath && exec $SHELL

# Install neko
pipx install neko
```

## Installation from source

```bash
git clone https://github.com/Fastiraz/neko.git
cd neko

uv build
uv venv
uv pip install dist/*.whl
uv run -- neko help
```

---

<div align="center">
  <code>Coming soon...</code>
</div>
