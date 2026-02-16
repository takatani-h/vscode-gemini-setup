# Gemini CLI 導入ガイド

## Gemini CLI とは

Google が提供するオープンソースの AI エージェントツール。ターミナル上で Gemini モデルを直接利用できる。

- GitHub: <https://github.com/google-gemini/gemini-cli>
- 公式ドキュメント: <https://geminicli.com/docs/get-started/>

## 動作環境

| 項目         | 要件                                          |
| ------------ | --------------------------------------------- |
| OS           | macOS 15+ / Windows 11 24H2+ / Ubuntu 20.04+  |
| ランタイム   | Node.js 20.0.0 以上                           |
| メモリ       | 4GB 以上（推奨 16GB 以上）                    |
| シェル       | Bash または Zsh                               |
| ネットワーク | インターネット接続が必要である                |

## インストール手順

### 1. Node.js のインストール（未導入の場合）

公式サイトから LTS 版をインストールする: [公式サイト](https://nodejs.org/)

インストール後、バージョンを確認する:

```bash
node -v   # v20.0.0 以上であること
npm -v
```

### 2. Gemini CLI のインストール

**方法 A: npm（推奨）**

```bash
npm install -g @google/gemini-cli
```

**方法 B: Homebrew（macOS / Linux）**

```bash
brew install gemini-cli
```

**方法 C: インストールなしで実行（npx）**

```bash
npx @google/gemini-cli
```

### 3. 認証（初回のみ）

インストール後、初回起動時に Google アカウントでの認証が求められる。

```bash
gemini
```

ブラウザが開くので、Google アカウントでログインして認証を完了する。

個人の Google アカウントで認証すると、以下の無料枠が利用できる:

- 1 分あたり **60 リクエスト**まで利用できる。
- 1 日あたり **1,000 リクエスト**まで利用できる。

## リリースチャンネル

用途に応じてチャンネルを選択できる。

```bash
# 安定版（デフォルト・推奨）
npm install -g @google/gemini-cli@latest

# プレビュー版（週次リリース）
npm install -g @google/gemini-cli@preview

# ナイトリー版（日次ビルド）
npm install -g @google/gemini-cli@nightly
```

## 基本的な使い方

```bash
# 対話モードで起動
gemini

# プロンプトを指定して実行
gemini -p "このプロジェクトの構成を説明して"
```

## サンドボックスモード（Docker）

安全な環境で実行したい場合に使う:

```bash
gemini --sandbox -y -p "your prompt here"
```

## 補足

- Google Cloud Shell や Cloud Workstations にはプリインストールされている。
- Anaconda 環境でも利用できる（`conda` で Node.js 環境を作成後に `npm install`）。

## 参考リンク

- [Gemini CLI 公式ドキュメント - インストール](https://geminicli.com/docs/get-started/installation/)
- [GitHub - google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)
- [Google Codelabs - Hands-on with Gemini CLI](https://codelabs.developers.google.com/gemini-cli-hands-on)
- [DataCamp - Gemini CLI ガイド](https://www.datacamp.com/tutorial/gemini-cli)
