# Netlifyへのデプロイ手順

このドキュメントでは、akanen.jpの静的ミラーサイトをNetlifyにデプロイする手順を説明します。

## 前提条件

- Netlifyアカウント（無料プランで可）
- GitHubアカウント（このリポジトリへのアクセス権）

## デプロイ手順

### 方法1: Netlify UIからデプロイ（推奨）

1. **Netlifyにログイン**
   - https://app.netlify.com/ にアクセス
   - GitHubアカウントでログイン

2. **新しいサイトを作成**
   - "Add new site" → "Import an existing project" をクリック
   - "Deploy with GitHub" を選択

3. **リポジトリを選択**
   - `miyoshi-newmeta/akanen-jp-mirror` を検索して選択

4. **ビルド設定**
   - **Branch to deploy**: `main`
   - **Build command**: 空欄のまま
   - **Publish directory**: `.` (ドット)
   - "Deploy site" をクリック

5. **デプロイ完了**
   - 数分でデプロイが完了します
   - Netlifyが自動生成したURLでサイトにアクセス可能

### 方法2: Netlify CLIからデプロイ

```bash
# Netlify CLIをインストール
npm install -g netlify-cli

# Netlifyにログイン
netlify login

# リポジトリをクローン
git clone https://github.com/miyoshi-newmeta/akanen-jp-mirror.git
cd akanen-jp-mirror

# デプロイ
netlify deploy --prod
```

## カスタムドメインの設定（オプション）

1. Netlifyのサイト設定で "Domain settings" を開く
2. "Add custom domain" をクリック
3. 独自ドメインを入力
4. DNSレコードを設定（Netlifyの指示に従う）

## トラブルシューティング

### 画像が表示されない場合

- `netlify.toml` の設定を確認
- 相対パスが正しく変換されているか確認

### CSSが適用されない場合

- ブラウザのキャッシュをクリア
- Netlifyのデプロイログでエラーを確認

## 注意事項

- このサイトは静的ファイルのミラーです
- 動的機能（フォーム送信、コメントなど）は動作しません
- 元サイトの更新は自動的に反映されません

## サポート

問題が発生した場合は、GitHubのIssuesで報告してください。
