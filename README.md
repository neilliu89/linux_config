# My Mac/Ubuntu dotfiles

参考 mac 开发环境配置：http://sourabhbajaj.com/mac-setup/

# Mac 开发常用软件

- Iterm2
- Alfred
- Dash
- Vscode/Neovim
- Pycharm/Idea/Goland

# Mac 环境快速安装

```
# install Homebrew https://brew.sh/
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# brew tap caskroom/cask 命令提示错误Error: caskroom/cask was moved. Tap homebrew/cask-cask instead. 
cd "$(brew --repo)"/Library/Taps/homebrew/homebrew-cask
git remote set-url origin https://github.com/Homebrew/homebrew-cask

# 关于镜像源指导文档：http://mirrors.ustc.edu.cn/help/index.htmlt

# brew cask install
brew cask install iterm2 \
  alfread \
  docker-toolbox

# brew install
# ignore：忽略几个暂时不需要的文件
  kafka \
  lua \
  ruby \
  nginx \
  zookeeper \
# 不能安装的工具包
  universal-ctags \
brew install aria2 \
  autojump \
  cloc \
  ctags \
  ffmpeg \
  fswatch \
  fzf \
  git \
  go \
  gotags \
  msgpack \
  mysql \
  neovim \
  pyenv \
  pyenv-virtualenv \
  python \
  redis \
  rmtrash \
  sqlite \
  the_silver_searcher \
  thefuck \
  tig \
  tmux \
  tree \
  vim \
  wget \
  youtube-dl \
  zplug \
  zsh-syntax-highlighting

```
安装完提示：
```
==> Summary
🍺  /usr/local/Cellar/zsh-syntax-highlighting/0.7.1: 27 files, 164.4KB
==> Caveats
==> aria2
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
==> ctags
Under some circumstances, emacs and ctags can conflict. By default,
emacs provides an executable `ctags` that would conflict with the
executable of the same name that ctags provides. To prevent this,
Homebrew removes the emacs `ctags` and its manpage before linking.
==> unbound
To have launchd start unbound now and restart at startup:
  sudo brew services start unbound
==> tesseract
This formula contains only the "eng", "osd", and "snum" language data files.
If you need any other supported languages, run `brew install tesseract-lang`.
==> git
The Tcl/Tk GUIs (e.g. gitk, git-gui) are now in the `git-gui` formula.

Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions and functions have been installed to:
  /usr/local/share/zsh/site-functions

Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/git
==> mysql
We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default
只允许本地连接，有必要的话修改配置
To connect run:
    mysql -uroot

To have launchd start mysql now and restart at login:
  brew services start mysql
Or, if you don't want/need a background service you can just run:
  mysql.server start
==> pyenv-virtualenv
To enable auto-activation add to your profile:
  if which pyenv-virtualenv-init > /dev/null; then eval "$(pyenv virtualenv-init -)"; fi
==> python
Python has been installed as
  /usr/local/bin/python3

Unversioned symlinks `python`, `python-config`, `pip` etc. pointing to
`python3`, `python3-config`, `pip3` etc., respectively, have been installed into
  /usr/local/opt/python/libexec/bin

You can install Python packages with
  pip3 install <package>
They will install into the site-package directory
  /usr/local/lib/python3.7/site-packages

See: https://docs.brew.sh/Homebrew-and-Python
==> redis
To have launchd start redis now and restart at login:
  brew services start redis
Or, if you don't want/need a background service you can just run:
  redis-server /usr/local/etc/redis.conf
==> the_silver_searcher
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions have been installed to:
  /usr/local/share/zsh/site-functions
==> thefuck
Add the following to your .bash_profile, .bashrc or .zshrc:

  eval $(thefuck --alias)

For other shells, check https://github.com/nvbn/thefuck/wiki/Shell-aliases
==> tig
A sample of the default configuration has been installed to:
  /usr/local/opt/tig/share/tig/examples/tigrc
to override the system-wide default configuration, copy the sample to:
  /usr/local/etc/tigrc

Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions and functions have been installed to:
  /usr/local/share/zsh/site-functions
==> lua
You may also want luarocks:
  brew install luarocks
==> perl
By default non-brewed cpan modules are installed to the Cellar. If you wish
for your modules to persist across updates we recommend using `local::lib`.

You can set that up like this:
  PERL_MM_OPT="INSTALL_BASE=$HOME/perl5" cpan local::lib
  echo 'eval "$(perl -I$HOME/perl5/lib/perl5 -Mlocal::lib=$HOME/perl5)"' >> /Users/neilliu/.bash_profile
==> ruby
By default, binaries installed by gem will be placed into:
  /usr/local/lib/ruby/gems/2.7.0/bin

You may want to add this to your PATH.

ruby is keg-only, which means it was not symlinked into /usr/local,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

If you need to have ruby first in your PATH run:
  echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> /Users/neilliu/.bash_profile

For compilers to find ruby you may need to set:
  export LDFLAGS="-L/usr/local/opt/ruby/lib"
  export CPPFLAGS="-I/usr/local/opt/ruby/include"

For pkg-config to find ruby you may need to set:
  export PKG_CONFIG_PATH="/usr/local/opt/ruby/lib/pkgconfig"

==> youtube-dl
Bash completion has been installed to:
  /usr/local/etc/bash_completion.d

zsh completions have been installed to:
  /usr/local/share/zsh/site-functions

fish completions have been installed to:
  /usr/local/share/fish/vendor_completions.d
==> zplug
In order to use zplug, please add the following to your .zshrc:
  export ZPLUG_HOME=/usr/local/opt/zplug
  source $ZPLUG_HOME/init.zsh
==> zsh-syntax-highlighting
To activate the syntax highlighting, add the following at the end of your .zshrc:
  source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh

If you receive "highlighters directory not found" error message,
you may need to add the following to your .zshenv:
  export ZSH_HIGHLIGHT_HIGHLIGHTERS_DIR=/usr/local/share/zsh-syntax-highlighting/highlighters
```

```
# install oh-my-zsh  https://github.com/robbyrussell/oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
# now you can copy your own .zshrc file


# install zplug, plugin manager for zsh, https://github.com/zplug/zplug
curl -sL --proto-redir -all,https https://raw.githubusercontent.com/zplug/installer/master/installer.zsh | zsh

# install iterm2 theme: https://draculatheme.com/iterm/
```



# 注意：

- 如果 oh-my-zsh 使用 powerlevel10k 之类的特殊主题，注意需要安装 nerd font 之类的特殊字体显示图标
# github：https://github.com/ohmyzsh/ohmyzsh

- 安装Nerd Font字体
# https://github.com/ryanoasis/nerd-fonts
```
brew tap homebrew/cask-fonts
brew cask install font-hack-nerd-font
```
- 安装powerlevel10k 
# powerlevel10k: https://github.com/romkatv/powerlevel10k
```
brew install romkatv/powerlevel10k/powerlevel10k
echo 'source /usr/local/opt/powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc
```

