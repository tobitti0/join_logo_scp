# CM自動カット位置情報作成 join_logo_scp for Linux
## 概要
これは[sogaani氏][1]がLinuxに移植された[join_logo_scp][2]をもとに  
[Yobi氏のv4.0.0][3]での更新内容を取り込みLinuxにて正常にビルドできるようにしたもの。

また、こちらは[JoinLogoScpTrialSetLinux][4]で使用するモジュールの1つです。  
単体でも動作しますが、Linux環境にてjoin logo scpを用いたCMカット環境構築を検討されているのであれば
[JoinLogoScpTrialSetLinux][4]を使用することをおすすめします。

[1]:https://github.com/sogaani
[2]:https://github.com/sogaani/JoinLogoScp/tree/master/join_logo_scp
[3]:https://github.com/yobibi/join_logo_scp/releases/tag/v4.0.0
[4]:https://github.com/tobitti0/JoinLogoScpTrialSetLinux

## 機能
事前に別ソフトで検出した
* ロゴ表示区間
* 無音＆シーンチェンジ
の情報を基にして、CMカット情報(Trim)を記載したAVSファイルを作成します。

## ビルド方法
srcでmakeしてください。  

## 使用方法
````
join_logo_scp -inlogo ファイル名 -inscp ファイル名 -incmd ファイル名 -o ファイル名 その他オプション
````
詳細はオリジナルの[readme](readme.txt)を参照してください。

## 謝辞
オリジナルの作成者であるYobi氏  
Linuxに移植されたsogaani氏  
に深く感謝いたします。

## 更新履歴
・Yobi氏のv4.0.0更新に追従（したがってNekopanda氏のv3.0.6nも適用）  
・sogaani氏のMakefileを修正しビルドできるようにした。
