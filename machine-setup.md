# Machine Setup

Follow this document from top to bottom to setup your machine!

## Mac

1. Install [Homebrew](https://brew.sh/) by pasting the install command into your terminal.
2. When Homebrew is done, it will output some commands for you to add it to your PATH. Copy and paste those commands into your terminal and run them.
3. Close your terminal and open a new terminal. Run `brew install git`.
4. Follow [these Node instructions](https://nodejs.org/en/download/package-manager) in your terminal to install Node.
   1. Make sure to restart your terminal before running the `nvm install` command!
5. Continue to the "Everyone" section below.

## Windows

1. Download and run the [PowerShell](https://github.com/PowerShell/PowerShell/releases) installer. Look for `PowerShell-#.#.#-win-x64.msi` under the **Assets** section of the latest release.
2. Install [Windows Terminal](https://apps.microsoft.com/detail/9n0dx20hk701).
   1. In Windows Terminal, go into **Settings** and change the **Default Profile** to either `PowerShell` or `pwsh` (instead of `Windows Powershell`).
3. Download and run the **Standalone 64-bit** [Git Installer](https://git-scm.com/download/win). Select the default options _except for_ the following:
   1. The default editor should be changed to "Use Visual Studio Code as Git's default editor".
   1. Override the default branch name to "main".
   1. Select "Git from the command line and also from 3rd-party software".
4. Download and run the [Node Version Manager](https://github.com/coreybutler/nvm-windows/releases) installer. Look for `nvm-setup.exe` under the **Assets** section of the latest release.
   1. Once that is installed, run the following commands in your terminal:
      ```
      nvm install lts
      nvm use lts
      ```
5. Continue to the "Everyone" section below.

## Everyone

1. In your terminal, run the following commands with **your actual information** inside the double quotes.
   1. `git config --global user.name "Your Name"`
   2. `git config --global user.email "your_email@example.com"`
2. Run these commands without changing anything.
   1. `git config --global init.defaultBranch main`
   2. `git config --global core.editor code`
3. Install the [GitHub CLI](https://cli.github.com/).
   1. On Mac, run `brew install gh` in your terminal instead of "Download for Mac".
4. Close your terminal and open a new one.
5. In the new terminal, run `gh auth login`.
   1. Choose the `Github.com` account.
   2. The preferred protocol is `HTTPS`.
   3. Type `Y` to authenticate Git with your GitHub credentials.
   4. Follow the prompts to **login with a web browser**.
6. Install [Visual Studio Code](https://code.visualstudio.com/).
7. In VS Code, install these two extensions:
   1. [Live Preview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server)
   2. [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
8. Configure your VS Code settings as follows:
   1. Set **Editor: Default Formatter** to **Prettier**.
   2. Enable **Editor: Format on Save**.
9. (**Mac only**) Follow [these instructions to install `code` command in PATH](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line).

## Checklist

Double check your machine setup by running the following commands in your terminal:

- [ ] `git --version` returns a version number such as `git version 2.39.5`
  - don't worry about the actual version number!
- [ ] `node --version` returns a version number such as `v22.12.0`
  - don't worry about the actual version number!
- [ ] `gh auth status` returns a message stating that you are `Logged in to github.com account`
- [ ] `code .` should open a VS Code window. You can close the window immediately afterwards.
