# Glimpse 👁️

> **Code review at the speed of thought.**
> *Paradigm shift from Line-Oriented to Intent-Oriented diffs.*

[![CI](https://github.com/glimpse-rs/glimpse/actions/workflows/ci.yml/badge.svg)](https://github.com/glimpse-rs/glimpse/actions)
[![Crates.io](https://img.shields.io/crates/v/glimpse.svg)](https://crates.io/crates/glimpse)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Rust](https://img.shields.io/badge/rust-1.80%2B-orange.svg)](https://www.rust-lang.org)

---

**Glimpse** is a next-generation Git CLI tool designed for the 2026 developer. It moves beyond the 50-year-old "patch" format to provide a **Semantic**, **Visual**, and **Context-Aware** understanding of your code changes.

![Glimpse Demo](https://raw.githubusercontent.com/glimpse-rs/glimpse/main/assets/demo.gif)
*(Above: Semantic Zooming in action - from Galaxy View to Logic View)*

## 🌟 Why Glimpse?

Software complexity has outpaced our tools. `git diff` shows you *what* lines changed, but Glimpse tells you *why* and *where* it matters.

*   **🌌 Galaxy View (Semantic Zoom L1)**: See the "Heatmap" of your changes. Which modules are most affected?
*   **🏗️ Structure View (Semantic Zoom L2)**: Don't read files; read *functions*. See a tree of modified symbols (functions, structs) powered by **Tree-sitter**.
*   **📝 Logic View (Semantic Zoom L3)**: Context-aware diffs with syntax highlighting and noise reduction.
*   **🐙 GitHub PR Mode**: Review Pull Requests directly in your terminal with the same semantic power.

## 🚀 Installation

### Using Cargo (Recommended)

```bash
cargo install glimpse
```

### From Source

```bash
git clone https://github.com/glimpse-rs/glimpse.git
cd glimpse
make build
cargo install --path .
```

## 🎮 Usage

Glimpse adapts to your context. Whether you're coding locally or reviewing a teammate's PR.

### 1. Local Development

View working tree changes in the current directory:

```bash
glimpse .
```

Or target a specific repository:

```bash
glimpse ~/dev/my-project
```

### 2. GitHub PR Review

Review a Pull Request by URL or ID (Requires `gh` CLI):

```bash
# By URL
glimpse https://github.com/owner/repo/pull/123

# By Short Format
glimpse owner/repo#123
```

## ⌨️ Controls

Glimpse uses a Vim-inspired, game-like navigation system.

| Key | Action |
| --- | --- |
| `j` / `k` | Navigate items |
| `Enter` | **Zoom In** (Galaxy -> Structure -> Logic) |
| `Backspace` | **Zoom Out** |
| `q` | Quit |
| `?` | AI Context Summary (Coming Soon) |

## 🛠️ Technology Stack (2026 Standard)

We leverage the cutting edge of the Rust ecosystem:

*   **Core**: Rust 2021/2024 Edition
*   **TUI**: [Ratatui v0.30](https://github.com/ratatui-org/ratatui) (The future of TUI)
*   **Parsing**: [Tree-sitter v0.24](https://tree-sitter.github.io/) (Incremental parsing)
*   **Git**: `git2` / `libgit2`
*   **Async**: Tokio v1.43

## 🤝 Contributing

We believe in **Emotional Design**. Tools should be a joy to use.
We enforce strict quality standards via our DevSecOps pipeline:

```bash
# Setup environment (install nextest, typos, cargo-deny)
make setup

# Run full CI check locally
make check
```

## 📜 License

MIT © [Glimpse Contributors](https://github.com/glimpse-rs/glimpse/graphs/contributors)