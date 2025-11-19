# AKANEN Website - Static Mirror

このリポジトリは、akanen.jpのウェブサイトの静的ミラーです。

## 概要

- **元サイト**: http://akanen.jp
- **取得日**: 2025年11月20日
- **目的**: Netlifyでホスティング可能な静的ファイル群として保存

## デプロイ方法

### Netlifyへのデプロイ

1. Netlifyにログイン
2. "New site from Git"を選択
3. このGitHubリポジトリを接続
4. デプロイ設定:
   - Build command: (空欄)
   - Publish directory: `.`
5. "Deploy site"をクリック

## ファイル構成

- `index.html` - トップページ
- `wp-content/` - WordPressのコンテンツ（CSS、画像など）
- `wp-includes/` - WordPressのライブラリファイル
- `contact/` - コンタクトページ
- `works-2/` - 作品ページ
- `netlify.toml` - Netlify設定ファイル
- `_redirects` - リダイレクト設定

## 注意事項

このサイトは静的ファイルとして保存されているため、動的機能（フォーム送信、コメントなど）は動作しません。
