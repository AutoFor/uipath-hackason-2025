# 🏥 カルテからレセプトへの業務自動化 with UiPath Agentic Automation

## 📄 提案書（日本語）

👉 [提案書はこちら（docs/Proposal.md）](https://github.com/AutoFor/uipath-hackason-2025/blob/draft/docs/00_Proposal.md)

このリポジトリの詳細な提案背景、課題構造、活用技術などは上記Markdownにまとめています。

---

## 概要

本リポジトリは、UiPath主催のグローバルハッカソン **AgentHack 2024** に向けた提案プロジェクトです。

日本の医療現場における「カルテ（EMR）」と「レセプト（診療報酬請求）」の乖離を、**RPA × AI × エージェント型オートメーション（Agentic Automation）**の力で解決する仕組みを提案します。

---

## 🎯 解決したい課題

| 課題                          | 説明                                                                 |
|-----------------------------|----------------------------------------------------------------------|
| 用語の乖離                    | 医学的なカルテ記載と言語が異なるため、機械変換が困難                        |
| 自由記載テキストの処理         | 「朝から頭痛が…」のような自然言語記述の構造化が困難                         |
| 転記作業の手間とヒューマンエラー | 医事課がEMRを見ながら手動入力するためミスや工数が発生                        |
| 制度改正対応の難しさ           | 請求ルールが頻繁に変わるため、ツール側の対応も複雑                           |
| 属人化したノウハウの継承        | ベテランの経験が暗黙知化し、若手職員の教育コストが高い                       |

---

## 🧩 提案ソリューション構成

### Step 1：EMRからの構造化抽出（AI）
- EMR記録から診療行為・診断名・処方などを抽出（LLM + NLP）
- 抽出結果をEMR上・Action Center上に表示
- 医師による「承認／保留」操作で学習フィードバック

### Step 2：レセプト作成・提出（RPA）
- AI抽出内容をもとに、レセコンへRPAで自動入力
- 提出・返戻処理も自動対応し、医事課に通知

### Step 3：Agentic Automation（Coded Agents + Maestro）
- LLMベースの診療内容変換エージェントを用意
- ガイドラインや症例ナレッジをもとに点数コード候補を提示

### Step 4：改善と学習のループ
- 返戻理由の分析 → 抽出ルールやプロンプト改善
- 医事課の手動修正結果も再学習データに活用

---

## 🔧 使用技術

| 分類 | 技術・サービス |
|------|----------------|
| RPA  | UiPath Studio / Orchestrator / Action Center |
| AI   | Coded Agents / OpenAI GPT / 日本語医療BERT (商用利用可否要検討) |
| 自動化基盤 | UiPath Agent Builder / Maestro / Coded Agents |
| データ抽出 | Document Understanding / OCR |
| 提出管理 | レセプトソフト連携（UI操作ベース） |

---

## 📈 期待される効果

- **医事課の工数最大50%削減**
- **返戻率の低減（取り漏れ・記載不備の防止）**
- **AIによる若手教育支援・属人性排除**
- **制度改正への柔軟な追従**
- **現場に負担をかけない形で自然に制度理解を促進**

---

## 📅 スケジュール（ハッカソン用）

| 期間         | 内容                             |
|--------------|----------------------------------|
| ～7月7日     | アイデア提出・リポジトリ作成完了         |
| 7月8日～7月末 | プロトタイプ実装・PoC構築               |
| 8月上旬       | 動画提出・最終提出・最終調整             |

---

## 📎 リンク・参考資料

- [UiPath AgentHack公式ページ](https://community.uipath.com/events/details/uipath-hackathons-presents-agenthack/)
- [日本医療情報学会 医療NLPリソース](https://www.jami.jp/)
- [厚生労働省 診療報酬点数表](https://www.mhlw.go.jp/stf/seisakunitsuite/bunya/0000177182.html)

---

## 🧑‍💻 コンタクト

**提案者**：Seiya Kawashima  
**所属**：AutoFor株式会社（福岡）  
**連絡先**：seiya-kawashima@autofor.co.jp  
**GitHub**：[AutoFor](https://github.com/AutoFor)

---

📌 ご質問・フィードバックは Pull Request または Issues までお願いします。
