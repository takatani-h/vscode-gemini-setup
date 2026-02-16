# Visual Studio Code（VSCode）導入ガイド

## VSCodeとは

Microsoft が提供する無料・オープンソースのコードエディタ。Windows / macOS / Linux に対応している。

## 動作環境

- **Windows:** Windows 10 / 11 以降に対応している。
- **macOS:** macOS 10.15 以降に対応している。
- **Linux:** Ubuntu 20.04 以降など主要ディストリビューションに対応している。

## インストール手順

### 1. ダウンロード

公式サイトからインストーラをダウンロードする。

- 公式サイト: <https://code.visualstudio.com/>

トップページにアクセスすると、使用中の OS に合ったダウンロードボタンが表示される。

### 2. Windows の場合

1. ダウンロードした `VSCodeUserSetup-xxx.exe` を実行する。
2. 使用許諾契約に同意し「次へ」を押す。
3. インストール先フォルダを指定する（デフォルトのままで可）。
4. 追加タスクの選択画面で、以下にチェックを入れておくと便利。
   - 「PATHへの追加」（デフォルトでチェック済み）
   - 「エクスプローラーのコンテキストメニューに追加」
5. 「インストール」をクリックすれば完了する。

### 3. macOS の場合

**方法 A: 手動インストール**

1. ダウンロードした `.zip` ファイルを展開する。
2. `Visual Studio Code.app` を `/Applications` フォルダに移動する。
3. アプリケーションフォルダから起動する。

**方法 B: Homebrew**

```bash
brew install --cask visual-studio-code
```

### 4. Linux（Ubuntu / Debian 系）の場合

```bash
sudo apt update
sudo apt install -y wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/
echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" | sudo tee /etc/apt/sources.list.d/vscode.list
sudo apt update
sudo apt install -y code
```

または Snap を使う場合:

```bash
sudo snap install code --classic
```

## 初期設定

### 日本語化

1. `Ctrl+Shift+X`（macOS: `Cmd+Shift+X`）で拡張機能パネルを開く。
   - 左のアイコン (積まれた四角形) を押してもよい。
2. 検索欄に `Japanese` と入力する。
3. **Japanese Language Pack for VS Code** をインストールする。
4. 「Change Language and Restart」をクリックして再起動する。

### おすすめの基本設定

`Ctrl+,`（macOS: `Cmd+,`）で設定画面を開き、必要に応じて以下を調整する。

| 設定項目             | 説明                                 |
| -------------------- | ------------------------------------ |
| `Editor: Font Size`  | フォントサイズを変更できる。         |
| `Editor: Tab Size`   | タブ幅を変更できる（デフォルト: 4）。|
| `Files: Auto Save`   | ファイルを自動保存できる。           |
| `Editor: Word Wrap`  | 行の折り返しを有効にできる。         |

## 参考リンク

- [VSCode 公式ドキュメント](https://code.visualstudio.com/docs)
- [キカガク - VSCodeのインストール方法を解説](https://www.kikagaku.co.jp/personal/blog/visual-studio-code-windows)
- [WEBST8 - VSCodeのインストール・設定手順](https://webst8.com/code/vscode-install/)
