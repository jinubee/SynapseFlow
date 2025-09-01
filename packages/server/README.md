<!-- markdownlint-disable MD030 -->

# SynapseFlow

English | [中文](./README-ZH.md)

<h3>Build AI Agents, Visually</h3>

![SynapseFlow](https://github.com/SynapseFlowAI/SynapseFlow/blob/main/images/SynapseFlow_agentflow.gif?raw=true)

## ⚡Quick Start

1. Install SynapseFlow
    ```bash
    npm install -g SynapseFlow
    ```
2. Start SynapseFlow

    ```bash
    npx SynapseFlow start
    ```

3. Open [http://localhost:3000](http://localhost:3000)

## 🌱 Env Variables

SynapseFlow support different environment variables to configure your instance. You can specify the following variables in the `.env` file inside `packages/server` folder. Read [more](https://github.com/SynapseFlowAI/SynapseFlow/blob/main/CONTRIBUTING.md#-env-variables)

You can also specify the env variables when using `npx`. For example:

```
npx SynapseFlow start --PORT=3000 --DEBUG=true
```

## 📖 Tests

We use [Cypress](https://github.com/cypress-io) for our e2e testing. If you want to run the test suite in dev mode please follow this guide:

```sh
cd SynapseFlow/packages/server
pnpm install
./node_modules/.bin/cypress install
pnpm build
#Only for writting new tests on local dev -> pnpm run cypress:open
pnpm run e2e
```

## 📖 Documentation

[SynapseFlow Docs](https://docs.SynapseFlowai.com/)

## 🌐 Self Host

-   [AWS](https://docs.SynapseFlowai.com/deployment/aws)
-   [Azure](https://docs.SynapseFlowai.com/deployment/azure)
-   [Digital Ocean](https://docs.SynapseFlowai.com/deployment/digital-ocean)
-   [GCP](https://docs.SynapseFlowai.com/deployment/gcp)
-   <details>
      <summary>Others</summary>

    -   [Railway](https://docs.SynapseFlowai.com/deployment/railway)

        [![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/pn4G8S?referralCode=WVNPD9)

    -   [Render](https://docs.SynapseFlowai.com/deployment/render)

        [![Deploy to Render](https://render.com/images/deploy-to-render-button.svg)](https://docs.SynapseFlowai.com/deployment/render)

    -   [HuggingFace Spaces](https://docs.SynapseFlowai.com/deployment/hugging-face)

        <a href="https://huggingface.co/spaces/SynapseFlowAI/SynapseFlow"><img src="https://huggingface.co/datasets/huggingface/badges/raw/main/open-in-hf-spaces-sm.svg" alt="HuggingFace Spaces"></a>

    -   [Elestio](https://elest.io/open-source/SynapseFlowai)

        [![Deploy on Elestio](https://elest.io/images/logos/deploy-to-elestio-btn.png)](https://elest.io/open-source/SynapseFlowai)

    -   [Sealos](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DSynapseFlow)

        [![](https://raw.githubusercontent.com/labring-actions/templates/main/Deploy-on-Sealos.svg)](https://cloud.sealos.io/?openapp=system-template%3FtemplateName%3DSynapseFlow)

    -   [RepoCloud](https://repocloud.io/details/?app_id=29)

        [![Deploy on RepoCloud](https://d16t0pc4846x52.cloudfront.net/deploy.png)](https://repocloud.io/details/?app_id=29)

      </details>

## ☁️ SynapseFlow Cloud

[Get Started with SynapseFlow Cloud](https://SynapseFlowai.com/)

## 🙋 Support

Feel free to ask any questions, raise problems, and request new features in [discussion](https://github.com/SynapseFlowAI/SynapseFlow/discussions)

## 🙌 Contributing

See [contributing guide](https://github.com/SynapseFlowAI/SynapseFlow/blob/master/CONTRIBUTING.md). Reach out to us at [Discord](https://discord.gg/jbaHfsRVBW) if you have any questions or issues.

## 📄 License

Source code in this repository is made available under the [Apache License Version 2.0](https://github.com/SynapseFlowAI/SynapseFlow/blob/master/LICENSE.md).
