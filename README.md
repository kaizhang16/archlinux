# archlinux

## Editor

```
sudo pacman -S emacs vim
```

## Shell

```
sudo pacman -S fish
chsh -s /usr/bin/fish $USER
```

## Dotfiles

```
sudo chown -R vagrant:vagrant ~/apps
mkdir ~/tmp
cd ~/tmp
curl -LO https://github.com/kaizhang91/dotfiles/releases/download/1.2.0/dotfiles-linux.tar.xz
tar -xvJf dotfiles-linux.tar.xz
./dotfiles templates
```

## Git

```
sudo pacman -S git
```

## Spacemacs

```
git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d
cd ~/.emacs.d
git checkout develop
systemctl --user daemon-reload
systemctl --user enable emacs
systemctl --user start emacs

## 使用时输入 emacsclient -t
```

## Go

```
sudo pacman -S go
go get -u -v github.com/golang/dep/cmd/dep

go get -u -v github.com/nsf/gocode
go get -u -v github.com/rogpeppe/godef
go get -u -v golang.org/x/tools/cmd/guru
go get -u -v golang.org/x/tools/cmd/gorename
go get -u -v golang.org/x/tools/cmd/goimports
go get -u -v github.com/alecthomas/gometalinter
gometalinter --install --update
```

## System

```
sudo pacman -S aspell aspell-en bind-tools fakeroot gdisk graphviz htop lsof make strace
go get -u -v github.com/Jguer/yay
```

## Docker

```
sudo pacman -S docker
sudo usermod -aG docker $USER
sudo systemctl enable docker
sudo systemctl start docker
```

## Haskell

```
sudo pacman -S hasktags hlint hindent hoogle stack stylish-haskell
stack --resolver lts-8.24 install ghc-mod
yay -S haskell-apply-refact
stack install apply-refact
```

## Node.js

```
sudo pacman -S yarn
yarn global add tern
```

## Pandoc

```
sudo pacman -S pandoc pandoc-citeproc pandoc-crossref texlive-most texlive-langchinese
```

## Python

```
sudo pacman -S ipython python python2 python-virtualenv

cd ~ && virtualenv -p python2 mypy2
```

## Rust

```
sudo pacman -S rust
```

## Font

```
sudo pacman -S adobe-source-han-sans-cn-fonts adobe-source-han-serif-cn-fonts wqy-microhei wqy-zenhei
```

## Utility

```
yay -S pet-bin
```
