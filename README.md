# fixed-pages

GourmetSwipe の固定ページを GitHub Pages で配信するためのリポジトリである。

## 概要

スマートフォンアプリ外で公開する静的ページ（プライバシーポリシーなど）を管理する。
当分の間、GitHub Pages を利用し、`privacy.gourmetswipe.com` のカスタムドメインで配信する。

## 配信先

| ページ                         | URL                                  | 言語    |
|--------------------------------|--------------------------------------|---------|
| プライバシーポリシー（日本語） | https://privacy.gourmetswipe.com/    | 日本語  |
| プライバシーポリシー（英語）   | https://privacy.gourmetswipe.com/en/ | English |

## 構成

```
fixed-pages/
├── index.md              # プライバシーポリシー（日本語・トップページ）
├── en/
│   └── index.md          # Privacy Policy（English）
├── CNAME                 # カスタムドメイン設定（privacy.gourmetswipe.com）
├── _config.yml           # Jekyll 設定
└── README.md
```

## セットアップ

### 前提

- GitHub Pages が有効になっている（Settings > Pages > Source: main branch）
- DNS に CNAME レコードが設定されている: `privacy` → `GourmetSwipeDevTeam.github.io`
- HTTPS が有効になっている（Settings > Pages > Enforce HTTPS）

### デプロイ

`main` ブランチにプッシュすると、GitHub Pages が自動でビルド・デプロイする。Jekyll が Markdown を HTML に変換するため、手動変換は不要である。

## 関連

- Issue: [#153 AppStore 外部テスト配布の審査申請](https://github.com/GourmetSwipeDevTeam/gourmet-swipe/issues/153)
