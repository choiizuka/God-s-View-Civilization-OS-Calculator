# 神の視点 — Civilization OS Calculator

**God's View: Civilization OS Calculator**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue)](https://choiizuka.github.io/God-s-View-Civilization-OS-Calculator/)

> 6つの変数を操作すると、文明の絶滅リスクと残存時間がリアルタイムで変わる。
> これは予言ではない。不完全な文明OSが引き起こすスタックオーバーフローの計算結果だ。

---

## 概要 / Overview

AI軍事利用・フェイク情報・戦争強度・愛と平和の因子など6つの入力パラメータをスライダーで操作すると、文明の絶滅リスク・エントロピー・残存時間などの出力値がリアルタイムで更新される。

書籍・GitHubレポート・2026年宣言の思想を「動くコード」として実装したもの。

---

## デモ / Live Demo

**https://choiizuka.github.io/God-s-View-Civilization-OS-Calculator/**

---

## 入力パラメータ / Input Parameters

| パラメータ | 説明 | 影響方向 |
|---|---|---|
| AI軍事利用率 (AI Military Use) | AIが軍事・兵器に利用される度合い | エントロピー増加 |
| フェイク情報率 (Fake Information Rate) | SNS・メディア上の偽情報の割合 | エントロピー増加 |
| 真実密度 (Truth Density) | 検証可能な真実の情報の割合 | エントロピー抑制 |
| 戦争強度 (War Intensity) | 世界規模での戦争・紛争の激しさ | エントロピー増加 |
| 人間の責任度 (Human Responsibility) | 人間が自らの判断と行動に責任を持つ度合い | ネゲントロピー増加 |
| 愛と平和の因子 (Love / Peace Factor) | 社会における協調・共感・平和的解決の度合い | ネゲントロピー増加 |

---

## 出力パラメータ / Output Parameters

| パラメータ | 説明 |
|---|---|
| 絶滅リスク (Extinction Risk) | 文明崩壊・人類絶滅の確率指標 (0–100%) |
| システムエントロピー (System Entropy) | 文明の無秩序・崩壊圧力の度合い (0–100%) |
| 文明安定度 (Civilization Stability) | 現在の文明が安定稼働している度合い (0–100%) |
| 回復可能性 (Recovery Probability) | 崩壊から回復できる可能性 (0–100%) |
| 情報汚染度 (Info Pollution) | 情報空間の汚染・信頼崩壊の度合い (0–100%) |
| 推計残存時間 (Time Remaining) | 現在の変数が続いた場合の文明の推計残存時間 |

---

## 最終判定 / Final Verdict

| 判定 | 条件 | 意味 |
|---|---|---|
| **STABLE** | 文明安定度 ≥ 55% | ネゲントロピーがエントロピーを上回っている |
| **UNSTABLE** | 上記以外 | 崩壊と安定の境界線上にある |
| **CRITICAL** | 絶滅リスク ≥ 50% | 深刻な危機状態。即時の介入が必要 |
| **COLLAPSE** | 絶滅リスク ≥ 75% | 臨界超過。システム全損が不可避に近い |

---

## 計算ロジック / Calculation Logic

厳密な学術モデルではなく、直感的に正しい挙動をするシンプルな因果モデル。

```
エントロピー = (AI軍事利用×0.30 + フェイク情報×0.35 + 戦争強度×0.25 - 真実密度×0.10) × 0.9

ネゲントロピー = (愛と平和×0.40 + 人間責任×0.35 + 真実密度×0.25) × 0.8

文明安定度 = clamp(ネゲントロピー - エントロピー×0.6 + 30, 0, 100)

絶滅リスク = clamp(エントロピー×0.70 - ネゲントロピー×0.50 + 20, 0, 100)

回復可能性 = clamp(ネゲントロピー×0.60 - エントロピー×0.30 + 20, 0, 100)

情報汚染度 = clamp(フェイク情報×0.50 + AI軍事利用×0.20 - 真実密度×0.30, 0, 100)
```

---

## 技術仕様 / Technical Specs

| 項目 | 内容 |
|---|---|
| 構成 | HTML + CSS + JavaScript（単一ファイル） |
| 外部依存 | なし（ライブラリ不使用） |
| 対応環境 | モダンブラウザ全般 |
| ホスティング | GitHub Pages |

---

## 関連レポート・書籍 / Related Reports & Books

このCalculatorは以下の著作・レポートの思想に基づいている。

### 書籍
- **人類は必ず絶滅する 2026** — JP: https://amzn.to/4ryj2Nz / EN: https://amzn.to/4b7Vt9x
- **侵略の21世紀 2026** — JP: https://amzn.to/4sdzGU5 / EN: https://amzn.to/4bkJVPa
- **イランAI戦争 2026** — JP: https://amzn.to/4aYlXKL / EN: https://amzn.to/4rhrv7W

### GitHubレポート
- [人類残存時間の計算](https://github.com/choiizuka/Mathematical-Calculation-of-Humanity-s-Remaining-Lifespan)
- [Eden Protocols — 反戦科学](https://github.com/choiizuka/Eden_Protocols-Anti-War_Scientific_Report)
- [SNSフェイク情報の確率と有害度](https://github.com/choiizuka/The-Probability-and-Toxicity-of-Fake-Information-on-SNS)
- [人類絶滅の確率の超シンプルな証明](https://github.com/choiizuka/The-Simple-Proof-of-Human-Extinction-Probability)
- [全レポート一覧 (reports-index)](https://github.com/choiizuka/reports-index)

### 2026年宣言
- JP: https://choappceo.wordpress.com/2026/03/10/2026-manifesto-intelligence-ai-and-human-responsibility/
- EN: https://choiizuka.wordpress.com/2026/03/10/2026-manifesto-intelligence-ai-and-human-responsibility/

---

## 今後の予定 / Roadmap

- **v1.1 — Simulator版**: アニメーションで変数の変化が視覚的に動く版
- **AI War Decision Simulator**: AI軍事判断・誤爆率・エスカレーション確率を扱う拡張版

---

## 作者 / Author

**CHOIIZUKA (Toshihide Choiizuka)**

- Web JP: https://choappceo.wordpress.com/
- Web EN: https://choiizuka.wordpress.com/
- GitHub: https://github.com/choiizuka
- X: https://x.com/choiizuka
- YouTube: https://youtube.com/@choiizuka/

---

*Civilization OS Calculator v1.0 — CHOIIZUKA 2026*
