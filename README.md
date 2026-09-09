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
* **Jupyter**


The setup consists of the following steps:

1. Install Python 3.13.15
2. Install Visual Studio Code
3. Install Git

---

## 1. Install Python 3.13.15

We will use **Python 3.13.15** for the course.

### Windows

Download the **Python 3.13.15 Windows installer (64-bit)** from the official Python website:

https://www.python.org/downloads/release/python-31315/

Run the installer.

**Important:** at the beginning of the installation, check:

```text
☑ Add python.exe to PATH
```

Then click **Install Now**.

After installation, open **Git Bash** and check:

```bash
python --version
```

You should see:

```text
Python 3.13.15
```

### macOS

Download the **Python 3.13.15 macOS installer**:

https://www.python.org/downloads/release/python-31315/

Download the `.pkg` installer and follow the installation instructions.

Open Terminal and check:

```bash
python3 --version
```

You should see:

```text
Python 3.13.15
```

### Linux

First check whether Python 3.13 is already installed:

```bash
python3 --version
```

If Python 3.13 is not available, install it using your Linux distribution's package manager or the official Python website:

https://www.python.org/downloads/

Then check:

```bash
python3 --version
```

You should have Python 3.13 installed.

> **Do not replace your Linux system Python if your distribution depends on it.**

---

## 2. Install Visual Studio Code

Download **Visual Studio Code** from:

https://code.visualstudio.com/download

Choose the version for your operating system and install it.

After opening VS Code, go to **Extensions** and install:

* **Python** — Microsoft
* **Jupyter** — Microsoft

These extensions allow you to work with Python scripts and Jupyter notebooks directly from VS Code.

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

