# Neuroengineering and AI — Course Repository

This repository contains the **Jupyter notebooks and materials used during the Neuroengineering and AI course**.

The notebooks are organized according to the different topics covered during the course and are designed to be used during the practical exercises and tutorials.

Before using the notebooks, you need to complete the software setup described below.

---

# Setup

The following setup needs to be completed **before the first exercise**.

The setup is the same for Windows, macOS, and Linux, with only a few differences in the commands used by each operating system.

We will use:

* **Python 3.13.15**
* **Visual Studio Code**
* **Git**
* **Git Bash** on Windows


> **If you already have Python installed** (any version, including from Anaconda, the Microsoft Store, Homebrew, or your Linux distro), **do not uninstall it or remove it from PATH.** We will install Python 3.13.15 *alongside* it and call it explicitly by its exact version, so it can't be shadowed by another Python on your system. The steps below show you how.

The setup consists of the following steps:

1. Install Python 3.13.15
2. Install Visual Studio Code
3. Install Git

---

## 1. Install Python 3.13.15

We will use **Python 3.13.15** for the course. Because many machines already have another Python installed (from Anaconda, a Linux distro, Homebrew, etc.), the instructions below never rely on the bare `python` or `python3` command — they always call 3.13.15 explicitly, so there's no ambiguity about which interpreter you're using.

### Windows

Download the **Python 3.13.15 Windows installer (64-bit)** from the official Python website:

https://www.python.org/downloads/release/python-31315/

Run the installer.

**Important:** at the beginning of the installation, check:

```text
☑ Add python.exe to PATH
```

Then click **Install Now**. (If you already have another Python on PATH, this is fine — Windows installs a version-aware **`py` launcher** that we'll use to pick 3.13.15 specifically, regardless of what `python` currently points to.)

After installation, open **Git Bash** and check that the launcher can see it:

```bash
py -0
```

You should see `3.13` in the list of installed versions. Then confirm the exact version:

```bash
py -3.13 --version
```

You should see:

```text
Python 3.13.15
```

> **Do not use the bare `python --version` command to verify this** — if you have another Python installed, `python` may resolve to that one instead. Always use `py -3.13` for this course.

If `py -0` does not show 3.13, close and reopen Git Bash (PATH changes require a fresh terminal), or re-run the installer and confirm "Add python.exe to PATH" was checked.

### macOS

Download the **Python 3.13.15 macOS installer**:

https://www.python.org/downloads/release/python-31315/

Download the `.pkg` installer and follow the installation instructions. The official installer creates a version-specific command, `python3.13`, without touching whatever `python3` currently points to (system Python, Homebrew Python, a `pyenv` version, etc.).

Open Terminal and check the version-specific command:

```bash
python3.13 --version
```

You should see:

```text
Python 3.13.15
```

> **Do not rely on `python3 --version` to verify this.** If you have Homebrew Python, a `pyenv` shim, or another 3.x installed, `python3` may point there instead of to 3.13.15. Always use `python3.13` explicitly for this course.

If `python3.13: command not found`, the installer likely didn't finish, or your terminal needs to be restarted — reopen Terminal and try again before reinstalling.

If you manage Python with **Homebrew** or **pyenv**, you can install 3.13.15 through those instead if you prefer, but make sure whichever `python3.13`-equivalent command you use resolves to exactly `3.13.15` before continuing.

### Linux

First check what's already installed — don't assume:

```bash
python3 --version
which -a python3.13
```

Most distributions ship an older Python 3 as `python3` (used by the OS itself), so **do not replace or reinstall over it.** We need `python3.13` to exist as its own separate command.

If `python3.13` is not found, install it alongside your system Python:

**Ubuntu/Debian** (via the deadsnakes PPA, which installs versioned binaries without touching the default `python3`):

```bash
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.13 python3.13-venv
```

**Fedora:**

```bash
sudo dnf install python3.13
```

**Arch:** Python 3.13 may already be the system default; if you need a pinned version alongside it, use `pyenv` instead of replacing the system package.

If your distribution doesn't package 3.13.15 and you don't want to touch system packages, install it via **pyenv** (recommended for Linux in general, since it never conflicts with the OS Python):

```bash
curl https://pyenv.run | bash
# follow the printed instructions to add pyenv to your shell, then restart your terminal
pyenv install 3.13.15
```

Whichever route you use, confirm with the *explicit* command (not the bare `python3`):

```bash
python3.13 --version
```

You should see:

```text
Python 3.13.15
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

> Note: VS Code will list *every* Python interpreter it finds on your machine when you select a kernel later. Once you create the course's virtual environment (in a later step), always pick the interpreter inside that environment's `.venv` folder — not whatever "Python 3.x" appears at the top of the list, which may be an unrelated installation.

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
