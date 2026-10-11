# 七面鳥モラトリアム PHOTO GALLERY

七面鳥モラトリアム公式WEB写真館。

## 現在の公開範囲

このリポジトリには PUBLIC（一般公開）用サイトのみを配置します。

**MEMBER（メンバー限定）および GOODS（購入者限定）の元画像は、このPublicリポジトリへ絶対に保存しません。**

限定領域は後工程で、認証付きの非公開ストレージとして実装します。

## 公演データ

- 2026.08.13 横浜BAYSIS

## セキュリティ方針

Public GitHub repository / public deployment に配置してよいのは一般公開が確定した写真だけです。写真選別GUIの MEMBER / GOODS 出力先をこのリポジトリへ同期しないでください。

## SNS共有カード（写真館全体）

`index.html` の静的OGP / Twitter Cardは、写真館全体の紹介に使用します。
画像は `assets/ogp.jpg`（1200×630、JPEG）。GitHub Pagesのプロジェクトパスを
含むHTTPS絶対URLを指定しています。JavaScriptの実行は不要です。

使用写真は既存の一般公開リスト
`public/2026-08-13-yokohama-baysis/photos.json` に登録された
`photo_014.jpg` のみ。写真館名・公演日・会場・撮影者 `@yocamerayo` を画像内に記載。
MEMBER / GOODS画像、外部の限定ストレージは使用していません。
画像を差し替える際も、一般公開が確定した写真だけを使用してください。

### 検証範囲（2026-10-11）

- HTMLのメタタグ重複なし、OGPとTwitter Cardの画像URL一致、canonical / og:url一致。
- JPEGの寸法・デコード・目視確認、ローカルHTTPでHTML・共有画像・公演JSON・25枚を取得。
- 既存25枚の写真、JSON、撮影者クレジット、JS、CSSは変更なし。
- 本番GitHub Pagesへの追加画像の配信確認は、PRマージとデプロイ完了後に実施する必要があります。
- LINE / X / Facebook / Instagramでの実際のカード表示とキャッシュ更新は未検証です。
  サービスごとの画像切り抜きや共有画面の違いを含め、表示を保証するものではありません。

### マージ後の確認

1. 本番トップページのHTMLにOGPがあり、`assets/ogp.jpg` がHTTP 200 / image/jpegで取得できることを確認。
2. LINEへのリンク貼り付け、Xでのリンク共有プレビュー、FacebookのSharing Debuggerで確認。
3. Instagramは利用する共有画面（DM等）で実機確認。通常投稿・ストーリーズも同じ表示になるとは想定しない。
4. 古いカードが残る場合は各サービスの再取得機能を使用。画像更新時はファイル名と両メタタグを同時更新。
