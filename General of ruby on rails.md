# Ruby on Railsの基本

## 前回までの勉強会の流れ
- ルーティングの確認
	* config/routes.rb
	* rake routes
- コントローラの動作確認(app/controllers/user_controller.rb)
	* localhost:3000/usersにアクセス
	* indexメソッドを確認
- 新規レコードの作成
	* localhost:3000/usersにアクセス→レコードを作成する
	* newメソッドを確認
	* rails console でも新規レコードを作成
- バリデーションの設定
- show,edit,update,createの動作を確認

## Railsアプリの読み方
### 1. Railsの基本的な動作
　Railsでは以下のようにユーザのリクエストに応答します．  

1. アクセスURLからコントローラとメソッドを探し出す．
2. 探し出したメソッドを実行する．
3. __app/views/コントローラ名/メソッド名.html.erb__からhtmlを生成して返す．

### 2. ルーティングの確認
　ルーティングを確認するにはコンソールで`rake routes`を実行します．  
　例えば以下のような応答が返ってきます．  

```
welcome_index	GET	/welcome/index(:format)	welcome#index
```

　これは，`http://localhost:3000/welcome/index.html`にGETメソッドでアクセスすれば`welcome_contoroller`というコントローラの`index`というメソッドが実行されることを意味します．コントローラは__app/contorollers/welcome_contoroller.rb__に存在するファイルです．  

コントローラ内ではindexメソッドは以下のように記述されています．

```ruby:welcome_contoroller.rb
def index

.
.
.

end			# ここで，index.html.erbからhtmlを生成
```

　このとき，endの行で__app/views/welcome/index.html.erb__からhtmlを生成し，クライアントに返してブラウザに表示させます．

### 3. viewファイルのrenderについて
　コントローラはviewファイルからhtmlを生成して，クライアントに送ります．例えば以下のように記述されていたとします．

```ruby:app/views/welcome/index.html.erb

.
.

<%= render 'dashboard' %>
.
.

```

　この場合，`<%= render 'dashboard' %>`は__app/views/welcome/_dashboard.html.erb__をこの位置に展開するという動作を実行します．
　Viewファイルでは<%= %>で囲まれた部分はrubyプログラムとして実行されます．

### 4. MVCモデルについて
　Ruby on Railsでは MVCモデルというモデルに乗っ取ってアプリケーションを作成することになります．モデル(Model)，ビュー(View)，コントローラ(Controller)それぞれの頭文字を取ってMVCモデルです．MVCモデルではコクライアントからのリクエストをントローラが受けて，モデル，ビューと連携して，何らかの応答を返します．また，モデルはデータベースとのやり取りを担い，ビューはレスポンスのhtmlのもとになります．
