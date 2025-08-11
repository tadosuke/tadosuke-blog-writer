# 全ての処理を実行する

分析結果の更新に必要な一連のコマンドを実行します。

## 手順

1. @.claude/commands/fetch-unanalyzed-article-urls.md の指示を実行し、URL リストを取得する
   引数で数字が指定された場合はコマンドの引数に渡す
2. @.claude/commands/analyze-article.md の指示を実行する
   (1) で取得した URL リストを引数とする
3. @analyses/ 以下にファイルが出力されたら、@.claude/commands/integrate-analyses.md の指示を実行する
4. 処理結果を報告する

## 注意事項

- 関係ないファイルは絶対に編集しないこと
- 途中の処理に失敗した場合は処理を中止すること
