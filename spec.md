# 椿 TSUBAKI — beauty-salon/wabi Spec

**Status:** Draft
**Author:** torifo
**Created:** 2026-05-25
**Updated:** 2026-05-25

---

## 1. Overview

### Problem Statement
日本の高級美容サロンは「華やか・煌びやか・最先端」を競うあまり、和の素養に近い顧客が本来求めている「鎮まる時間」「儀式としての美の所作」が表現の俎上に乗らない。茶室の所作・水音・湯気・墨の匂いを延長線として美容空間を捉え、頭髪・頭皮・着付け・髪結いを一連の「整いの儀」として提示するサイトの例が、特に Web 上では極めて乏しい。煌びやかなネオン・煽り CTA・派手な配色は、和の客の所作と相容れない。

### Goal
架空の総合美容サロン「椿 TSUBAKI」を、**茶室の延長線にある美容空間**として実装する。ヘッドスパ・髪施術・着付け・ヘアセットの 4 領域を「整いの儀」として束ね、Aman Spa の retreat 表現と、星のや・界の季節季語の語り口、日本古来の茶室・床の間の余白支配を接続する。墨・鶸萌黄・生成り・銀朱を主とし、縦組み明朝の主見出し、障子・水滴・銘木・椿・和ろうそくの素材写真で「鎮まる」第一印象を構築する。

### Non-Goals
- 煽り CTA（「今すぐ予約」「期間限定 30%OFF」など即時性訴求）
- 派手な配色（蛍光ピンク・ネオンゴールド・原色）と過剰な金属光沢の装飾
- ビフォーアフター写真によるダイエット・小顔・若返り訴求
- 顔写真の使用（顔は写さず、後ろ姿・首筋・髪・手・道具のみ）
- カート・オンライン決済・物販 EC
- 価格表のキャンペーン枠・ポップアップバナー・カウントダウン
- 自動再生動画・カルーセル・視差スクロール

---

## 2. User Stories

| ID | Persona | Want to | So that |
|----|---------|---------|---------|
| US-01 | 40代経営者の女性（茶道嗜む） | ヘッドスパと髪結いを「一つの儀」として通しで受けたい | 慌ただしさを断ち切る午後を持てる |
| US-02 | 30代結婚式列席の女性 | 着付け＋ヘアセットを式当日朝にお願いしたい | 移動や着替えの負担なく式に臨める |
| US-03 | 50代常客（隠れ家好み） | 個室・予約少数・静かな時間帯を選びたい | 人と顔を合わせず籠れる |
| US-04 | 20代日本舞踊の稽古生 | 黒髪を丁寧に梳く頭皮ケアを継続したい | 髷を結いやすい状態を保てる |

### Acceptance Criteria

**US-01:**
- WHEN ページを開いた THEN 縦組みの主題「整いの儀」が大型明朝で現れる
- WHEN 「品書き」セクションに到達した THEN ヘッドスパ → 髪 → 着付け → ヘアセットが「一連の儀」として図示されている

**US-02:**
- WHEN 「儀の段」で着付け＋ヘアセットの所要時間・持ち物・当日の流れが読める
- WHEN ご予約セクションに到達した THEN 「当日朝のお仕度」の特別枠があると分かる

**US-03:**
- WHEN 「閑室」（個室）案内に到達した THEN 部屋数・障子・畳・水屋の説明と写真がある
- WHEN 営業時間を見た THEN 早朝・深夜枠が「静かな時間」として用意されている

**US-04:**
- WHEN ヘッドスパの品書きを見た THEN 椿油・木櫛・湯通し・乾燥儀の手順が記載されている

---

## 3. Functional Requirements

