# bashrc, zshrcの例

```wsl版
# Ubuntuのデフォルト設定処理（非対話モード時のリターンなど）

case $- in
    *i*) ;;
      *) return;;
esac

# 環境依存
. ~/dotfiles/wsl_sh

# 共通設定
. ~/dotfiles/common_sh
. ~/dotfiles-opencode/common_sh
```


```Windows（Git Bash）版 ~/.bashrc
case $- in
    *i*) ;;
      *) return;;
esac

# 環境依存
. ~/dotfiles/win_sh

# 共通設定
. ~/dotfiles/common_sh
. ~/dotfiles-opencode/common_sh
```

Git Bash は `-l`（ログインシェル）で起動すると `~/.bash_profile` しか読まないため、
`~/.bash_profile` も作って `.bashrc` を読み込む。
```Windows（Git Bash）版 ~/.bash_profile
[ -f ~/.bashrc ] && . ~/.bashrc
```


```zshrc版
# 環境依存
. ~/dotfiles/mac_sh

# 共通設定
. ~/dotfiles/common_sh
```


## opencodeがある場合
```
. ~/dotfiles-opencode/common_sh
```

# tmux.confの例

※ Windows（Git Bash）には tmux が無いので不要。画面分割は Windows Terminal のペインで代用する。

`~/.config/tmux/tmux.conf`（wsl・mac 共通）
```
# 環境依存（必要になったら）
# source-file ~/dotfiles/wsl_tmux

# 共通設定
source-file ~/dotfiles/common_tmux
```
