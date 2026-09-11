# Neuroengineering and AI — Course Repository

This repository contains the **Jupyter notebooks and materials used during the Neuroengineering and AI course**.

The notebooks are organized according to the different topics covered during the course and are designed to be used during the practical exercises and tutorials.

Before using the notebooks, you need to complete the software setup described below.

---

# Setup

The following setup needs to be completed **before the first exercise**.

The setup is the same for Windows, macOS, and Linux, with only a few differences in the commands used by each operating system.

We will use:

* **Python 3.11+** (recommended), **Python 3.9+** minimum required
* **Visual Studio Code**
* **Git**
* **Git Bash** on Windows

> **If you already have Python installed** (any version 3.9 or later, including from Anaconda, the Microsoft Store, Homebrew, or your Linux distro), you're good to go — no need to install anything else. If your Python is older than 3.9, or you don't have Python installed at all, follow the steps below to install a current version.

### Checking your Python version

Open a terminal (Command Prompt / PowerShell on Windows, Terminal on macOS/Linux) and run:

```bash
python3 --version
```

If that command isn't found, try:

```bash
python --version
```

You should see something like `Python 3.11.4`. As long as the version is **3.9 or higher**, you can skip the Python installation step below and go straight to Step 2.

The setup consists of the following steps:

1. Install Python (3.11+ recommended, 3.9+ required)
2. Install Visual Studio Code
3. Install Git

---

## 1. Install Python

We recommend **Python 3.11 or later**; **Python 3.9 is the minimum required version**. If you already have a compatible Python installed (see version check above), skip to step 2.

### Windows

Download the latest **Python 3 installer (64-bit)** from the official Python website:

https://www.python.org/downloads/

Run the installer.

**Important:** at the beginning of the installation, check:

```text
☑ Add python.exe to PATH
```

Then click **Install Now**.

After installation, open **Git Bash** and confirm the install:

```bash
python --version
```

You should see something like:

```text
Python 3.11.4
```

If the command is not found, close and reopen Git Bash (PATH changes require a fresh terminal), or re-run the installer and confirm "Add python.exe to PATH" was checked.

### macOS

Download the latest **Python 3 macOS installer** from:

https://www.python.org/downloads/

Download the `.pkg` installer and follow the installation instructions.

Open Terminal and check the version:

```bash
python3 --version
```

You should see something like:

```text
Python 3.11.4
```

If you manage Python with **Homebrew** or **pyenv**, you can install a recent version through those instead if you prefer — just make sure the resulting version is 3.9 or higher.

If `python3: command not found`, the installer likely didn't finish, or your terminal needs to be restarted — reopen Terminal and try again before reinstalling.

### Linux

First check what's already installed:

```bash
python3 --version
```

If the version is 3.9 or higher, you're done — skip to step 2.

If it's older, or not installed, add it via your package manager:

**Ubuntu/Debian:**

```bash
sudo apt update
sudo apt install python3
```

If your distribution's default `python3` is still older than 3.9 (common on older LTS releases), install a newer version alongside it via the deadsnakes PPA:

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.11 python3.11-venv
```

**Fedora:**

```bash
sudo dnf install python3
```

**Arch:** the system Python is generally recent enough already.

If your distribution doesn't package a recent enough version and you'd rather not touch system packages, install via **pyenv**:

```bash
curl https://pyenv.run | bash
# follow the printed instructions to add pyenv to your shell, then restart your terminal
pyenv install 3.11
```

> **Do not replace your Linux system Python (`/usr/bin/python3`) if your distribution depends on it.** Breaking it can break system tools like package managers.

---

## 2. Install Visual Studio Code

Download **Visual Studio Code** from:

https://code.visualstudio.com/download

Choose the version for your operating system and install it.

After opening VS Code, go to **Extensions** and install:

* **Python** — Microsoft
* **Jupyter** — Microsoft

These extensions allow you to work with Python scripts and Jupyter notebooks directly from VS Code.

> Note: VS Code will list *every* Python interpreter it finds on your machine when you select a kernel later. Once you create the course's virtual environment (in a later step), always pick the interpreter inside that environment's `.venv` folder.

---

## 3. Install Git

Git is used to download the course repository and retrieve updates.

Download Git from:

https://git-scm.com/downloads

### Windows

Install **Git for Windows**.

Git for Windows includes **Git Bash**, which we will use throughout the course.

After installation, open **Git Bash** and run:

```bash
git --version
```

### macOS

Open Terminal and run:

```bash
git --version
```

If Git is not installed, macOS will normally offer to install the required Command Line Tools.

### Linux

Open a terminal and run:

```bash
git --version
```

If Git is not installed, install it using your distribution's package manager.

For Ubuntu/Debian:

```bash
sudo apt update
sudo apt install git
```
