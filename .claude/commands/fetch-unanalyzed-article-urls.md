# 分析済みでない URL のリストを取得する

ブログ記事のうち、分析が済んでいない記事の URL 一覧を最大 10 件取得します。

## 手順

- WebFetch ツールが利用可能であることを確認する
  - 利用できない場合は処理を中止する
- `analysis.md` 内の `分析対象ファイル` セクションから、分析済みファイル名リストを取得する
- `https://tadosuke.com/` から、分析済みファイル名リストに**含まれない**記事の URL を、更新日時が新しい順に 10 件取得する
  - ファイル名: URL の `https://tadosuke.com/` 以降の部分に対応
  - カテゴリ区切りの `/` はハイフンに変換
  - 例: `https://tadosuke.com/common/6808/` → `common-6808.md`
- URL リストの取得に失敗した場合は処理を中止する
- URL リストを改行区切りのプレーンテキストで回答する

## 具体例

```
https://tadosuke.com/programming/6840/
https://tadosuke.com/programming/6824/
https://tadosuke.com/programming/6808/
https://tadosuke.com/life/6793/
https://tadosuke.com/work/6779/
https://tadosuke.com/programming/6776/
https://tadosuke.com/programming/6770/
https://tadosuke.com/programming/6761/
https://tadosuke.com/english/6747/
```

## 注意事項

- ファイルの編集はしないこと
- 途中の処理に失敗した場合は処理を中止すること
