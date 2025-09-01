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

[English](../README.md) | 繁體中文 | [简体中文](./README-ZH.md) | [日本語](./README-JA.md) | [한국어](./README-KR.md)

<h3>可視化建置 AI/LLM 流程</h3>
<a href="https://github.com/SynapseFlowAI/SynapseFlow">
<img width="100%" src="https://github.com/SynapseFlowAI/SynapseFlow/blob/main/images/SynapseFlow_agentflow.gif?raw=true"></a>

## ⚡ 快速開始

下載並安裝 [NodeJS](https://nodejs.org/en/download) >= 18.15.0

1. 安裝 SynapseFlow
    ```bash
    npm install -g SynapseFlow
    ```
2. 啟動 SynapseFlow

    ```bash
    npx SynapseFlow start
    ```

3. 打開 [http://localhost:3000](http://localhost:3000)

## 🐳 Docker

### Docker Compose

1. 複製 SynapseFlow 專案
2. 進入專案根目錄的 `docker` 資料夾
3. 複製 `.env.example` 文件，貼到相同位置，並重新命名為 `.env` 文件
4. `docker compose up -d`
5. 打開 [http://localhost:3000](http://localhost:3000)
6. 您可以透過 `docker compose stop` 停止容器

### Docker 映像

1. 本地建置映像：
    ```bash
    docker build --no-cache -t SynapseFlow .
    ```
2. 運行映像：

    ```bash
    docker run -d --name SynapseFlow -p 3000:3000 SynapseFlow
    ```

3. 停止映像：
    ```bash
    docker stop SynapseFlow
    ```

## 👨‍💻 開發者

SynapseFlow 在單個 mono 儲存庫中有 3 個不同的模組。

-   `server`: 提供 API 邏輯的 Node 後端
-   `ui`: React 前端
-   `components`: 第三方節點集成
-   `api-documentation`: 從 express 自動生成的 swagger-ui API 文檔

### 先決條件

-   安裝 [PNPM](https://pnpm.io/installation)
    ```bash
    npm i -g pnpm
    ```

### 設置

1.  複製儲存庫

    ```bash
    git clone https://github.com/SynapseFlowAI/SynapseFlow.git
    ```

2.  進入儲存庫文件夾

    ```bash
    cd SynapseFlow
    ```

3.  安裝所有模組的所有依賴項：

    ```bash
    pnpm install
    ```

4.  建置所有程式碼：

    ```bash
    pnpm build
    ```

    <details>
    <summary>Exit code 134（JavaScript heap out of memory）</summary>  
      如果在運行上述 `build` 腳本時遇到此錯誤，請嘗試增加 Node.js 中的 Heap 記憶體大小並重新運行腳本：

        export NODE_OPTIONS="--max-old-space-size=4096"
        pnpm build

    </details>

5.  啟動應用：

    ```bash
    pnpm start
    ```

    您現在可以開啟 [http://localhost:3000](http://localhost:3000)

6.  對於開發建置：

    -   在 `packages/ui` 中創建 `.env` 文件並指定 `VITE_PORT`（參考 `.env.example`）
    -   在 `packages/server` 中創建 `.env` 文件並指定 `PORT`（參考 `.env.example`）
    -   運行

        ```bash
        pnpm dev
        ```

    任何程式碼更改都會自動重新加載應用程式 [http://localhost:8080](http://localhost:8080)

## 🌱 環境變數

SynapseFlow 支持不同的環境變數來配置您的實例。您可以在 `packages/server` 文件夾中的 `.env` 文件中指定以下變數。閱讀 [更多](https://github.com/SynapseFlowAI/SynapseFlow/blob/main/CONTRIBUTING.md#-env-variables)

## 📖 文檔

[SynapseFlow 文檔](https://docs.SynapseFlowai.com/)

## 🌐 自行架設

在您現有的基礎設施中部署 SynapseFlow，我們支持各種自行架設選項 [部署](https://docs.SynapseFlowai.com/configuration/deployment)

-   [AWS](https://docs.SynapseFlowai.com/configuration/deployment/aws)
-   [Azure](https://docs.SynapseFlowai.com/configuration/deployment/azure)
-   [Digital Ocean](https://docs.SynapseFlowai.com/configuration/deployment/digital-ocean)
-   [GCP](https://docs.SynapseFlowai.com/configuration/deployment/gcp)
-   [阿里雲](https://computenest.console.aliyun.com/service/instance/create/default?type=user&ServiceName=SynapseFlow社区版)
-   <details>
      <summary>其他</summary>

    -   [Railway](https://docs.SynapseFlowai.com/configuration/deployment/railway)

        [![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/pn4G8S?referralCode=WVNPD9)

    -   [Render](https://docs.SynapseFlowai.com/configuration/deployment/render)

        [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://docs.SynapseFlowai.com/configuration/deployment/render)

    -   [HuggingFace Spaces](https://docs.SynapseFlowai.com/deployment/hugging-face)

        <a href="https://huggingface.co/spaces/SynapseFlowAI/SynapseFlow"><img src="https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg" alt="HuggingFace Spaces"></a>

    -   [Elestio](https://elest.io/open-source/SynapseFlowai)

        [![Deploy on Elestio](https://elest.io/images/logos/deploy-to-elestio-btn.png)](https://elest.io/open-source/SynapseFlowai)

    -   [Sealos](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DSynapseFlow)

        [![](https://raw.githubusercontent.com/labring-actions/templates/main/Deploy-on-Sealos.svg)](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DSynapseFlow)

    -   [RepoCloud](https://repocloud.io/details/?app_id=29)

        [![Deploy on RepoCloud](https://d16t0pc4846x52.cloudfront.net/deploy.png)](https://repocloud.io/details/?app_id=29)

      </details>

## ☁️ SynapseFlow 雲端平台

[開始使用 SynapseFlow 雲端平台](https://SynapseFlowai.com/)

## 🙋 支持

隨時在 [討論](https://github.com/SynapseFlowAI/SynapseFlow/discussions) 中提出任何問題、提出問題和請求新功能

## 🙌 貢獻

感謝這些出色的貢獻者

<a href="https://github.com/SynapseFlowAI/SynapseFlow/graphs/contributors">
<img src="https://contrib.rocks/image?repo=SynapseFlowAI/SynapseFlow" />
</a>

請參閱 [貢獻指南](../CONTRIBUTING.md)。如果您有任何問題或問題，請透過 [Discord](https://discord.gg/jbaHfsRVBW) 與我們聯繫。
[![Star History Chart](https://api.star-history.com/svg?repos=SynapseFlowAI/SynapseFlow&type=Timeline)](https://star-history.com/#SynapseFlowAI/SynapseFlow&Date)

## 📄 許可證

此儲存庫中的原始碼根據 [Apache 2.0 授權條款](../LICENSE.md) 授權使用。
