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
