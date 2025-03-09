# Code-github-termux 
Installing v4.97.2 of the arm64 release from GitHub.

+ mkdir -p ~/.cache/code-server
+ curl -#fL -o ~/.cache/code-server/code-server-4.97.2-linux-arm64.tar.gz.incomplete -C - https://github.com/coder/code-server/releases/download/v4.97.2/code-server-4.97.2-linux-arm64.tar.gz
+ mv ~/.cache/code-server/code-server-4.97.2-linux-arm64.tar.gz.incomplete ~/.cache/code-server/code-server-4.97.2-linux-arm64.tar.gz
+ mkdir -p ~/.local
+ sudo mkdir -p ~/.local/lib ~/.local/bin
+ sudo tar -C ~/.local/lib -xzf ~/.cache/code-server/code-server-4.97.2-linux-arm64.tar.gz
+ sudo mv -f ~/.local/lib/code-server-4.97.2-linux-arm64 ~/.local/lib/code-server-4.97.2
+ sudo ln -fs ~/.local/lib/code-server-4.97.2/bin/code-server ~/.local/bin/code-server

Standalone release has been installed into ~/.local/lib/code-server-4.97.2

Extend your path to use code-server:
  PATH="$HOME/.local/bin:$PATH"
Then run with:
  code-server
  
