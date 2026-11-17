# Yusuke F.

薬剤師・エンジニアです。医用画像 AI、病院薬剤部の業務支援及び機械学習の運用基盤について、再現できる実装と、評価の限界を明示した文書を公開しています。

> **注記** 公開物は、研究及びポートフォリオの提示を目的とします。いずれも医療機器ではなく、診療又は調剤の判断に用いるものではありません。実在の患者及び職員のデータは収録していません。

## 1. 活動領域

### 1.1 医用画像 AI

| リポジトリ | 内容 |
|---|---|
| [isles2022-2p5d-reproducible-pipeline](https://github.com/yskfuji/isles2022-2p5d-reproducible-pipeline) | ISLES 2022 の脳梗塞病変セグメンテーション。2.5D の2モデルによるアンサンブルで、ローカルのテストの平均 Dice は 0.631 です（3D U-Net ベースライン 0.514 に対し +22.8%）。 |
| [isles2022-3d-reproducible-pipeline](https://github.com/yskfuji/isles2022-3d-reproducible-pipeline) | 3D U-Net によるベースライン。しきい値及び後処理のスイープと、病変の大きさ別の報告を含みます。 |
| [isles2022-2d3d-blend-reproducible-pipeline](https://github.com/yskfuji/isles2022-2d3d-blend-reproducible-pipeline) | 2D・3D・2.5D の異種アンサンブル。アーキテクチャをまたぐ確率の融合と、症例に応じたしきい値処理により、独自に分けた25症例のテストで平均 Dice 0.7527。 |
| [rsna-ich-reproducible-pipeline](https://github.com/yskfuji/rsna-ich-reproducible-pipeline) | 頭蓋内出血の分類。検査単位のグループ分割評価、校正の解析及び FastAPI のデモを含みます。代表指標は1エポックの追加学習に基づく値であり、未知の検査に対する性能ではありません（[評価ノート](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/docs/evaluation_notes_ja.md)）。 |

### 1.2 病院薬剤部の業務支援

| リポジトリ | 内容 |
|---|---|
| [PharmShiftMaker](https://github.com/yskfuji/PharmShiftMaker) | 病院薬剤部の勤務計画、申請及び当日運用を支援する試作ソフトウェア（FastAPI、Next.js、PostgreSQL）。合成データで検証しています。 |
| [synthetic-prescription-ocr-eval](https://github.com/yskfuji/synthetic-prescription-ocr-eval) | 合成した処方箋画像の読み取り評価基盤。AWS のサーバーレス構成で、Tesseract と Amazon Bedrock の Claude を、正解率・処理時間・費用で比較します。 |

### 1.3 機械学習の運用基盤（MLOps）

| リポジトリ | 内容 |
|---|---|
| [cmapss-fd004-rul-mlops](https://github.com/yskfuji/cmapss-fd004-rul-mlops) | NASA CMAPSS FD004 による残存耐用時間（RUL）の予測。再現できる GBDT のベンチマークと、予測・バックテスト・監視を提供する FastAPI のサービスを含みます。 |

### 1.4 生活支援アプリケーション

| リポジトリ | 内容 |
|---|---|
| [FamilyHub-pipeline](https://github.com/yskfuji/FamilyHub-pipeline) | 家族の予定、タスク、メモ及び家計をまとめて確認する「よりどころ」の参照実装。Web の画面と API サーバーを含みます。 |

### 1.5 オープンソースへの寄与

| リポジトリ | 内容 |
|---|---|
| [ATAS](https://github.com/yskfuji/ATAS)（fork） | 動画生成のフレームワーク [ziplab/ATAS](https://github.com/ziplab/ATAS) を、Apple Silicon（MPS/Metal、CPU）で動かすための対応（作業中）。 |

## 2. 共通の方針

1. **再現性**：手順、設定及び評価を、第三者が端から端まで追える形で公開します。
2. **評価の限界の明示**：代表指標だけでなく、データの分割、校正及び学習データとの重なりなどの制約を併記します。
3. **安全な公開**：実在の患者及び職員のデータを使わず、合成データ又は公開データセットで検証します。

---

## Summary (English)

Pharmacist and engineer. I publish reproducible implementations and evaluation-aware documentation in three areas:

- **Medical imaging AI** — ISLES 2022 ischemic stroke lesion segmentation (2.5D, 3D U-Net, and 2D/3D/2.5D blend pipelines) and RSNA intracranial hemorrhage classification.
- **Hospital pharmacy operations** — [PharmShiftMaker](https://github.com/yskfuji/PharmShiftMaker), a prototype for pharmacy department shift planning, and a serverless OCR evaluation on synthetic prescriptions.
- **MLOps and applications** — CMAPSS FD004 remaining-useful-life forecasting with a FastAPI service, a family-life reference app, and Apple Silicon support work for ATAS.

All repositories are for research and portfolio purposes, are **not medical devices**, and contain no real patient or staff data.