| ID | Requirement | Priority | Notes |
|----|-------------|----------|-------|
| FR-01 | ヒーローは縦組み明朝の主題「整いの儀」＋障子越しの光／水滴／椿一輪の静止画 | P0 | writing-mode: vertical-rl、主見出しは画面右上 |
| FR-02 | 季語バッジ（現在の二十四節気・七十二候を上部に小さく表示） | P0 | 例：「立夏 蛙始鳴」。月替わりではなく候替わり |
| FR-03 | 品書き（メニュー）4 部：頭浴の儀／髪の儀／纏いの儀（着付け）／結いの儀（ヘアセット） | P0 | 各 3–5 項目、所要時間・お代を縦書き混じり |
| FR-04 | 「整いの順」を 受付 → 着替え → 頭浴 → 髪 → 結い → 茶 の 6 段で図示 | P0 | 罫線一本と中点で連結、横スクロールなし |
| FR-05 | 茶室／個室（閑室）案内、4 室の名前と季の写真（椿の間／露地の間／苔の間／月の間） | P0 | 障子・畳・銘木の素材マクロ |
| FR-06 | 道具と材の章：椿油・木櫛・湯桶・墨・和ろうそく・水のマクロ写真と一言解説 | P1 | 顔は出さず、手と道具のみ |
| FR-07 | 結い手（スタッフ）3 名の後ろ姿／手元と短い随筆 | P1 | 肩書きは「結い手」「頭浴の手」「纏いの手」 |
| FR-08 | 店主の随筆「ひとひら」を 3–4 本（縦書き章番号 壹／貳／參／肆） | P1 | 商業文ではなく随筆的トーン |
| FR-09 | お代（料金）は通常／会員／早暁・夜半 の 3 段、煽りや割引バナー無し | P0 | 表は中央寄せ、罫線一本 |
| FR-10 | ご予約・お問合せ（直接 CTA「予約はこちら」は使わず「ご予約を承ります」） | P0 | 電話・お問合せフォーム文言は丁寧体 |
| FR-11 | 和ろうそくの灯りを模した極控えめなフッターアクセント（点滅でなく fade のみ） | P1 | prefers-reduced-motion で停止 |
| FR-12 | 840px 以下で縦組み主見出しは横組みに畳む。品書きは 1 カラム化 | P0 | mobile では vertical-rl を解除 |

---

## 4. Key Design Decisions

| Decision | Chosen | Rationale | Rejected |
|----------|--------|-----------|----------|
| 美学方向 | 茶室の延長線にある美容空間 | wabi-sabi を「装飾の無さ」ではなく「儀式の所作」として翻訳 | 旅館サイト的な観光寄り表現 |
| 主見出し書体 | Shippori Mincho B1（縦組み） | 細い縦画と余白で「鎮まり」を担保 | 太いゴシック（力みすぎる） |
| 副見出し書体 | Yuji Syuku | やや個性ある明朝で「手書きの気配」を残す | 標準的明朝のみ（個性が弱い） |
| 本文書体 | Noto Sans JP Light（数字とラテンは Inter Light） | 細字で静寂を担保、可読性は確保 | Bold 多用 |
| 主見出し書字方向 | writing-mode: vertical-rl | 茶室の床の間・掛軸の語彙を採用 | 全横組み（和の所作が消える） |
| 配色 | 墨 #1a1614 × 鶸萌黄 #7a8c5e × 生成り #ebe2d2 × 銀朱 #a85e4a × 利休鼠 #888573 | 抹茶碗・茶室・椿の世界観を 5 色に絞る | 純黒・蛍光・原色 |
| 黒の温度 | 純黒ではなく墨色 #1a1614 | 印刷物の墨に近い温度感 | #000000（冷たすぎる） |
| アクセント | 銀朱（一輪の椿のような最小限の差し色） | 茶花としての椿の象徴を残す | 金箔ゴールド全面（成金的） |
| 写真トーン | 低彩度・自然光・障子越しの柔光 | 茶室の光線量に合わせる | スタジオ照明の高彩度 |
| 写真被写体 | 後ろ姿・首筋・髪・手・道具・椿・水・障子・和ろうそく | 顔を出さず気配で語る | 笑顔のモデル正面写真 |
| 季の表現 | 二十四節気・七十二候バッジを常時上部に | 季節と一体化させた星のや的語り口 | 季節無視の通年同一 |
| CTA トーン | 「ご予約を承ります」「お問合せ」「ご案内」 | 茶室への招きの言葉 | 「今すぐ申し込む」「無料体験！」 |
| アニメ | 1.0–1.4 秒の fadeup と障子の光のような slow fade | 「ととのう」までの間 | スライド・カルーセル・視差 |
| 装飾 | 罫線一本・中点・章番号（壹・貳・參・肆）・店主印（朱の四角） | 民藝・茶道の押印文化 | グラデ・シャドウ・派手ボタン |
| ナビ | 上部に縦組みロゴ＋横に細罫で区切ったメニュー | 余白の支配を崩さない | メガメニュー・固定ヘッダ |

---

## 5. Design System

### Color Palette

```css
:root {
  /* 墨・鶸萌黄・生成り・銀朱・利休鼠 */
  --sumi:       #1a1614;   /* 墨（主テキスト・主見出し） */
  --sumi-asa:   #2b2521;   /* 浅墨（副テキスト） */
  --hiwa:       #7a8c5e;   /* 鶸萌黄（アクセント・罫線） */
  --hiwa-fukai: #5a6b48;   /* 深鶸（hover） */
  --kinari:     #ebe2d2;   /* 生成り（基盤背景） */
  --washi:      #f1ebde;   /* 和紙（セクション背景・浮上） */
  --shu:        #a85e4a;   /* 銀朱（椿の一輪・店主印） */
  --rikyu:      #888573;   /* 利休鼠（補助・キャプション） */
  --yuge:       #ffffff;   /* 湯気（最薄ハイライト） */
}
```

