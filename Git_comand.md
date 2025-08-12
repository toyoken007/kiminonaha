## ローカルで作成する場合
任意のフォルダで
1 git init
2 git remote add origin git@github.com:takuya0018/dev_environment-macmini.git

## gitからクローン
sshで対象をクローン
ターミナルで
1 git clone git@github.com:<ユーザー名>/<リポジトリ名>.git ディレクトリー名

## 作業開始
1 git pull origin master                  （最新版にする）
2 git branch <ブランチ名>                   （git branch　で一覧が見れる）
3 git checkout <ブランチ名>                 （git branch　で一覧が見れる）

* git checkout -b <新規ブランチ> <既存ブランチ>    既存ブランチから新規ブランチを作成しチェックアウト
* git checkout -b <ブランチ名>          これだとブランチ作成とチェックアウトが一緒にできる

## 作業が終わったら
4 git status
5 git add -A
6 git commit -m "Commit message"
7 git push origin master                   (git push <リモート名><ブランチ名>)

* git push origin develop:develop          (git push <レポジトリ名> <ローカルブランチ名>:<リモートブランチ名> *:<リモートブランチ名>を省略するとリモートブランチと同じ所にプッシュされる)

* git commit -am "Commit message"              これだとステージ・コミットが一回で出来る

## 公開したくないファイル・git管理から除外するファイル
.gitignoreファイルを作る（indexがある所でいい）
ファイル名を拡張し付きでかく

## ローカルからブランチを削除
git branch -D <ブランチ名>

## リモートブランチを削除
git push --delete origin <ブランチ名>

## 作成したmasterブランチをmainに変更
git branch -m master main

## 差分の確認
git diff                                  (終わる時は半角qを押す)

## ローカルでの変更を元に戻す
git checkout .
git checkout <ファイル名>                   (こちらはファイルで変更した物だけを元に戻す)
                  
## ローカルブランチとリモート別ブランチの差分を取り込みたい
git merge origin/master                   （変更を加えたいブランチにチェックアウトし`git merge fuature/test` みたいな変更されたブランチ名を入れる）

<!-- 例 -->
1 git fetch origin master                       (masterブランチのリモート追跡ブランチ origin/master を最新の状態にする)
2 git diff <ローカルブランチ> origin/master       (masterブランチ（リモート追跡）と⚪︎⚪︎⚪︎ブランチの差分を比較)
3 git merge origin/master                       (差分をマージ)