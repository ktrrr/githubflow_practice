# 初めてチーム開発にJOINしたときにmustで使うgit command

1. ローカルにリポジトリを作成する
 - git clone <リモートリポジトリのurl>

2. リモートのmasterブランチの最新の状態をローカルリポジトリの現在のブランチにマージする
 - 下記のどれでも同じ挙動です。
 - git pull origin master
 - git pull
 - git fetch → git merge origin/master

3. コミット履歴を確認する
 - git log --graph --oneline --decorate

4. ローカルリポジトリで新しいブランチを作成して移動する
  - 下記のどれでも同じ挙動です。
 - git checkout -b feature/hoge
 - git branch feature/hoge → git checkout feature/hoge

5. hogeの機能を開発する。githubflow_practice.mdファイルを保存。


6. ステージにファイルを追加する
 - git add githubflow_practice.md

7. ステージにファイルが追加されているか確認する
 - git status

8. ステージに追加したファイルをローカルリポジトリにコミットする
 - git commit -m "これは開発メンバーへのメッセージです。機能hogeを開発しました。"
 - git commit → vimが立ち上がるのでメッセージを記入して esc+:wq を入力

9. 開発した機能をリモートリポジトリにプッシュする
 - git push origin feature/hoge

10. githubのWEBサイトに移動してプルリクエストを作成する
 - レビュワーをきめる

11. レビュワーがレビューして問題なければmasterブランチにマージする

