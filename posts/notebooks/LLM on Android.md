---
title: How to Run Ollama on Your Android Phone
description: Learn how to install and run Ollama, a powerful tool for serving LLMs, straight on your Android device.
date: "2024-04-23"
toc: true
badges: true
categories: [llm, ollama, android]
hide: false
image: images/purview_custom_process.png
---

# How to Set Up Your System with F-Droid, Termux and Ollama

In an interconnected digital world, automation has never been more relevant. This tutorial walks you through the process of installing certain applications namely F-droid, Termux & setting up Ollama, which is less known but equally efficient in machine learning models for your smartphone. That's right - you can have your machine learning models directly on your Android phone!

## Step 1: Installing F-Droid 

F-Droid is an installable catalog of FOSS (Free and Open Source Software) application for the Android platform. To install F-Droid, follow the instructions provided on their official website or find it directly in the Google Play Store.

```bash
install f-droid
```

## Step 2: Installing Termux

Termux is a terminal emulator for Android that works directly without any rooting or setup required. It embodies a minimal base system providing you with a complete Linux system in a reduced environment. 

```bash
install termux
```

Now let's get your Termux package up to date:

```bash
pkg update
pkg upgrade
```

## Step 3: Installing proot-distro

proot-distro is a Termux plugin that helps you to install Linux distributions in a Termux environment. 

```bash
pkg install proot-distro
```

To login to Debian, use the proot-distro login command:

```bash
pd login debian
```

## Step 4: Installing Tmux

Tmux is a terminal multiplexer, it lets you switch easily between several programs in one terminal. 

First, update your apt package and then upgrade it:

```bash
apt update
apt upgrade
```

Now for installing tmux:

```bash
apt install tmux
```

## Step 5: Installing Ollama

Ollama is an AI-infrastructure startup that enables AI teams to deploy their machine learning models directly.

To install Ollama, use the curl command to fetch the install.sh script from the ollama website:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

## Step 6: Setting Up Tmux Window and Ollama 

Once the installation is completed, you can then create a new tmux window and serve it with Ollama.

Create a new tmux session:

```bash
tmux new -s llm
```

Then run Ollama:

```bash
ollama serve
```

Next, you'll need to create a new pane in your tmux window. To do this, use the following commands. The quotes mean that it will split your window horizontally:

```bash
ctrl+b "
```

Finally, you can run Ollama's model:

```bash
ollama run gemma:2b
```

## Step 7: Model Testing

With all the steps accurately followed and implemented, you're now equipped to test your models. Ollama helps you implement and test your machine learning models with utmost ease.

Moore's law is a pretty amazing phenomenon that has allowed us to witness the current level of technological advancements. It brings the power of machine learning models right at your fingertips, literally, on your smartphone. It all starts with setting yourself up with F-Droid and Termux. Happy coding!