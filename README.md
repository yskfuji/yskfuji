# Yusuke F.

Medical imaging ML engineer focused on reproducible MRI and CT pipelines, audit-ready documentation, and practical evaluation workflows.

医用画像 AI の再現可能な実装、監査しやすいドキュメント、実運用を意識した評価系の整備に取り組んでいます。

## Featured repositories

1. [isles2022-2p5d-reproducible-pipeline](https://github.com/yskfuji/isles2022-2p5d-reproducible-pipeline)
   Lightweight 2.5D ischemic stroke lesion segmentation for ISLES 2022 with a two-model ensemble, calibration utilities, and reproducibility notes.
2. [isles2022-3d-reproducible-pipeline](https://github.com/yskfuji/isles2022-3d-reproducible-pipeline)
   Reproducible 3D U-Net baseline for ischemic stroke lesion segmentation with threshold and postprocess sweeps.
3. [rsna-ich-reproducible-pipeline](https://github.com/yskfuji/rsna-ich-reproducible-pipeline)
   Reproducible intracranial hemorrhage classification workflow with group-split evaluation, calibration analysis, and a public FastAPI demo surface.\
   Code: [dataset](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/core/pipeline/src/datasets/rsna_ich_dataset.py) · [training](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/core/pipeline/src/training/train_rsna_cnn2d_classifier.py) · [uncertainty evaluation](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/core/pipeline/tools/eval_rsna_uncertainty.py) · [evaluation notes](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/docs/evaluation_notes.md)\
   Caveat: the headline numbers come from 1-epoch fine-tuning and are not performance on unseen studies; see the evaluation notes.

## What I care about

- Reproducible medical imaging pipelines that can be reviewed end to end
- Clear evaluation protocols, not just headline metrics
- Public documentation that external reviewers can actually follow

## 公開中の主要リポジトリ

1. [isles2022-2p5d-reproducible-pipeline](https://github.com/yskfuji/isles2022-2p5d-reproducible-pipeline)
   ISLES 2022 向けの 2.5D 脳梗塞病変セグメンテーション実装です。2 モデルのアンサンブル、校正ツール、再現性資料を含みます。
2. [isles2022-3d-reproducible-pipeline](https://github.com/yskfuji/isles2022-3d-reproducible-pipeline)
   3D U-Net ベースの脳梗塞病変セグメンテーション実装です。しきい値と後処理のスイープを含め、公開レビューしやすい構成にしています。
3. [rsna-ich-reproducible-pipeline](https://github.com/yskfuji/rsna-ich-reproducible-pipeline)
   RSNA ICH challenge 向けの頭蓋内出血の分類実装です。検査単位のグループ分割評価、校正解析、FastAPI のデモを含みます。\
   コード：[データセット](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/core/pipeline/src/datasets/rsna_ich_dataset.py) · [学習](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/core/pipeline/src/training/train_rsna_cnn2d_classifier.py) · [不確実性の評価](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/core/pipeline/tools/eval_rsna_uncertainty.py) · [評価の注意点](https://github.com/yskfuji/rsna-ich-reproducible-pipeline/blob/main/docs/evaluation_notes_ja.md)\
   注意：代表指標は1エポックの追加学習による値で、未知の検査に対する性能ではありません。詳しくは評価の注意点を読んでください。

## 関心のあるテーマ

- 端から端まで追える再現可能な医用画像パイプライン
- 見かけのスコアだけで終わらない評価設計
- 外部レビュアーが迷わず読める公開ドキュメント