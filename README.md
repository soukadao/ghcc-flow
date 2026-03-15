# ghcc-flow

## セットアップ

### 前提条件

- Node.js（LTS推奨）
- pnpm

### 初期セットアップ

```bash
pnpm install
```

依存関係をインストールします。

## Biome の実行方法

このプロジェクトでは Biome を使ってコード整形・チェックを実行できます。

```bash
pnpm biome:fix
```

上記コマンドは `biome check --write` を実行し、問題の自動修正を試みます。

## 利用可能なスクリプト

- `pnpm biome:fix`: `biome check --write` を実行します。
