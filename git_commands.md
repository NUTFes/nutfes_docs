# よく使うgitコマンド一覧

### git clone 'レポジトリ'
- GitHubで公開されているリモートレポジトリをローカルにクローン(コピー)する
- ex. `git clone git@github.com:NUTFes/group-manager.git` => group-managerをローカルにクローン

### git status
- (gitで管理しているレポジトリ上の)ファイルの変更点や現在のブランチなどの状態を表示する

### git log
- 過去のコミットの一覧を表示する

### git branch
- ブランチの一覧を表示する

### git checkout 'branch'
- ブランチを<branch>に切り替える
- ex. `git checkout develop` => developブランチに切り替える

### git checkout -b 'new_branch'
- 新しい<new_branch>という名前のブランチを作る
- ex. `git checkout -b issue100` => issue100という名前のブランチを作成

### git init
- 現在のディレクトリをgitで管理することを開始する
- (.git/というディレクトリが作られる)

### git diff 'file'
- (ステージに乗せていない変更ファイルの)変更箇所を表示する

### git add 'file'
- 変更したファイルをステージに乗せる(セーブする変更ファイルを指定する)

### git commit -m 'commit_massage'
- ステージに乗っている変更ファイルをコミットする(セーブポイントを作る)
- ex. `git commit -m 'ダッシュボードの表示ミスを修正'`

### git remote -v
- 登録されているリモートリポジトリを確認する

```
$ git remote -v
origin	github:NUTFes/group-manager.git (fetch)
origin	github:NUTFes/group-manager.git (push)
```

### git push origin master
- コミットをGitHubにプッシュする(セーブポイントをアップロードする)
- 正確に言うと `git push <リモートリポジトリの名前> <branch>`

### git pull --rebase
- リモートリポジトリの変更点をローカルリポジトリに適用する

### git checkout .
- 変更したファイルを変更前の状態に全て戻す

### 用語
`リモートリポジトリ`: GitHub上で公開されているリポジトリ  
`ローカルリポジトリ`: 自分のPC上のgitで管理されているレポジトリ  
`ブランチ`: 木の枝のイメージ. どの枝にセーブポイントを付けるか.  
`ステージ`: pushしたい変更ファイルをステージに乗せるイメージ  
`ブランチを切る`: 新しくブランチを作ること  

# 順番

0.ブランチを切る
```
git checkout -b <issue名>
```
### 〜〜group-manager編集〜〜
1.編集したファイルを確認
```
git status
```
2.編集したファイルをadd
```
git add <編集したファイル名>
```
3.編集したファイルをcommit
```
git commit -m "コミットメッセージ"
```
4.編集したファイルをpush
```
git push origin <ブランチ名>
```
