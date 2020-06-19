# 初めてチーム開発にJOINしたときにmustで使うgitコマンド

チュートリアルが出来る準備をする。

- 自分のgithubのリモートリポジトリを作成する
- 作成した場所になにかファイルをアップロードする
- 自分のローカルの開発場所に移動する

1. ローカルにリポジトリを作成する
 - git clone <リモートリポジトリのurl>

3. プッシュしたいリモートリポジトリのURLを追加する
 - git remote add origin URL

2. リモートのmasterブランチの最新の状態をローカルリポジトリの現在のブランチにマージする
 - 下記のどれでも同じ挙動です。
 - git pull origin master
 - git pull
 - git fetch → git merge origin/master

4. コミット履歴を確認する
 - git log --graph --oneline --decorate

5. ローカルリポジトリで新しいブランチを作成して移動する
  - 下記のどれでも同じ挙動です。
 - git checkout -b feature/hoge
 - git branch feature/hoge → git checkout feature/hoge

6. hogeの機能を開発する。githubflow_practice.mdファイルを保存。


7. ステージにファイルを追加する
 - git add githubflow_practice.md

8. ステージにファイルが追加されているか確認する
 - git status

9. ステージに追加したファイルをローカルリポジトリにコミットする
 - git commit -m "これは開発メンバーへのメッセージです。機能hogeを開発しました。"
 - git commit → vimが立ち上がるのでメッセージを記入して esc+:wq を入力

10. 開発した機能をリモートリポジトリにプッシュする
 - git push origin feature/hoge

11. githubのWEBサイトに移動してプルリクエストを作成する
 - レビュワーをきめる

12. レビュワーがレビューして問題なければmasterブランチにマージする

