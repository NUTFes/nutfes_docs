### WN_AC1167GRのマニュアル

#### ブラウザのプロキシをオフ 
ルータの設定に入る前にブラウザのプロキシをoffにする

#### SSID, パスワードの変更
1. 起動
ルータ背面の[ルータ/自動]スイッチを[ルータ側]に設定.  
そして, 電源を入れる.  

2. 設定画面にアクセス
SSID : stream00886
SSID : AirPort00886
どちらでも良いのでアクセス.   
パスワードは筐体に書いてあるものを入力.  
もしくは, ``gidaifes``  
ブラウザで``192.168.0.1``にアクセス

3. パスワードの再設定
無線設定 -> 暗号化に飛ぶ
パスワードを変更するSSIDを選択する.  
stream, airportともに変更する.  
PW : gidaifes
一度wifiとの接続が切れるので再接続必須.  

4. SSIDの再設定
stream, airportともに``nutfes_soumu``に変更する.  
一度wifiとの接続が切れるので再接続必須.  

#### APモードとして再起動
5. APモードにする
まずは, ルータ背面の[ルータ/自動]スイッチを[ルータ側]に設定されていることを確認.    
電源が入っているなら一度電源コードを抜く.  
その後, WANポートにLANケーブルを挿入.   
再度電源コードを接続.  

その後, ``192.168.0.1``に接続.  
``インターネット``タブを開き, APモードにチェック.  
設定をクリック.  

#### ブラウザのプロキシをONに
プロキシをオンにして, 接続できるか試す.  
うまくいかない場合は, APモードにうまく移行できていない可能性がある.  
MagicFinderという純正APPを入れて設定画面に行き, APモードに再度設定するとうまくいった.  


