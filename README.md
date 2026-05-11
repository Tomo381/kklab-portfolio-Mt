# Portfolio Site

A lightweight, dependency-free static portfolio site. Built with just `index.html`, `style.css`, and `script.js` — ready to deploy on GitHub Pages.

[日本語版はこちら](#概要)

---

## Overview

This is a personal portfolio template featuring:

- **Dark / Light theme toggle** with persistent preference
- **Japanese / English language switch** with persistent preference
- **Smooth scroll animations** using IntersectionObserver
- **Responsive design** for mobile and desktop
- **Accessible** — skip links, ARIA labels, focus states, reduced-motion support
- **Zero build steps** — just open in a browser or deploy to GitHub Pages

## Demo

Open `index.html` directly in a browser, or serve locally:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy to GitHub Pages

1. Create a repository on GitHub  
   (name it `<username>.github.io` for root domain deployment)

2. Push the files:

```bash
git init
git add index.html style.css script.js README.md
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

3. Enable GitHub Pages:  
   Settings → Pages → Source: Deploy from a branch → Branch: `main` / `(root)`

## Customization

Replace the `{{...}}` placeholders in `index.html` with your own information.

| Placeholder | Description |
|-------------|-------------|
| `{{NAME_JP}}` | Name (Japanese) |
| `{{NAME_EN}}` | Name (English) |
| `{{INITIALS}}` | Initials for logo/favicon (e.g., `KK`) |
| `{{HEADLINE_JP}}` | Tagline (Japanese) |
| `{{HEADLINE_EN}}` | Tagline (English) |
| `{{BIO_JP}}` | Bio (Japanese) |
| `{{BIO_EN}}` | Bio (English) |
| `{{PHOTO_URL}}` | Profile photo URL |
| `{{GITHUB_USERNAME}}` | GitHub username |
| `{{EMAIL}}` | Email address |
| `{{X_HANDLE}}` | X (Twitter) handle (without `@`) |

### Add Skills

Duplicate `<li class="badge ...">` elements in the `#skills` section.

- Languages → `badge-accent`
- Tools & Frameworks → `badge-accent2`
- Other → `badge-accent3`

### Add Projects

Duplicate `<article class="project-card">` in the `#projects` section.

### Add Experience

Duplicate `<li class="timeline-item">` in the `#experience` section.

### Change Accent Colors

Edit CSS custom properties in `style.css`:

```css
:root {
  --accent:   #6366f1; /* primary */
  --accent-2: #ec4899; /* secondary */
  --accent-3: #06b6d4; /* tertiary */
}
```

## File Structure

```
.
├── index.html   # Markup & content
├── style.css    # Styles, themes & animations
├── script.js    # Theme toggle, language switch, scroll animations
└── README.md    # This file
```

## License

MIT

---

## 概要

ビルドツール・外部依存ゼロの静的ポートフォリオサイトです。`index.html` / `style.css` / `script.js` の 3 ファイルで完結しており、GitHub Pages にそのまま公開できます。

## 機能

- **ダーク / ライト テーマ切り替え**（設定を保存）
- **日本語 / 英語 言語切り替え**（設定を保存）
- **スクロールアニメーション**（IntersectionObserver 使用）
- **レスポンシブデザイン**
- **アクセシビリティ対応**（スキップリンク、ARIA、フォーカス状態、リデュースモーション対応）

## GitHub Pages へのデプロイ手順

1. GitHub で新しいリポジトリを作成  
   （`https://<ユーザー名>.github.io/` として公開する場合は、リポジトリ名を **`<ユーザー名>.github.io`** にしてください）

2. ファイルをプッシュ：

```bash
git init
git add index.html style.css script.js README.md
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<ユーザー名>/<リポジトリ名>.git
git push -u origin main
```

3. GitHub Pages を有効化：  
   Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `(root)`

数分後、サイトが公開されます。

## プロフィールの編集方法

`index.html` 内の `{{...}}` プレースホルダを自分の情報に書き換えてください。

| プレースホルダ | 内容 |
|---|---|
| `{{NAME_JP}}` | 氏名（日本語） |
| `{{NAME_EN}}` | 氏名（英語） |
| `{{INITIALS}}` | イニシャル（例: `KK`）|
| `{{HEADLINE_JP}}` | キャッチコピー（日本語） |
| `{{HEADLINE_EN}}` | キャッチコピー（英語） |
| `{{BIO_JP}}` | 自己紹介（日本語） |
| `{{BIO_EN}}` | 自己紹介（英語） |
| `{{PHOTO_URL}}` | プロフィール写真の URL |
| `{{GITHUB_USERNAME}}` | GitHub ユーザー名 |
| `{{EMAIL}}` | メールアドレス |
| `{{X_HANDLE}}` | X (Twitter) ハンドル（`@` なし） |

### スキルの追加

`#skills` セクション内の `<li class="badge ...">` を複製して追加します。カテゴリに応じてクラスを使い分けてください。

- 言語系 → `badge-accent`
- ツール・フレームワーク系 → `badge-accent2`
- その他 → `badge-accent3`

### プロジェクトの追加

`#projects` セクション内の `<article class="project-card">` を複製して追加します。`{{REPO_URL}}` と `{{LIVE_URL}}` を実際の URL に書き換えてください。

### 経歴の追加

`#experience` セクション内の `<li class="timeline-item">` を複製して追加します。

### アクセントカラーの変更

`style.css` の `:root` と `[data-theme="light"]` 内の `--accent` / `--accent-2` / `--accent-3` を変更してください。

## ライセンス

MIT
