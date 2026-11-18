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

## Windows（Git Bash）で使う場合

WSL ではなく Windows ネイティブで使うときの前提（初回のみ）。

1. **改行コード**: clone する前に `git config --global core.autocrlf input` を実行する。
   このリポジトリは `.gitattributes` で LF に固定しているが、他のリポジトリでも CRLF 混入を防げる。
2. **開発者モード**: 「設定 → システム → 開発者向け → 開発者モード」をオン。
   `win_sh` の `MSYS=winsymlinks:nativestrict` と組み合わせて、`ln -s` が本物のシンボリックリンクになる
   （オフのままだと `ln -s` はエラーになる。コピーにはならない）。
3. **シェル**: Windows Terminal のプロファイルで `"C:\Program Files\Git\bin\bash.exe" -i -l` を起動する。
   `~/.bashrc` と `~/.bash_profile` の例は [SAMPLE.md](SAMPLE.md) を参照。
4. **tmux**: Git Bash には無い。分割は Windows Terminal のペイン／タブで代用する。
   `win_sh` が OSC 9;9 でカレントディレクトリを通知するので、「タブの複製」(Ctrl+Shift+D) で同じ場所が開く。

## opencode設定 (オプション)
opencode を使うデバイスでは、リポジトリをクローンしてセットアップしてください。

```bash
git clone git@github.com:OMOCHInoHOSHI/dotfiles-opencode.git ~/dotfiles-opencode
```

詳細は `dotfiles-opencode/README.md` を参照してください。
