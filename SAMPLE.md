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

`~/.config/tmux/tmux.conf`（wsl・mac 共通）
```
# 環境依存（必要になったら）
# source-file ~/dotfiles/wsl_tmux

# 共通設定
source-file ~/dotfiles/common_tmux
```
