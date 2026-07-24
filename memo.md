md2docx利用メモ
===

## はじめに

-  [md2docx](https://github.com/nokonoko1203/md2docx/tree/main) を利用した時のメモをまとめています。
- 詳しくは、上記サイトの`README`を参照ください。

## Rustのインストール

### Macの場合(Homebrewを利用する場合)

```zsh
brew update
brew install rust
```

## md2docxのインストール

```bash
# gitでファイルを取得する
git clone https://github.com/nokonoko1203/md2docx.git

# コマンドとしてインストール
cargo install --path .

# PATHを通す
export PATH="$HOME/.cargo/bin:$PATH"

# ビルドだけ
cargo build --release
```

### Macの場合のインストール作業の追加

`.zshrc`に、下記の文言を追加する。

```zsh
export PATH="$HOME/.cargo/bin:$PATH"
```

## 使い方

```bash
# 基本的な変換（document.docxが生成される）
mdd document.md

# 出力先を指定
mdd document.md -o output.docx

# 設定ファイルを指定
mdd document.md -o output.docx -c mdd.toml

# 全項目とデフォルト値の確認
mdd --help
```

## マークダウン要素（個人的に忘れやすいもの厳選）

要素 | 書き方
|--|--|
改ページ | `\pagebreak`
水平線 | `---`
画像 | `![alt](path)`
太字 | `**text**`
斜体 | `*text*`
