# SIGNATE Beginner コンペ参加記録

📊 **成果**：195人中 2位（最終スコア 0.5301）、提出数 137件で最多\
📅 **開催期間**：2025年5月\
📍 **テーマ**：携帯電話の機能データから販売価格帯（4クラス）を分類\
📈 **評価指標**：マクロ平均F1スコア（0～1、1に近いほど良い）

---
## ノートブック構成
* **EDA.ipynb**\
  データの可視化・基礎分析（EDA）を実施
* **TRAIN.ipynb**\
  特徴量の追加・モデルの学習（LightGBM / XGBoost / TabPFN）
* **INFER.ipynb**\
  学習済みモデルを用いた予測、testデータに対する推論、提出用ファイル作成
---
## アプローチと工夫
* One-vs-All手法で LightGBM モデルを作成
* XGBoost と TabPFN を組み合わせたアンサンブルを実施
* 少量データへの適応として TabPFN を活用
* 投稿数を重ねて多くの仮説検証を実施（137件）
---
## 学び
* 短期間での仮説検証サイクルの重要性を実感
* モデル選定により精度が大きく変わることを体感
* TabPFN は小規模データに強いが、実務適用はケースバイケース
---
## 環境構築
本プロジェクトは **Google Colab** 上で実行しました。\
Colab 環境において必要なライブラリを `pip install` することで再現可能です。
```
!pip install pandas numpy scikit-learn lightgbm xgboost tabpfn matplotlib seaborn
```
---
## 使用ライブラリ
* **pandas**：データ前処理
* **numpy**：数値計算
* **scikit-learn**：モデル評価、データ分割
* **lightgbm**：勾配ブースティングモデル
* **xgboost**：勾配ブースティングモデル
* **tabpfn**：少量データ用モデル（Transformerベース）
* **matplotlib / seaborn**：データ可視化
