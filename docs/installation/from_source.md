---
sidebar_position: 2
---

# Installation from Source

To install FastChat from source:

1. Clone the repository:

```bash
git clone https://github.com/lm-sys/FastChat.git
```

2. Navigate to the FastChat folder:

```bash
cd FastChat
```

3. If you are running on a Mac, install Rust and CMake:

```bash
brew install rust cmake
```

4. Install FastChat package with its dependencies:

```bash
pip3 install --upgrade pip  # enable PEP 660 support
pip3 install -e ".[model_worker,webui]"
```
