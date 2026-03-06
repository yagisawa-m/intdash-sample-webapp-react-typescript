# intdash-sample-webapp-react-typescript
チュートリアルA: ReactとTypescriptを使用したフロントエンドアプリケーション
https://docs.intdash.jp/manual/docs/2025R1L/ja/api-sdk/tutorials/browser-script-app.html

# 必要な開発環境
```sh
$ node -v
v24.14.0

$ npm -v
11.9.0

$ java --version
openjdk 21.0.10 2026-01-20
OpenJDK Runtime Environment (build 21.0.10+7-Ubuntu-124.04)
OpenJDK 64-Bit Server VM (build 21.0.10+7-Ubuntu-124.04, mixed mode, sharing)

$ docker compose version
Docker Compose version v2.40.3
```

# プロジェクトディレクトリを作成
```sh
$ npm create vite@latest
Need to install the following packages:
create-vite@8.3.0
Ok to proceed? (y)

> npx
> "create-vite"

│
◇  Project name:
│  custom-app
│
◇  Select a framework:
│  React
│
◇  Select a variant:
│  TypeScript + SWC
│
◇  Use Vite 8 beta (Experimental)?:
│  No
│
◇  Install with npm and start now?
│  Yes
│
◇  Scaffolding project in /mnt/c/repositories/GitHub.com/yagisawa-m/intdash-sample-webapp-react-typescript/custom-app...
│
◇  Installing dependencies with npm...

added 173 packages, and audited 174 packages in 47s

47 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
│
◇  Starting dev server...

> custom-app@0.0.0 dev
> vite


  VITE v7.3.1  ready in 1092 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
```

```sh
cd custom-app
```

# REST API用ライブラリーの生成
```sh
npm install @openapitools/openapi-generator-cli
VERSION=v2.6.0
./node_modules/.bin/openapi-generator-cli generate \
-g typescript-axios -i https://docs.intdash.jp/api/intdash-api/${VERSION}/openapi_public.yaml \
-o ./src/intdash \
--additional-properties=useSingleRequestParameter=true
```
