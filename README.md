# 🦋 047 Awesome Design Mihon-cho — デザイン見本帳

**QQ#047**

> 世界 71 ブランドが語る「言葉にならない思想」

🌐 **Live Demo:** https://design-mihoncho.vercel.app

---

## 概要

世界の主要ブランドのデザインシステム（DESIGN.md）を収集・分析し、  
**カラーパレット・デザイン哲学・ミニUIプレビュー**として見える化したカタログサイト。

お父さんの酒瓶ラベル見本帳、毛糸の色見本帳。  
あのアナログの豊かさをデジタルで再現したいという思いから生まれた。

---

## 機能

- **71ブランドのカードグリッド** — ブランドのプライマリカラーでヒーロー背景を自動生成
- **カテゴリフィルター** — AI / Dev Tools / フィンテック / 自動車 / 音楽 など13カテゴリ
- **テキスト検索** — ブランド名・キーワード・哲学文を横断検索
- **詳細パネル** — カラーパレット・タイポグラフィ・企業概要・ミニUIプレビュー
- **公式サイトリンク** — 各ブランドの公式サイトへ直接アクセス

---

## 技術構成

```
design-mihoncho/
  index.html    — メインUI（バニラHTML/CSS/JS）
  brands.json   — 71ブランドのデザインデータ
```

- フレームワークなし、バニラHTMLのみ
- Vercelでホスティング（Static Deploy、ビルド時間15ms）
- データソース：[awesome-design-md](https://github.com/VoltAgent/awesome-design-md)

---

## データ構造（brands.json）

各ブランドは以下のフィールドを持つ：

```json
{
  "name": "Ferrari",
  "category": "自動車",
  "about": "イタリア高級スポーツカーメーカー",
  "philosophy": "A luxury-automotive brand whose marketing surfaces read as cinematic editorial.",
  "colors": ["#da291c", "#b01e0a", "#9d2211", "#ffffff"],
  "typography": "'FerrariSans' / w500/700/400",
  "keywords": ["情熱", "速度", "イタリアン"],
  "url": "https://www.ferrari.com"
}
```

---

## 位置づけ

本プロジェクトは **Vivillon Code** の第一弾コンテンツ。

```
Vivillon Code（構想中）
  └── デザイン見本帳（本リポジトリ）← 既存ブランドのカタログ
  └── ソムリエ機能（開発予定）← 作りたいものからデザインを推薦
  └── 一般化エンジン（開発予定）← 猫・寿司・小鳥など任意の素材からカタログ生成
```

> *Vivillon Code — 色から入る世界のナレッジ*

---

## 開発メモ

- 2026年5月17日 早朝着想・同日午前中に初版完成
- ClaudeCode（実装）＋ Claude（設計・壁打ち）で開発
- Comomo先生（セナリ学院）のDESIGN.mdレクチャーがきっかけ
