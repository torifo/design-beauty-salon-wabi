# 椿 TSUBAKI — beauty-salon / wabi

**Domain:** `design.beauty-salon-wabi.riumu.net`
**Series:** beauty-salon (4 personas, 美学軸)
**Persona:** wabi — 和モダン・侘び寂び・茶室の延長線にある総合美容空間

---

## 概要

架空の総合美容サロン「椿 TSUBAKI」。ヘッドスパ・髪施術・着付け・ヘアセット の 4 領域を「**整いの儀**」として束ね、Aman Spa の retreat 表現と、星のや・界の季節季語の語り口を、茶室の所作と床の間の余白支配で接続する。

煌びやかなネオン・煽り CTA・派手な配色は使わない。墨と鶸萌黄と生成りで、首筋・髪・手・道具・椿のマクロ写真だけで、「鎮まる」第一印象を構築する。

---

## デザイン要点

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

## 9 セクション構成

1. **ヒーロー** — 縦組み主題「整いの儀」＋椿一輪／障子越しの光
2. **整いの順** — 受付 → 着替え → 頭浴 → 髪 → 結い → 茶 の 6 段
3. **品書き** — 頭浴の儀／髪の儀／纏いの儀／結いの儀（4 部）
4. **閑室** — 椿の間／露地の間／苔の間／月の間（4 室）
5. **道具と材** — 椿油・木櫛・湯桶・墨・和ろうそく・水
6. **結い手** — 結い手／頭浴の手／纏いの手 の 3 名
7. **ひとひら** — 店主の随筆 3 篇（壹・貳・參）
8. **お代** — 通常／会員／早暁・夜半 の 3 段、煽り無し
9. **ご予約** — 「ご予約を承ります」の丁寧な招き

---

## ファイル

| ファイル | 役割 |
|---|---|
| `index.html` | 単一ページ実装 |
| `spec.md` | 仕様書（実装前に作成） |
| `DESIGN_LEARNINGS.md` | 実装で得た知見 |
| `CNAME` | GitHub Pages 用 |
| `.nojekyll` | Jekyll 無効化 |

---

## 参考

- [PLAN_BEAUTY_SALON.md](../PLAN_BEAUTY_SALON.md) — シリーズ全体の方向性
- [spec.md](./spec.md) — 本ペルソナの仕様
- [fitness-gym/totonoi](../../fitness-gym/totonoi/) — 和モダン・縦組み明朝の最近接兄弟
- [vintage-sundries/mingei](../../vintage-sundries/mingei/) — 印章モチーフ・縦組み

---

© Fictitious 椿 TSUBAKI ─ A design study, not a real salon.
