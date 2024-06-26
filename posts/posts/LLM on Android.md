---
title: "Running LLMs on Android: A Step-by-Step Guide"
description: "Unleash the Power of LLMs on Your Android Device with Termux and Ollama"
author: Davide Fornelli
date: 2024-05-10
toc: true
categories:
  - llm
  - ollama
  - android
hide: false
image: assets/llama_phone_2.png
---
In this blog post, we'll explore how to install and run the Ollama language model on an Android device using Termux, a powerful terminal emulator. This tutorial is designed for users who wish to leverage the capabilities of large language models directly on their mobile devices without the need for a desktop environment.

### Step 1: Install F-Droid
F-Droid is an installable catalogue of FOSS (Free and Open Source Software) applications for the Android platform. Download and install the F-Droid app from [https://f-droid.org/](https://f-droid.org/).

### Step 2: Install Termux
Once F-Droid is installed, open it and search for Termux. Install Termux, which will serve as your Linux environment on Android.

### Step 3: Update and Upgrade Packages
Open Termux and update its package repository to ensure you have access to the latest software versions:
```bash
pkg update
pkg upgrade
```

### Step 4: Install Proot-Distro
Proot-Distro allows you to run different Linux distributions within Termux. Install it using:
```bash
pkg install proot-distro
```

```bash
pd install debian
```

For more details, visit the [Proot-Distro GitHub page](https://github.com/termux/proot-distro).

### Step 5: Login to a Linux Distribution
For this tutorial, we will use Debian. Log in to your Debian environment with:
```bash
pd login debian
```

### Step 6: Install Tmux
Tmux is a terminal multiplexer that allows you to run multiple terminal sessions simultaneously:
```bash
apt update
apt upgrade
apt install tmux
```

### Step 7: Install Ollama
Within the Debian environment, download and install Ollama:
```bash
curl -fsSL https://ollama.com/install.sh | sh
```
This script installs Ollama and its dependencies.

### Step 8: Create a New Tmux Session
Start a new tmux session dedicated to running Ollama:
```bash
tmux new -s llm
```

### Step 9: Run Ollama Server
In the tmux session, start the Ollama server:
```bash
ollama serve
```

### Step 10: Create a New Pane in Tmux
Split the current window into two panes by pressing `Ctrl+b "`.

### Step 11: Run an Ollama Model
In the new pane, run a specific Ollama model. For example, to run the Gemma 2B model:
```bash
ollama run gemma:2b
```

Depending on your device, you can run also run phi3:
```bash
ollama run phi3
```

### Step 12: Test the Model
Once the model is running, you can interact with it directly from the terminal. Enter prompts and observe the model's responses, effectively using your Android device as a powerful AI tool.

### Conclusion
This tutorial provides a foundation for exploring further applications of LLMs on mobile devices, opening up possibilities for mobile-based AI development and experimentation.