### Typography

```css
:root {
  /* 書体 */
  --font-mei:    'Shippori Mincho B1', 'Hiragino Mincho ProN', 'Yu Mincho', serif;
  --font-shuku: 'Yuji Syuku', 'Shippori Mincho B1', serif;
  --font-honbun:'Noto Sans JP', 'Inter', system-ui, sans-serif;
  --font-latin: 'Inter', 'Helvetica Neue', sans-serif;

  /* 字組み */
  --leading-body:    2.0;       /* 行間広め（茶室の呼吸） */
  --leading-mincho:  1.8;
  --tracking-mei:    0.12em;    /* 明朝の縦画を活かす */
  --tracking-shuku:  0.08em;
}

h1, h2 {
  font-family: var(--font-mei);
  font-weight: 300;
  letter-spacing: var(--tracking-mei);
}

.hero-tate {
  writing-mode: vertical-rl;
  font-family: var(--font-mei);
  font-weight: 300;
  letter-spacing: var(--tracking-mei);
}
```

### Rhythm & Lines

```css
:root {
  --space-xl: clamp(5rem, 9vw, 9rem);
  --space-lg: clamp(3rem, 6vw, 6rem);
  --space-md: 1.75rem;
  --space-sm: 1rem;
  --rule:     1px solid var(--rikyu);
  --rule-shu: 1px solid var(--shu);
}
```

### Motion

```css
/* 障子越しの光のような fade */
@keyframes shoji-fade {
  from { opacity: 0; transform: translateY(16px); }
  to   { opacity: 1; transform: none; }
}
.reveal { animation: shoji-fade 1.2s cubic-bezier(.2,.7,.2,1) both; }

@media (prefers-reduced-motion: reduce) {
  .reveal { animation: none; }
}
```

### Texture

```css
/* 和紙ノイズ（控えめに重ねる） */
body::before {
  content: "";
  position: fixed; inset: 0;
  background:
    url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg'><filter id='n'><feTurbulence baseFrequency='0.85'/></filter><rect width='100%' height='100%' filter='url(%23n)' opacity='0.6'/></svg>");
  mix-blend-mode: multiply;
  opacity: 0.18;
  pointer-events: none;
}
```

### Components

- **店主印**: `border:1px solid var(--shu); border-radius:2px; transform: rotate(-6deg);` の朱の四角に「椿」一文字
- **章番号**: 壹／貳／參／肆 を縦書きで章タイトル左に配置、`var(--rikyu)` 色
- **季語バッジ**: 上部ナビ右端、`var(--shu)` の細罫一本＋小さな明朝で「立夏 蛙始鳴」表示
- **罫線**: 太さ 1px、長さは画面幅の 40–60% 程度、中央寄せまたは左寄せ
- **CTA**: ボタン背景無し、罫線一本のみ。hover で hairline が右へ伸びる演出

---

## 6. References

### 参照サイト
- [Aman Spa](https://www.aman.com/spa) — retreat の静寂、余白支配、自然素材の写真扱い、CTA の押し付けない動詞
- [星のや・界](https://www.hoshinoresorts.com/jp/hotels/kai/) — 季節季語と感情価値の接続、明朝主体の階層設計
- [SaunaLab](https://saunalab.jp/) — 日本のリトリート系ロゴと配色のトーン参考

### Fonts
- [Shippori Mincho B1](https://fonts.google.com/specimen/Shippori+Mincho+B1) — 主見出し（縦組み対応）
- [Yuji Syuku](https://fonts.google.com/specimen/Yuji+Syuku) — 副見出し（個性ある明朝）
- [Noto Sans JP](https://fonts.google.com/noto/specimen/Noto+Sans+JP) — 本文
- [Inter](https://fonts.google.com/specimen/Inter) — ラテン併記

### 写真モチーフ（Unsplash 想定）
- 障子越しの柔光、銘木の床、苔、椿一輪、和ろうそく、墨と硯、水滴、湯気、木櫛、椿油の瓶
- 後ろ姿の首筋、髪を梳く手元、結いの手の所作

### 同シリーズ参照
- [beauty-salon 親 README](../README.md)（実装フェーズで作成）
- [fitness-gym/totonoi spec](../../fitness-gym/totonoi/spec.md) — 和モダン・余白・縦組み明朝の系譜（最も近い兄弟ペルソナ）
- [seasidebookshop/fuyunagi spec](../../seasidebookshop/fuyunagi/spec.md) — 和の静の表現
- [vintage-sundries/mingei spec](../../vintage-sundries/mingei/spec.md) — 縦組み・余白・明朝・印章モチーフ

### 上位計画
- [PLAN_BEAUTY_SALON.md](../../PLAN_BEAUTY_SALON.md) — シリーズ全体の方向性と 4 ペルソナの位置付け
