# dotfiles

## bashrc、zshrcの例
[SMAPLE.mdを参照](SAMPLE.md)

## tmux設定
`~/.config/tmux/tmux.conf` は手動で作成してください（Git管理対象外）。
内容は [SAMPLE.mdを参照](SAMPLE.md)

## bashrc、zshrcを更新したら
再読み込みのコマンド

```
source ~/.bashrc
```
```
source ~/.zshrc
```

## tmuxを更新したら
```
tmux source-file ~/.config/tmux/tmux.conf
```

## opencode設定 (オプション)
opencode を使うデバイスでは、リポジトリをクローンしてセットアップしてください。

```bash
git clone git@github.com:OMOCHInoHOSHI/dotfiles-opencode.git ~/dotfiles-opencode
```

詳細は `dotfiles-opencode/README.md` を参照してください。
