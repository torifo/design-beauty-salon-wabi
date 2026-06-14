---
name: design-beauty-salon-wabi
description: "beauty salon landing-page design study — 'wabi' theme/persona (pure HTML/CSS/JS, no build). Use when designing a 'wabi'-style beauty salon site aesthetic. beauty salonの「wabi」テーマLPのデザイン参照スキル。"
---

# design-beauty-salon-wabi

A landing-page **design study** for a fictional **wabi**-theme beauty salon (pure HTML + CSS + vanilla JS, no build, GitHub-Pages ready). Use this as a **style / design-system reference** when building a similar aesthetic.

架空の「wabi」テーマのbeauty salon LP デザイン研究。同種の世界観を作るときの**スタイル／デザインシステム参照**として使う。

## When to use / 使いどころ
- **EN:** designing a 'wabi'-style beauty salon site — match its palette, typography and layout discipline.
- **JP:** 「wabi」系のbeauty salonサイトを設計するとき。配色・タイポ・レイアウト規律を流用。

## Bundled assets / 同梱アセット
This skill folder is the reference implementation — start from these files:
- `index.html` — full page markup
- `style.css` — design tokens (CSS custom properties) + layout
- `script.js` — vanilla JS (if present)
- `README.md` — full bilingual doc, brand context and series links

## Design reference / デザイン参照
_Lifted from the repo README — see README.md for the complete, bilingual version._

### 概要
架空の総合美容サロン「椿 TSUBAKI」。ヘッドスパ・髪施術・着付け・ヘアセット の 4 領域を「**整いの儀**」として束ね、Aman Spa の retreat 表現と、星のや・界の季節季語の語り口を、茶室の所作と床の間の余白支配で接続する。

煌びやかなネオン・煽り CTA・派手な配色は使わない。墨と鶸萌黄と生成りで、首筋・髪・手・道具・椿のマクロ写真だけで、「鎮まる」第一印象を構築する。

---

### デザイン要点
| 項目 | 採用 |
|---|---|
| 配色 | 墨 `#1a1614` × 鶸萌黄 `#7a8c5e` × 生成り `#ebe2d2` × 銀朱 `#a85e4a` × 利休鼠 `#888573` |
| 主見出し書体 | Shippori Mincho B1（縦組み・writing-mode: vertical-rl） |
| 副見出し書体 | Yuji Syuku（手書きの気配を残す明朝） |
| 本文書体 | Noto Sans JP 400 以上、ラテン数字は Inter |
| 章番号 | 壹／貳／參／肆／伍／陸／漆／捌／玖（縦組み・利休鼠） |
| 季語バッジ | 二十四節気・七十二候を上部ナビ右端に常時表示（例：立夏 蛙始鳴） |
| 店主印 | 朱の四角に「椿」一文字、`transform: rotate(-6deg)` |
| アニメ | 障子越しの光のような 1.2s fadeup のみ、視差スクロール禁止 |
| 写真 | 顔禁。後ろ姿・首筋・髪・手・道具・椿・障子・水・和ろうそく |
| アクセシビリティ | `prefers-reduced-motion` 対応、focus-visible に鶸萌黄の枠線 |

---

## How to apply / 適用方法
1. Reuse `style.css` custom properties (color / type / spacing tokens) as the design-system base.
2. Copy `index.html` layout as the starting structure, then swap brand name and content.
3. Keep the palette, font pairing and layout discipline described above.

---
> The brand is fictional (design study) — replace all brand/content. Full context: see **`README.md`**.
