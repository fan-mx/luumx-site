# LUUMX Static Site Starter

このフォルダは **GitHub Pages** で公開できる最小構成の静的サイトです。

## 公開手順（最短）
1. GitHubで新しいリポジトリを作成（例: `website`）。
2. このフォルダ内のファイルをそのままコミット＆プッシュ。
3. GitHubのリポジトリ → **Settings** → **Pages** で
   - **Build and deployment**: 「Deploy from a branch」を選択
   - Branch: `main` / Folder: `/ (root)` を選び **Save**
4. 数十秒後、表示されたURLでサイトが公開されます。

## 独自ドメイン（例: www.luumx.jp）
- ルートにある `CNAME` ファイルの中身を、使いたいドメイン名に変更してください（例: `www.luumx.jp`）。
- ドメイン側DNSに **CNAME レコード** を作成：
  - ホスト名: `www`
  - 値: `<your-github-username>.github.io`
- GitHub Pages の **Enforce HTTPS** にチェック。

> ルートドメイン（`luumx.jp`）を使う場合は、DNSに ALIAS/ANAME（または CNAME フラッテン）を設定できるDNSを推奨します。対応していない場合は、`luumx.jp → https://www.luumx.jp` の 301 リダイレクトを設定してください。

## 高度な使い方
- `404.html` は GitHub Pages 用のカスタム404です。
- ビルドが必要なフレームワーク（Astro/Next/Nuxt等）は GitHub Actions を使うと自動デプロイできます。
