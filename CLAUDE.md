# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 重要な注意事項
日本語で出力する際は必ずUTF-8エンコーディングを使用してください。

## プロジェクト概要

このリポジトリは**Dottoの2025年中間発表用のSlidevプレゼンテーション**です。SlidevはmarkdownとVue.jsコンポーネントを使用するWebベースのプレゼンテーションフレームワークです。

## 開発コマンド

### 基本的な開発コマンド
- `pnpm install` - 依存関係をインストール
- `pnpm dev` - 開発サーバーを起動（自動的にhttp://localhost:3030が開きます）
- `pnpm build` - プロダクション用にプレゼンテーションをビルド
- `pnpm export` - スライドをPDFやその他の形式でエクスポート

### パッケージマネージャー
このプロジェクトではnpmやyarnではなく**pnpm**を使用しています。

## アーキテクチャ

### メインエントリーポイント
- `slides.md` - テーマ設定とタイトルページ参照を含むメインスライド設定
- `pages/title.md` - タイトルスライドの内容
- `docs/` - プレゼンテーション内容のセクションを含むmarkdownファイル：
  - `draft.md` - 日本語でのメインプレゼンテーション概要
  - 個別のトピックファイル（ci_cd.md、design_system.mdなど）

### コンポーネント
- `components/Counter.vue` - Composition APIを使用したVueコンポーネントの例
- ユーティリティファーストスタイリングにUnoCSSを使用
- コンポーネントはスライド内でインポート・使用可能

### コードスニペット
- `snippets/external.ts` - スライド内で参照可能なTypeScriptコードスニペット
- プレゼンテーション内でのコードハイライト用に`#region snippet`コメントを使用

### デプロイ設定
- `netlify.toml` - Netlifyデプロイ設定
- `vercel.json` - Vercelデプロイ設定
- 両方ともindex.htmlへのフォールバックを持つSPA配信用に設定済み

## Slidev固有の機能

### テーマとスタイリング
- 日本語フォント（Hiragino Kaku Gothic ProN）を使用した`theme: default`
- 拡張markdown構文用のMDC（Markdown Components）をサポート
- トランジション無し設定（`transition: none`）

### コンテンツ構成
- スライドは`pages/`と`docs/`内の個別markdownファイルで整理
- メインプレゼンテーション概要は日本語（Dottoプロジェクト発表）
- インタラクティブ要素用にスライド内でVueコンポーネントを使用

## ファイル構造について
- `node_modules/`と`pnpm-lock.yaml`はpnpmパッケージ管理を示す
- プレゼンテーション素材用の`docs/images/`ディレクトリ
- NetlifyとVercel両方の設定でデプロイ準備完了