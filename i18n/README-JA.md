<!-- markdownlint-disable MD030 -->

<p align="center">
<img src="https://github.com/SynapseFlowAI/SynapseFlow/blob/main/images/SynapseFlow_white.svg#gh-light-mode-only">
<img src="https://github.com/SynapseFlowAI/SynapseFlow/blob/main/images/SynapseFlow_dark.svg#gh-dark-mode-only">
</p>

[![Release Notes](https://img.shields.io/github/release/SynapseFlowAI/SynapseFlow)](https://github.com/SynapseFlowAI/SynapseFlow/releases)
[![Discord](https://img.shields.io/discord/1087698854775881778?label=Discord&logo=discord)](https://discord.gg/jbaHfsRVBW)
[![Twitter Follow](https://img.shields.io/twitter/follow/SynapseFlowAI?style=social)](https://twitter.com/SynapseFlowAI)
[![GitHub star chart](https://img.shields.io/github/stars/SynapseFlowAI/SynapseFlow?style=social)](https://star-history.com/#SynapseFlowAI/SynapseFlow)
[![GitHub fork](https://img.shields.io/github/forks/SynapseFlowAI/SynapseFlow?style=social)](https://github.com/SynapseFlowAI/SynapseFlow/fork)

[English](../README.md) | [繁體中文](./README-TW.md) | [简体中文](./README-ZH.md) | 日本語 | [한국어](./README-KR.md)

<h3>AIエージェントをビジュアルに構築</h3>
<a href="https://github.com/SynapseFlowAI/SynapseFlow">
<img width="100%" src="https://github.com/SynapseFlowAI/SynapseFlow/blob/main/images/SynapseFlow_agentflow.gif?raw=true"></a>

## ⚡ クイックスタート

[NodeJS](https://nodejs.org/en/download) >= 18.15.0 をダウンロードしてインストール

1. SynapseFlow のインストール
    ```bash
    npm install -g SynapseFlow
    ```
2. SynapseFlow の実行

    ```bash
    npx SynapseFlow start
    ```

3. [http://localhost:3000](http://localhost:3000) を開く

## 🐳 Docker

### Docker Compose

1. プロジェクトのルートにある `docker` フォルダに移動する
2. `.env.example` ファイルをコピーして同じ場所に貼り付け、名前を `.env` に変更する
3. `docker compose up -d`
4. [http://localhost:3000](http://localhost:3000) を開く
5. コンテナを停止するには、`docker compose stop` を使用します

### Docker Image

1. ローカルにイメージを構築する:
    ```bash
    docker build --no-cache -t SynapseFlow .
    ```
2. image を実行:

    ```bash
    docker run -d --name SynapseFlow -p 3000:3000 SynapseFlow
    ```

3. image を停止:
    ```bash
    docker stop SynapseFlow
    ```

## 👨‍💻 開発者向け

SynapseFlow には、3 つの異なるモジュールが 1 つの mono リポジトリにあります。

-   `server`: API ロジックを提供する Node バックエンド
-   `ui`: React フロントエンド
-   `components`: サードパーティノードとの統合

### 必須条件

-   [PNPM](https://pnpm.io/installation) をインストール
    ```bash
    npm i -g pnpm
    ```

### セットアップ

1. リポジトリをクローン

    ```bash
    git clone https://github.com/SynapseFlowAI/SynapseFlow.git
    ```

2. リポジトリフォルダに移動

    ```bash
    cd SynapseFlow
    ```

3. すべてのモジュールの依存関係をインストール:

    ```bash
    pnpm install
    ```

4. すべてのコードをビルド:

    ```bash
    pnpm build
    ```

5. アプリを起動:

    ```bash
    pnpm start
    ```

    [http://localhost:3000](http://localhost:3000) でアプリにアクセスできるようになりました

6. 開発用ビルド:

    - `.env` ファイルを作成し、`packages/ui` に `VITE_PORT` を指定する（`.env.example` を参照）
    - `.env` ファイルを作成し、`packages/server` に `PORT` を指定する（`.env.example` を参照）
    - 実行

        ```bash
        pnpm dev
        ```

    コードの変更は [http://localhost:8080](http://localhost:8080) に自動的にアプリをリロードします

## 🌱 環境変数

SynapseFlow は、インスタンスを設定するためのさまざまな環境変数をサポートしています。`packages/server` フォルダ内の `.env` ファイルで以下の変数を指定することができる。[続き](https://github.com/SynapseFlowAI/SynapseFlow/blob/main/CONTRIBUTING.md#-env-variables)を読む

## 📖 ドキュメント

[SynapseFlow ドキュメント](https://docs.SynapseFlowai.com/)

## 🌐 セルフホスト

お客様の既存インフラに SynapseFlow をセルフホストでデプロイ、様々な[デプロイ](https://docs.SynapseFlowai.com/configuration/deployment)をサポートします

-   [AWS](https://docs.SynapseFlowai.com/deployment/aws)
-   [Azure](https://docs.SynapseFlowai.com/deployment/azure)
-   [Digital Ocean](https://docs.SynapseFlowai.com/deployment/digital-ocean)
-   [GCP](https://docs.SynapseFlowai.com/deployment/gcp)
-   <details>
      <summary>その他</summary>

    -   [Railway](https://docs.SynapseFlowai.com/deployment/railway)

        [![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/pn4G8S?referralCode=WVNPD9)

    -   [Render](https://docs.SynapseFlowai.com/deployment/render)

        [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://docs.SynapseFlowai.com/deployment/render)

    -   [Hugging Face Spaces](https://docs.SynapseFlowai.com/deployment/hugging-face)

        <a href="https://huggingface.co/spaces/SynapseFlowAI/SynapseFlow"><img src="https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg" alt="Hugging Face Spaces"></a>

    -   [Elestio](https://elest.io/open-source/SynapseFlowai)

        [![Deploy](https://pub-da36157c854648669813f3f76c526c2b.r2.dev/deploy-on-elestio-black.png)](https://elest.io/open-source/SynapseFlowai)

    -   [Sealos](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DSynapseFlow)

        [![](https://raw.githubusercontent.com/labring-actions/templates/main/Deploy-on-Sealos.svg)](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DSynapseFlow)

    -   [RepoCloud](https://repocloud.io/details/?app_id=29)

        [![Deploy on RepoCloud](https://d16t0pc4846x52.cloudfront.net/deploy.png)](https://repocloud.io/details/?app_id=29)

      </details>

## ☁️ クラウドホスト

[SynapseFlow Cloud の使い方を始める](https://SynapseFlowai.com/)

## 🙋 サポート

ご質問、問題提起、新機能のご要望は、[discussion](https://github.com/SynapseFlowAI/SynapseFlow/discussions)までお気軽にどうぞ

## 🙌 コントリビュート

これらの素晴らしい貢献者に感謝します

<a href="https://github.com/SynapseFlowAI/SynapseFlow/graphs/contributors">
<img src="https://contrib.rocks/image?repo=SynapseFlowAI/SynapseFlow" />
</a>

[コントリビューティングガイド](../CONTRIBUTING.md)を参照してください。質問や問題があれば、[Discord](https://discord.gg/jbaHfsRVBW) までご連絡ください。
[![Star History Chart](https://api.star-history.com/svg?repos=SynapseFlowAI/SynapseFlow&type=Timeline)](https://star-history.com/#SynapseFlowAI/SynapseFlow&Date)

## 📄 ライセンス

このリポジトリのソースコードは、[Apache License Version 2.0](../LICENSE.md)の下で利用可能です。
