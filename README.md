# 大阪成蹊大学チャットボットデータ

このリポジトリには、大阪成蹊大学の入試情報に関するチャットボット用のQ&Aデータセットが含まれています。

## 概要

大阪成蹊大学の入試に関する質問に自動応答するチャットボットシステム（ロボコットGPT）のためのデータセットです。学部紹介、入試日程、出願手続き、キャンパス情報など、受験生が知りたい情報を網羅しています。

## ファイル一覧

### データファイル

- **qa_data4.csv** - メインのQ&Aデータセット（103エントリ）
  - 大学の理念・教育目的
  - 各学部の特色（経営、スポーツマネジメント、国際観光、教育、芸術、データサイエンス、看護）
  - 入試種別と日程（総合型選抜、公募推薦、一般選抜、共通テスト利用など）
  - 出願手続き・検定料
  - キャンパス施設・学生支援

- **20250707_サンプル(ロボコットGPT).csv** - CSV形式のサンプルファイル
  - チャットボットの基本的な応答パターン
  - システムメッセージの例

### ソースドキュメント

- **【最終】大阪成蹊大学募集要項2026 (1).pdf** - 2026年度入試募集要項（元データ）

## データ形式

CSVファイルは以下の形式で構成されています：

```
回答文,,,,,,,ID,質問1,質問2,質問3,,
```

- 第1列：チャットボットの回答文
- ID列：エントリの識別子（ID001〜ID100、特殊エントリ）
- 質問列：同じ回答を引き出す複数の質問パターン

### 特殊エントリ

- `welcome` - 初回挨拶
- `RECSTART` - 会話開始
- `RECPRGRS` - タイムアウト処理
- `anything_else` - 不明な質問への対応

## 使用方法

1. CSVファイルをチャットボットシステムにインポート
2. IDと質問パターンを基にマッチング処理を実装
3. ユーザーの質問に対して適切な回答を返す

## データ内容の例

```csv
大阪成蹊大学の建学の精神は「桃李不言下自成蹊」です。,,,,,,ID001,建学の精神は？,大学の理念は？,桃李不言って？,,
総合型選抜A日程の出願期間は9月1日〜9月11日です。,,,,,,ID012,総合型A出願期間？,A日程申込はいつ？,A日程締切は？,,
```

## 注意事項

- 文字コードはUTF-8を使用
- 一部のファイルの先頭にBOM（Byte Order Mark）が含まれる場合があります
- 日本語テキストを含むため、エディタの文字コード設定に注意してください

## 更新履歴

- 2025年7月 - qa_data4.csv作成（2026年度募集要項対応）

## ライセンス

このデータは大阪成蹊大学の公式募集要項を基に作成されています。使用に際しては大学の規定に従ってください。