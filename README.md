# Azure ロール翻訳ツール / Azure Role Translator

Azure の組み込みロール（RBAC）の英語名・日本語名・説明を検索できる無料の Web ツールです。
「Owner って日本語のポータルだと何て表示される？」「所有者の英語名は？」といった疑問をすぐに解決できます。

A free web tool for looking up Azure built-in RBAC roles in both English and Japanese — role names, translations, descriptions, and links to the official docs.

**🌐 サイト / Live site:** https://brave-ocean-0bdad5900.azurestaticapps.net

## 機能 / Features

- **476 の組み込みロール** を 17 カテゴリ（特権、コンピューティング、ネットワーク、ストレージ、セキュリティなど）に整理して収録
- **日英どちらでも検索可能** — 英語名・日本語名・説明・カテゴリを対象にインクリメンタル検索（ハイライト表示付き）
- **カテゴリフィルターと列ソート** で目的のロールに素早くアクセス
- **各ロールから Microsoft Learn 公式ドキュメントへ直接リンク**（該当ロールのアンカー付き）
- **近似訳マーク（※ 近似訳）** — Azure Portal の UI に公式な日本語名が確認できないロールには明示的にマークを付与
- **Azure RBAC の参考ドキュメント集** — RBAC の概要、コントロールプレーン／データプレーン、カスタムロール、ベストプラクティスなどへのリンクをページ上部に掲載
- **レスポンシブ対応** — モバイルでは列を自動的に省略して表示

<!-- English summary -->
- 476 built-in roles organized into 17 categories (Privileged, Compute, Networking, Storage, Security, …)
- Instant search across English names, Japanese names, descriptions, and categories, with match highlighting
- Category filters and sortable columns
- Direct deep links to each role's section in the official Microsoft Learn documentation
- Roles without a confirmed Japanese name in the Azure Portal UI are flagged as approximate translations (※ 近似訳)
- Fully responsive layout

## 使い方 / Usage

サイトを開いて検索ボックスにロール名（英語・日本語どちらでも可）を入力するだけです。カテゴリボタンで絞り込み、列ヘッダーのクリックでソートできます。

Just open the site and type a role name (English or Japanese) into the search box. Use the category buttons to filter and click column headers to sort.

### ローカルで実行 / Run locally

ビルド不要の単一 HTML ファイルです。`index.html` をブラウザーで開くだけで動作します。

This is a single self-contained HTML file with no build step — simply open `index.html` in a browser.

```bash
git clone https://github.com/chiericloud/azure-role-translator.git
cd azure-role-translator
# ブラウザーで index.html を開く / open index.html in your browser
```

## 構成 / Project structure

| ファイル / File | 説明 / Description |
|---|---|
| `index.html` | アプリ本体（HTML / CSS / JavaScript / ロールデータをすべて含む） / The entire app: markup, styles, logic, and role data |
| `.github/workflows/azure-static-web-apps-*.yml` | Azure Static Web Apps への CI/CD（`main` への push で自動デプロイ） / CI/CD to Azure Static Web Apps (auto-deploys on push to `main`) |

ロールデータは `index.html` 内の `RAW` 配列（`[英語名, 日本語名, カテゴリ, 説明, ドキュメントアンカー]`）で管理しています。近似訳のロールは `APPROX` セットに列挙されています。

Role data lives in the `RAW` array inside `index.html` (`[englishName, japaneseName, category, description, docsAnchor]`). Roles with approximate translations are listed in the `APPROX` set.

## データソース / Data sources

- [Microsoft Learn — Azure 組み込みロール（日本語）](https://learn.microsoft.com/ja-jp/azure/role-based-access-control/built-in-roles)
- [Microsoft Learn — Azure built-in roles (English)](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)

## 免責事項 / Disclaimer

- 本サイトは **非公式** の参照ツールであり、Microsoft とは提携・関連していません。
- 対象は Azure RBAC の **組み込みロールのみ** です。Microsoft Entra ID ロール（グローバル管理者など）、カスタムロール、クラシック管理者ロールは含まれません。
- ロールの権限・可用性は変更される場合があります。アクセス制御の決定を行う前に、必ず公式ドキュメントを確認してください。
- 「※ 近似訳」マークのある日本語名は、Microsoft Learn ドキュメントまたは命名パターンから導出した近似値であり、実際の Azure Portal の表示と異なる場合があります。

This is an **unofficial** reference tool, not affiliated with Microsoft. It covers Azure RBAC **built-in roles only** (no Microsoft Entra ID roles, custom roles, or classic administrator roles). Role permissions and availability may change — always verify against the official documentation before making access-control decisions. Japanese names marked ※ 近似訳 are approximations derived from Microsoft Learn docs or naming patterns and may differ from the actual Azure Portal UI.

## サポート / Support

このツールが役に立ったら、コーヒーをおごっていただけると嬉しいです ☕
If you find this tool useful, consider buying me a coffee ☕

**https://buymeacoffee.com/lacerise**
