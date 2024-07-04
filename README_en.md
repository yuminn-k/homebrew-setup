# mac-dev-setup

## Setting Up Development Environment with Homebrew and Brewfile

### Installing Homebrew

Homebrew is a package manager that makes it easy to install and manage software packages on macOS.

#### How to Install Homebrew

1. Open Terminal.
2. Enter the following command to install Homebrew:
    ```sh
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
3. Once the installation is complete, verify that Homebrew is installed correctly:
    ```sh
    brew --version
    ```

### Basic Usage of Homebrew

#### Searching for Packages

To search for packages with Homebrew, use the following command:
```sh
brew search <package-name>
```

#### Installing Packages

To install packages with Homebrew, use the following command:
```sh
brew install <package-name>
```

#### Uninstalling Packages

To uninstall installed packages, use the following command:
```sh
brew uninstall <package-name>
```

#### Updating Packages

To update installed packages to the latest version, use the following command:
```sh
brew upgrade
```

#### Updating Homebrew

To update Homebrew itself to the latest version, use the following command:
```sh
brew update
```

#### Checking System Status

To check the system status of Homebrew, use the following command:
```sh
brew doctor
```

### Managing Packages with Brewfile

#### Creating a Brewfile

To generate a Brewfile based on the list of packages currently installed on your system, use the following command:
```sh
brew bundle dump --file=Brewfile
```

#### Installing Packages Using Brewfile

To install the necessary packages all at once using Brewfile, use the following command:
```sh
brew bundle --file=Brewfile
```

#### Updating Brewfile

To update Brewfile after installing new packages, use the following command:
```sh
brew bundle dump --file=Brewfile --force
```

#### Example Brewfile

Here is an example Brewfile for setting up a development environment:
```ruby
# Brewfile

# Homebrew taps
tap "adoptopenjdk/openjdk"
tap "hashicorp/tap"
tap "homebrew/bundle"
tap "homebrew/cask-fonts"
tap "homebrew/cask-versions"
tap "homebrew/services"
tap "lencx/chatgpt", "https://github.com/lencx/ChatGPT.git"
tap "mongodb/brew"
tap "shivammathur/php"

# Brew packages
brew "git"
brew "mas"
brew "wget"
brew "node"
brew "python"
brew "tmux"
brew "htop"
brew "go"
brew "redis"
brew "postgresql"
brew "mysql"
brew "mongodb-community"
brew "docker"
brew "kubernetes-cli"
brew "kubectl"
brew "jenkins"
brew "php"
brew "composer"
brew "nginx"
brew "httpd"
brew "yarn"
brew "watchman"
brew "jq"
brew "openssl"
brew "pipenv"
brew "pkg-config"
brew "rbenv"
brew "tree"
brew "zsh"
brew "zsh-syntax-highlighting"

# Cask applications
cask "google-chrome"
cask "visual-studio-code"
cask "slack"
cask "iterm2"
cask "docker"
cask "adoptopenjdk"
cask "chatgpt"
cask "font-fira-code"
cask "goland"
cask "pycharm"
cask "sequel-ace"
cask "temurin"

# Fonts (using Homebrew Cask Fonts tap)
tap "homebrew/cask-fonts"
cask "font-fira-code"

# Mac App Store applications
mas "KakaoTalk", id: 869223134

# VSCode extensions
vscode "adpyke.codesnap"
vscode "amazonwebservices.aws-toolkit-vscode"
vscode "cardinal90.multi-cursor-case-preserve"
vscode "christian-kohler.path-intellisense"
vscode "cschlosser.doxdocgen"
vscode "danielsanmedium.dscodegpt"
vscode "dbaeumer.vscode-eslint"
vscode "denoland.vscode-deno"
vscode "devsense.composer-php-vscode"
vscode "devsense.intelli-php-vscode"
vscode "devsense.phptools-vscode"
vscode "devsense.profiler-php-vscode"
vscode "dsznajder.es7-react-js-snippets"
vscode "eamodio.gitlens"
vscode "eg2.vscode-npm-script"
vscode "equinusocio.vsc-community-material-theme"
vscode "esbenp.prettier-vscode"
vscode "formulahendry.auto-close-tag"
vscode "formulahendry.auto-rename-tag"
vscode "formulahendry.code-runner"
vscode "formulahendry.vscode-mysql"
vscode "georgewfraser.vscode-javac"
vscode "github.copilot"
vscode "github.copilot-chat"
vscode "github.vscode-github-actions"
vscode "github.vscode-pull-request-github"
vscode "glenn2223.live-sass"
vscode "hazer.reactcodesnippets"
vscode "hookyqr.beautify"
vscode "humao.rest-client"
vscode "jeff-hykin.better-cpp-syntax"
vscode "kimseungtae.aicodehelper"
vscode "mathiasfrohlich.kotlin"
vscode "mhutchie.git-graph"
vscode "ms-azuretools.vscode-docker"
vscode "ms-ceintl.vscode-language-pack-ja"
vscode "ms-ceintl.vscode-language-pack-ko"
vscode "ms-python.autopep8"
vscode "ms-python.debugpy"
vscode "ms-python.isort"
vscode "ms-python.python"
vscode "ms-python.vscode-pylance"
vscode "ms-toolsai.jupyter"
vscode "ms-toolsai.jupyter-keymap"
vscode "ms-toolsai.jupyter-renderers"
vscode "ms-toolsai.vscode-jupyter-cell-tags"
vscode "ms-toolsai.vscode-jupyter-slideshow"
vscode "ms-vscode-remote.remote-containers"
vscode "ms-vscode-remote.remote-ssh"
vscode "ms-vscode-remote.remote-wsl"
vscode "ms-vscode.cmake-tools"
vscode "ms-vscode.cpptools"
vscode "ms-vscode.cpptools-extension-pack"
vscode "ms-vscode.cpptools-themes"
vscode "ms-vscode.remote-explorer"
vscode "oderwat.indent-rainbow"
vscode "onecentlin.laravel-blade"
vscode "onecentlin.laravel5-snippets"
vscode "orsenkucher.vscode-graphql"
vscode "pkief.material-icon-theme"
vscode "pranaygp.vscode-css-peek"
vscode "redhat.java"
vscode "ritwickdey.liveserver"
vscode "seatonjiang.gitmoji-vscode"
vscode "shalldie.background"
vscode "shan.code-settings-sync"
vscode "shinymimikyu.pokemon-color"
vscode "streetsidesoftware.code-spell-checker"
vscode "syler.sass-indented"
vscode "tabnine.tabnine-vscode"
vscode "techer.open-in-browser"
vscode "twxs.cmake"
vscode "vadimcn.vscode-lldb"
vscode "visualstudioexptteam.intellicode-api-usage-examples"
vscode "visualstudioexptteam.vscodeintellicode"
vscode "vscjava.vscode-java-debug"
vscode "vscjava.vscode-java-dependency"
vscode "vscjava.vscode-java-pack"
vscode "vscjava.vscode-lombok"
vscode "vscjava.vscode-maven"
vscode "vscjava.vscode-spring-initializr"
vscode "wakatime.vscode-wakatime"
vscode "walkme.java-extension-pack"
vscode "wallabyjs.quokka-vscode"
vscode "wayou.vscode-todo-highlight"
vscode "xabikos.javascriptsnippets"
vscode "yzhang.markdown-all-in-one"
vscode "zobo.php-intellisense"
```