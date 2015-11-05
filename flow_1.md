# Gitの使い方

## 目的
　Gitの使い方を1から学ぶので備忘録として記録を残します．  
　~~最終的には，この文書だけでGitの使い方を学べるようにします．~~

## 目次
empty

## 基本的なコマンド一覧　

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
- 追加予定
	* 全体の流れ図
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
	* Gitについて
		+ Gitはバージョン管理システムのことです．
		+ バージョン管理システムとはその言葉の通りにバージョンを管理するシステムのことをいいます．ここで管理されるのはPC上で作成したり編集したりしたデータです．
		+ つまり__Gitとはデータの管理を人間の代わりにやってくれる便利なシステム__のことです．
	* ローカルリポジトリとリモートリポジトリ
	* Gitの基本
		+ init・add・commit
		+ Gitの最も基本的な使い方を学習しましょう．
		+ まず適当なディレクトリ（フォルダ）を作り，作ったディレクトリへ移動しましょう．
		+ `mkdir helloGit	# helloGitというディレクトを作成します．`

	* branch機能
		+ Gitはある時点のデータを軽量で残せます．
		+ Git以前のバージョン管理システムはファイルの差分を保存していたので，HDDを大変圧迫しました．
		+ 一方Gitは変更を加えたら気軽にその状態を残すことができます．←gitのすばらしいところ
