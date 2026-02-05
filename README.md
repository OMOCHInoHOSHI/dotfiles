#
再読み込みのコマンド

これで設定を読み込む

`source ~/.bashrc`


secrets_sh は作成してください（git 管理しません）


## opencode設定

#### ① 既存ファイルの状態確認
- 通常ファイルなら次へ
- 既に symlink なら -> が表示される


``` bash
ls -l ~/.config/opencode/opencode.jsonc
```

#### ② 既存ファイルを退避（安全）

```bash
mv ~/.config/opencode/opencode.jsonc ~/.config/opencode/opencode.jsonc.bak
```

または削除
```bash
rm ~/.config/opencode/opencode.jsonc
```

#### ③ シンボリックリンク作成

```bash
ln -s ~/dotfiles/opencode/opencode.jsonc ~/.config/opencode/opencode.jsonc
```

#### ④ シンボリックリンク確認（最重要）

``` bash
ls -l ~/.config/opencode/opencode.jsonc
```

期待される出力

opencode.jsonc -> /home/ユーザー名/dotfiles/opencode/opencode.jsonc

#### ⑤ 実体ファイルが読めているか確認

```bash
cat ~/.config/opencode/opencode.jsonc
```

