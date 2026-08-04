# kafin2 — 未実装のAI金融ダッシュボード構想

> **状態: 未実装**  
> このリポジトリは、2024年に作成されたREADMEだけの構想文書です。実行可能なアプリケーション、データ、テスト、CI、公開環境は含まれていません。

## 目的

自然言語から金融データの取得・分析・可視化を指示できるダッシュボードの構想を記録しています。

構想上は、株価、経済統計、LLM、履歴保存、モバイルUIなどを一つの画面へ統合することを想定していました。ただし、これらは現在のdefault branchへ実装されていません。

## 現在の実体

2026年8月5日の監査時点で確認できるのは`README.md`だけです。

| 項目 | 状態 |
|---|---|
| アプリケーションコード | なし |
| `requirements.txt`または依存lock | なし |
| データ・schema | なし |
| テスト | なし |
| GitHub Actions | なし |
| Streamlit設定 | なし |
| database設定 | なし |
| 公開deploymentの証拠 | なし |

READMEの旧版に記載されていた`app/`、`data/`、`tests/`、`.github/workflows/`は存在しません。

## 現在できること

- 2024年時点の製品アイデアを確認する
- 将来実装する場合の要求候補として参照する

## 現在できないこと

- Streamlitアプリを起動する
- OpenAI、FRED、Google Driveへ接続する
- 自然言語から金融分析を生成する
- dashboardを保存・共有する
- 定期的にデータを更新する
- 公開URLで稼働状態を確認する

旧READMEに記載されていた公開URL、常時最新、完全無料、スケーラブルなどの表現は、現在のrepository実体では確認できないため撤回します。

## 再開する場合の最小条件

実装を再開する場合は、少なくとも次を追加する必要があります。

1. 正準なアプリケーションentrypoint
2. version固定された依存定義
3. 使用するデータ源、series ID、単位、取得日時の台帳
4. credentialをrepositoryへ保存しない設定
5. 実績、予測、LLM生成文の表示上の分離
6. 空データ、API失敗、古いcacheを成功扱いしない処理
7. unit testとend-to-end smoke test
8. deployment先とcommit SHAを照合できる公開証拠

## 金融情報の扱い

将来実装する場合でも、生成結果を投資助言、売買推奨、将来収益の保証として扱いません。株価・経済統計・企業財務は、出典、観測日、取得日、通貨、単位、改訂状態を保持する必要があります。

## 関連する監査

- README監査Issue: https://github.com/KAFKA2306/kafin2/issues/1
- 全repository README監査: https://github.com/KAFKA2306/com/issues/3

**README監査日:** 2026年8月5日
