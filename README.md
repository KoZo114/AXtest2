# 10FRESH 練馬店｜ブログ & Instagram 半自動更新ワークフロー

毎朝 09:40 に ChatGPT で **ブログ原稿＋Instagram キャプション＋カルーセル台本（5 枚）** を生成し、  
以下 4 ステップで公開しています。

---

## 🌱 デイリーフロー

| 時刻 | 手順 | 担当 | ツール |
|------|------|------|--------|
| 09:40 | ChatGPT へ固定プロンプト送信 → 原稿生成 | Bot | ChatGPT |
| 09:45 | ① Instagram キャプションをコピペ → 語尾や表現を微修正 | 人 | Notion / テキストエディタ |
| 09:50 | ② カルーセル台本 (5 枚) を Canva でデザイン → 動画 (mp4) に書き出し | 人 | Canva |
| 09:55 | ③ 画像 / 動画 + ①のキャプションを Instagram へ投稿 | 人 | Meta Business Suite |
| 10:00 | ④ ブログ構成を軽く修正して　Hot Pepper Beauty のブログ機能へ投稿 | 人 | Hot Pepper 管理画面 |

> **ポイント**：文章とデザイン案は自動生成。公開フェーズは 15 分の人手で完了。

---

## 🖥️ 動作環境

| 項目 | 値 |
|------|----|
| ChatGPT モデル | GPT-4o |
| デザイン | Canva (Web / App) |
| 投稿 | Meta Business Suite（Instagram） |
| ブログ | Hot Pepper Beauty 店舗管理画面 |

---

## 🚀 試してみる（ローカル手動生成）

```bash
# 1. プロンプトをコピーして ChatGPT に貼り付け
#    → 生成された Markdown を ./draft/ に保存
mkdir -p draft && code draft/2025-08-01.md

# 2. Instagram 用キャプションを微修正し ig.txt へ保存
# 3. Canva でカルーセル (5 枚) → mp4 出力
# 4. Meta Business Suite で ig.txt + mp4/画像 を予約投稿
# 5. blog.md を Hot Pepper Beauty ブログへコピペ
---

## 📎 補足資料とデモ

- [📄 調査レポート（report.md）](https://github.com/KoZo114/AXtest2/blob/main/report.md)  
　→ このツールの開発背景・業務改善ポイントをまとめたレポートです。

- [🌐 自動出力デモ（index.html）](https://kozo114.github.io/AXtest2/)  
　→ ブラウザで開けるサンプル出力（HTML形式）です。


