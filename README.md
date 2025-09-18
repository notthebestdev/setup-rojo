# 🚀 setup-rojo

[![GitHub release](https://img.shields.io/github/v/release/notthebestdev/setup-rojo?logo=github&color=red)](https://github.com/notthebestdev/setup-rojo/releases)
[![GitHub Marketplace](https://img.shields.io/badge/marketplace-setup--rojo-blue?logo=github)](https://github.com/marketplace/actions/setup-rojo)

A GitHub Action to install [Rojo](https://rojo.space/) (the Roblox project sync tool) in your CI pipelines.  
It works across **Linux**, **macOS (Intel & Apple Silicon)**, and **Windows**.

---

## 📦 Features

- Install the latest Rojo release or pin to a specific version  
- Cross-platform support (Linux, macOS, Windows)  
- Easy to use with GitHub Actions  
- Adds `rojo` to the system `PATH`  

---

## ⚡ Usage

### Install latest Rojo
```yaml
name: CI with Rojo
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Setup Rojo
        uses: notthebestdev/setup-rojo@v1
      - name: Check version
        run: rojo --version
```
### Pin to a specific version
```yaml
- name: Setup Rojo v7.5.1
  uses: notthebestdev/setup-rojo@v1
  with:
    version: v7.5.1
```

## ⚙️ Inputs

| Name      | Description                               | Default   | Example   |
|-----------|-------------------------------------------|-----------|-----------|
| `version` | Rojo version to install (tag name). Use `latest` for the newest release. | `latest` | `v7.5.1` |
