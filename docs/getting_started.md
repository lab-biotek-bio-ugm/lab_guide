# Getting Started

Welcome to the Bioengineering Research Group Lab Guide! This section will help you set up your machine for bioinformatics work. Follow these steps to install the necessary software and configure your environment.

## Installing UNIX/Linux

### For Windows Users: Using WSL2

Windows Subsystem for Linux (WSL2) allows you to run a Linux distribution directly on Windows. Follow these steps to install WSL2:

1. **Enable WSL2**:
   - Open PowerShell as Administrator and run:
     ```powershell
     wsl --install
     ```
   - Restart your computer if prompted.

2. **Install a Linux Distribution**:
   - Open Microsoft Store, search for "Ubuntu", and install it.
   - Launch Ubuntu from the Start menu and follow the prompts to set up your Linux user.

### For Mac Users

MacOS is UNIX-based, so you don't need to install anything additional. Open the Terminal application and you're ready to go.

## Installing VS Code

Visual Studio Code (VS Code) is a powerful code editor with great support for development and bioinformatics.

1. **Download and Install VS Code**:
   - Go to [Visual Studio Code](https://code.visualstudio.com/).
   - Download the installer for your operating system and follow the installation instructions.

2. **Install Recommended Extensions**:
   - Launch VS Code.
   - Go to the Extensions view by clicking the square icon on the sidebar or pressing `Ctrl+Shift+X`.
   - Search for and install the following extensions:
     - Python
     - Remote - WSL (for Windows users)
     - GitHub Copilot (if you have access)

## Create a GitHub Account

GitHub is essential for version control and collaboration.

1. **Sign Up for GitHub**:
   - Go to [GitHub](https://github.com/).
   - Click on "Sign up" and follow the instructions to create your account.

2. **Set Up Git on Your Machine**:
   - Open your terminal (Ubuntu on WSL2 for Windows or Terminal on Mac).
   - Configure your Git username and email:
     ```bash
     git config --global user.name "Your Name"
     git config --global user.email "your.email@example.com"
     ```

## Get a GitHub Copilot Account

GitHub Copilot is an AI-powered code completion tool.

1. **Request Access or Subscribe**:
   - Go to [GitHub Copilot](https://github.com/features/copilot).
   - Follow the instructions to request access or subscribe if it’s generally available.

2. **Install GitHub Copilot Extension**:
   - Open VS Code.
   - Go to the Extensions view (`Ctrl+Shift+X`).
   - Search for "GitHub Copilot" and install the extension.

## Install Mamba/Miniforge

Mamba is a fast package manager, and Miniforge is a minimal installer for conda.

1. **Install Miniforge**:
   - Download the Miniforge installer for your operating system from [Miniforge GitHub Releases](https://github.com/conda-forge/miniforge/releases).
   - Run the installer:
     - For Windows (in Ubuntu WSL2):
       ```bash
       wget <URL-to-Miniforge-installer>
       bash Miniforge3-Linux-x86_64.sh
       ```
     - For Mac:
       ```bash
       curl -L -O <URL-to-Miniforge-installer>
       bash Miniforge3-MacOSX-x86_64.sh
       ```

2. **Install Mamba**:
   - After installing Miniforge, open a new terminal session and run:
     ```bash
     conda install mamba -n base -c conda-forge
     ```

## Setting Up SSH Keys

SSH keys allow secure connections to GitHub without needing to enter your password each time.

1. **Generate SSH Keys**:
   - Open your terminal.
   - Run the following command and follow the prompts:
     ```bash
     ssh-keygen -t ed25519 -C "your.email@example.com"
     ```

2. **Add SSH Key to the SSH Agent**:
   - Start the ssh-agent:
     ```bash
     eval "$(ssh-agent -s)"
     ```
   - Add your SSH key to the agent:
     ```bash
     ssh-add ~/.ssh/id_ed25519
     ```

3. **Add SSH Key to Your GitHub Account**:
   - Copy your SSH key to the clipboard:
     ```bash
     cat ~/.ssh/id_ed25519.pub | pbcopy
     ```
   - Go to [GitHub SSH Keys Settings](https://github.com/settings/keys).
   - Click on "New SSH key", paste your key, and save.

---

Congratulations! Your machine is now set up for bioinformatics work. Proceed to the specific sections on Genome Assembly, Annotation, and Mining to start using the tools and protocols in our lab.
