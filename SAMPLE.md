# bashrc, zshrcの例

```wsl版
# Ubuntuのデフォルト設定処理（非対話モード時のリターンなど）

case $- in
    *i*) ;;
      *) return;;
esac

# 環境依存
. ~/dotfiles/wsl_sh

# dotfilesの読み込み
. ~/dotfiles/common_sh
. ~/dotfiles-opencode/common_sh
```


```zshrc版
. ~/dotfiles/common_sh
. ~/dotfiles/mac_sh

# OpenCode用は条件付きのまま
. ~/dotfiles/common_sh
```


## opencodeがある場合
```
. ~/dotfiles-opencode/common_sh
```
