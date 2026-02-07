# Versa

Tired of writing YAML files for CI/CD? Don't want to learn Conventional Commits just to bump a version? Versa is the release manager that works the way YOU work.

## What is Versa?
**Versa** is a lightweight, language-agnostic semantic version manager designed for professional workflows.
One `version.txt`.  
Zero ecosystem lock-in.  
Works everywhere.

---


## Why Versa?

Most versioning tools are tied to a specific ecosystem (npm, cargo, gradle, etc.).
Versa takes a different approach:

- 📦 **Single source of truth** (`version.txt`)
- 🌍 **Language-agnostic**
- ⚙️ **Perfect for C / C++ / Go / Rust / tooling**
- 🔁 **CI/CD friendly**
- 🧩 **Generates version snippets for multiple languages**

If your project is not owned by a single framework, **Versa fits naturally**.

---

## Features

### Core
- Initialize and manage semantic versions (`MAJOR.MINOR.PATCH`)
- Safe version bumping
- Manual version setting
- Simple, readable CLI

### Pro
- Generate version-reading snippets for:
  - C / C++
  - Python
  - JavaScript
  - C#
  - Go
  - Rust
- CI/CD version checks (`>=`, `<=`, `==`, etc.)
- Ideal for automated pipelines and release gates

---

## Installation

Download the prebuilt binary for your platform from **Releases**  
(or build from source with a C++17 compiler).

Place `versa` somewhere in your `$PATH`.

---

## Quick Start

```bash
versa init
``` 
Creates a version.txt file:

0.0.0

## Show current version
versa show
Output:

>Current Version: 0.0.0

## Set a specific version
versa set 1.2.3

## Bump versions
versa bump patch   # 1.2.3 → 1.2.4
versa bump minor   # 1.2.3 → 1.3.0
versa bump major   # 1.2.3 → 2.0.0
versa bump +n      # patch +n
versa bump -n      # patch -n (clamped at 0)

## Other Features
Generate version snippets
versa snippet rust


Supported languages:

-cpp
-python
-js
-cs
-go
-rust

Each snippet reads directly from version.txt, keeping your version consistent across tools and languages.

# CI / CD version checks
versa check minor >= 1

Output:
true


Exit codes:
0 → condition satisfied

1 → condition failed

Perfect for CI pipelines and release guards.

Example Use Cases

Monorepos with multiple languages

C/C++ projects without package managers

Internal developer tools

SDKs and CLIs

Build systems and automation scripts

Philosophy

Versa is intentionally simple.

No hidden metadata.
No lock-in.
No magic.

Just a clean, explicit version file that works everywhere.