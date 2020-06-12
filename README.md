# my-everything-vim

## install tmux  latest (3.1)

```bash
apt-get update
apt-get -y install wget tar libevent-dev libncurses-dev
VERSION=3.1
wget https://github.com/tmux/tmux/releases/download/${VERSION}/tmux-${VERSION}.tar.gz
tar xf tmux-${VERSION}.tar.gz
rm -f tmux-${VERSION}.tar.gz
cd tmux-${VERSION}
./configure
make
make install
cd ..
rm -rf /usr/local/src/tmux-*
mv tmux-${VERSION} /usr/local/src
source ~/.bashrc
tmux -V
export TERM=xterm-256color
```

## install oh my tmux

```bash
cd
git clone https://github.com/gpakosz/.tmux.git
ln -s -f .tmux/.tmux.conf
cp .tmux/.tmux.conf.local .
tmux new -s meta
```

## install Vim 8.2

```bash
add-apt-repository ppa:jonathonf/vim
apt update
apt install vim
```

## install vim-plug
```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs     https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## (optional) install fzf
```bash
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
source ~/.bashrc
```

## prepare to install coc 
### -- Install nodejs >= 10.12:

```bash
curl -sL install-node.now.sh/lts | bash
```

Run `:PlugInstall` and `:CocInstall coc-python`


