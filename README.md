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
ls -l ~/.config/opencode/opencode.json
```

#### ② 既存ファイルを退避（安全）

```bash
mv ~/.config/opencode/opencode.json ~/.config/opencode/opencode.json.bak
```

または削除
```bash
rm ~/.config/opencode/opencode.json
```

#### ③ シンボリックリンク作成

```bash
ln -s ~/dotfiles/opencode/opencode.json ~/.config/opencode/opencode.json
```

#### ④ シンボリックリンク確認（最重要）

``` bash
ls -l ~/.config/opencode/opencode.json
```

期待される出力

opencode.json -> /home/ユーザー名/dotfiles/opencode/opencode.json

#### ⑤ 実体ファイルが読めているか確認

```bash
cat ~/.config/opencode/opencode.json
```

