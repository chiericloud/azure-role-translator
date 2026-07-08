# Azure ロール翻訳ツール / Azure Role Translator

Azure の組み込みロール (RBAC) の名前と説明を英語 ⇄ 日本語で検索・参照できる無料の静的ウェブツールです。
Owner、Contributor、Reader などのロールが日本語でどう表示されるかを素早く調べられます。

A free, static web tool for looking up Azure built-in RBAC roles in English and Japanese. Quickly find how roles like Owner, Contributor, and Reader appear in the Japanese Azure Portal.

## 機能 / Features

- **476 の組み込みロール** を収録 — 英語名・日本語名・カテゴリ・説明
- **インクリメンタル検索** — 英語・日本語どちらでも検索可能、一致箇所をハイライト表示
- **カテゴリフィルター** — 特権、コンピューティング、ネットワーク、ストレージ、セキュリティなど 17 カテゴリ
- **列の並べ替え** — 見出しをクリックしてソート
- **公式ドキュメントへの直リンク** — 各ロールから Microsoft Learn の該当ページ (カテゴリ別サブページのアンカー) へ直接ジャンプ
- **参考ドキュメントパネル** — Azure RBAC の概要、コントロール/データ プレーン、カスタムロール、ベストプラクティスなどへのリンク集
- **単一 HTML ファイル** — ビルド不要・依存なし・オフラインでも動作 (Web フォント以外)

<!-- English -->
- **476 built-in roles** with English name, Japanese name, category, and description
- **Instant search** in either language, with match highlighting
- **Category filters** — 17 categories (Privileged, Compute, Networking, Storage, Security, …)
- **Sortable columns** — click a header to sort
- **Deep links to Microsoft Learn** — each role links to its anchor on the official category sub-page
- **Reference docs panel** — curated links to RBAC overview, control/data plane, custom roles, and best practices
- **Single HTML file** — no build step, no dependencies, works offline (except web fonts)

## 使い方 / Usage

ブラウザで [index.html](index.html) を開くだけです。サーバーは不要です。

Just open [index.html](index.html) in a browser — no server required.

静的ホスティング (GitHub Pages、Azure Static Web Apps、Netlify など) にそのまま配置できます。

The file can be deployed as-is to any static host (GitHub Pages, Azure Static Web Apps, Netlify, etc.).

## 翻訳について / About the translations

日本語のロール名・説明は [Microsoft Learn — Azure 組み込みロール (日本語)](https://learn.microsoft.com/ja-jp/azure/role-based-access-control/built-in-roles) に基づいています。

「※ 近似訳」マークのあるロールは、Azure Portal の UI に日本語名が存在しないか確認できないものです。これらの訳は Microsoft Learn ドキュメントまたは命名パターンから導出した近似値であり、実際の Portal 表示と異なる場合があります。

Roles marked "※ 近似訳" (approximate translation) have no confirmed Japanese name in the Azure Portal UI; their translations are derived from Microsoft Learn documentation or naming patterns and may differ from what the Portal actually displays.

## 免責事項 / Disclaimer

- 本サイトは **非公式** の参照ツールであり、Microsoft と提携・関連していません。
- 対象は Azure RBAC の**組み込みロールのみ**です。Microsoft Entra ID ロール (グローバル管理者など)、カスタムロール、クラシック管理者ロールは含まれません。
- ロールの権限・可用性は変更されることがあります。アクセス制御の決定を行う前に、必ず公式ドキュメントを確認してください。

This is an **unofficial** reference tool, not affiliated with Microsoft. It covers **Azure RBAC built-in roles only** (no Microsoft Entra ID roles, custom roles, or classic administrator roles). Role permissions and availability may change — always verify against the official documentation before making access-control decisions.

## ソース / Sources

- [Azure 組み込みロール (日本語)](https://learn.microsoft.com/ja-jp/azure/role-based-access-control/built-in-roles)
- [Azure built-in roles (English)](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles)
