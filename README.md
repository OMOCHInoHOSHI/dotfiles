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
設定は tmux の起動時に自動で読み込まれます。
起動中に変更を反映する場合（tmux の中で実行）
```
tmux source-file ~/.config/tmux/tmux.conf
```

## opencode設定 (オプション)
opencode を使うデバイスでは、リポジトリをクローンしてセットアップしてください。

```bash
git clone git@github.com:OMOCHInoHOSHI/dotfiles-opencode.git ~/dotfiles-opencode
```

詳細は `dotfiles-opencode/README.md` を参照してください。
