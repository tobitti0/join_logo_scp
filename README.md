# CM自動カット位置情報作成 join_logo_scp for Linux
## 概要
これは[sogaani氏][1]がLinuxに移植された[join_logo_scp][2]のmakeを修正したもの。

[1]:https://github.com/sogaani
[2]:https://github.com/sogaani/JoinLogoScp/tree/master/join_logo_scp

## 機能
事前に別ソフトで検出した
* ロゴ表示区間
* 無音＆シーンチェンジ
の情報を基にして、CMカット情報(Trim)を記載したAVSファイルを作成します。

## 使用方法
srcでmakeしてください。  
利用方法は次のとおりです。
````
join_logo_scp -inlogo ファイル名 -inscp ファイル名 -incmd ファイル名 -o ファイル名 その他オプション
````
詳細はオリジナルのの[readme][3]を参照してください。

[3]:https://github.com/tobitti0/join_logo_scp/blob/master/readme.txt

## 謝辞
オリジナルの作成者であるYobi氏  
Linuxに移植されたsogaani氏  
に深く感謝いたします。
