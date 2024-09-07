sudo apt-get install -y apt-transport-https 

sudo sh -c 'curl -1sLf "https://dl.modular.com/bBNWiLZX5igwHXeu/installer/gpg.0E4925737A3895AD.key" | gpg --dearmor > /usr/share/keyrings/modular-installer-archive-keyring.gpg'

sudo sh -c 'curl -1sLf "https://dl.modular.com/bBNWiLZX5igwHXeu/installer/config.deb.txt?distro=debian&codename=wheezy" > /etc/apt/sources.list.d/modular-installer.list'

apt-get update
apt-get install -y modular

modular auth mut_ca58f664a340488893cc3e7a68308397 &&  modular install mojo

## run

```

  🔥 Mojo installed! 🔥

Mojo's Python virtual environment created at /home/vlad/.modular/pkg/packages.modular.com_mojo/venv

If you are using ZSH (default on macOS), run the following commands:

echo 'export MODULAR_HOME="/home/vlad/.modular"' >> ~/.zshrc
echo 'export PATH="/home/vlad/.modular/pkg/packages.modular.com_mojo/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc

If you are using bash, run the following commands:

BASHRC=$( [ -f "$HOME/.bash_profile" ] && echo "$HOME/.bash_profile" || echo "$HOME/.bashrc" )
echo 'export MODULAR_HOME="/home/vlad/.modular"' >> "$BASHRC"
echo 'export PATH="/home/vlad/.modular/pkg/packages.modular.com_mojo/bin:$PATH"' >> "$BASHRC"
source "$BASHRC"

Then enter 'mojo' to start the Mojo REPL.

For tool help, enter 'mojo --help'.
For more docs, see https://docs.modular.com/mojo.

```


* vs code extension: https://marketplace.visualstudio.com/items?itemName=modular-mojotools.vscode-mojo