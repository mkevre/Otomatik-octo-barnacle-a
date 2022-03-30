When you use the repository's `GITHUB_TOKEN` to perform tasks, events triggered by the `GITHUB_TOKEN` will not create a new workflow run. これによって、予想外の再帰的なワークフローの実行が生じないようになります。 たとえば、ワークフローの実行によってリポジトリの`GITHUB_TOKEN`を使ったコードのプッシュが行われた場合、そのリポジトリに`push`イベントが生じた際に実行されるよう設定されたワークフローが含まれていても、新しいワークフローの実行は行われません。