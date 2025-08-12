変更したファイルをステージング（変更し内容をGitHubにセーブ）する準備
git add -A

名前を付けて保存
git commit -m "日本語（保存名）"

ローカルにアップしたデータをリモートにあげる
git push origin ブランチ名


（注：最初だけ）リモートリポジトリとローカルリポジトリを紐づける
git remote add origin ssh名

SSHキーはエクスプローラー/Cドライブ/user/ユーザー/.ssh/なんちゃら.pub