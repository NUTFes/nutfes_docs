# Gitの使い方

## 目的
　Gitの使い方を1から学ぶので備忘録として記録を残します．
　~~最終的には，この文書だけでGitの使い方を学べるようにします．~~

## 目次
empty

## 1日目まとめ　

```
# ローカルリポジトリの作成
git init

# file_nameをindexに反映→この操作をステージングするとも言います．
git add [file_name]

# indexの内容をリポジトリに反映
git commit

# branchの一覧を表示します
git branch
# 新しくbranch_nameというbranchを切ります
git branch [branch_name]

# branchを切り替えます
git checkout [branch_name]

# トラッキングされているファイルの変更状態を表示します．ユーザがcommitするファイルを選択するときの参考に使います．
git status

# コマンドを実行したシステムのカレントディレクトリにリポジトリをコピーします．
git clone [repository_address]

# remoteRipositoryの状態をbranch_nameの状態に置き換えます．
git push [remoteRipository] [branch_name]

# branch_nameの状態をremoteRiposirotyの状態に置き換えます．
git pull [remoteRipository] [branch_name]

# 現在のbranchにbranch_nameの状態をマージします．
git merge [branch_name]
```

## memo
- やったこと
	* git init
	* git add
	* git commit
	* git branch
	* git status
	* git clone
	* git push
	* git pull
	* git merge
- 解説候補
	* Gitのインストール
	* ローカルリポジトリとリモートリポジトリ
	* Gitの基本
		+ init・add・commit
