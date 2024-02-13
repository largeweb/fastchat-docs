---
sidebar_position: 1
---

# Quick Start

This guide helps you to get started with FastChat quickly and efficiently.

## Prerequisites

Ensure you have the following installed:

-   [Node.js](https://nodejs.org/en/download/) version 18.0 or above
-   [Python](https://www.python.org/downloads/) version 3.6 or above
-   [pip](https://pip.pypa.io/en/stable/installation/) version 21.3 or above

## Installation

### Method 1: With pip

```bash
pip3 install "fschat[model_worker,webui]"
```

### Method 2: From source

```bash
git clone https://github.com/lm-sys/FastChat.git
cd FastChat

# If you are running on Mac:
brew install rust cmake

# Install Package
pip3 install --upgrade pip  # enable PEP 660 support
pip3 install -e ".[model_worker,webui]"
```

Please refer to [Installation using Pip](/docs/installation/from_source.md) or [Installation from Source](/docs/installation/with_pip.md) for more details.
