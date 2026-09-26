# CM自動カット位置情報作成 join_logo_scp

## 概要

このリポジトリは [Yobi氏の join_logo_scp](https://github.com/yobibi/join_logo_scp) に追従しています。
現在の取り込み対象は [v5.1.1](https://github.com/yobibi/join_logo_scp/releases/tag/v5.1.1)
（コミット `4107b3e0e1a798287603b76b8d6d734c9c01396a`）です。

以前は [sogaani氏のLinux移植版](https://github.com/sogaani/JoinLogoScp/tree/master/join_logo_scp) をもとに、
Linuxでビルドするための修正を加えていました。現在は公式版がLinuxに対応しています。
ソース、makefile、JLスクリプトは公式版のものであり、独自のLinux対応の変更はありません。

また、こちらは [JoinLogoScpTrialSetLinux](https://github.com/tobitti0/JoinLogoScpTrialSetLinux) で使用するモジュールの1つです。
単体でも動作しますが、chapter_exeやlogoframeで検出した情報を入力として使用します。
Linux環境でjoin_logo_scpを用いたCMカット環境の構築を検討されているのであれば、
[JoinLogoScpTrialSetLinux](https://github.com/tobitti0/JoinLogoScpTrialSetLinux) を使用することをおすすめします。

## 機能

事前に別ソフトで検出したロゴ表示区間と無音・シーンチェンジ情報から、
CMカット情報（Trim）を記載したAVSファイルを作成します。

## Linuxでのビルド方法

C++17に対応したC++コンパイラとmakeが必要です。Ubuntuでのコマンド例は下記の通り。

```sh
sudo apt-get update
sudo apt-get install -y build-essential
make -C src
```

## 使用方法

```sh
./src/join_logo_scp \
  -inlogo ロゴ検出結果.txt \
  -inscp チャプター検出結果.txt \
  -incmd JL/JL_標準.txt \
  -o 結果.avs
```

JLスクリプトは `JL/common` などの関連ファイルも使用するため、実行ファイルの更新時には
`JL` ディレクトリ一式も同じバージョンに更新してください。
詳細は公式の [readme](readme.txt)、[JLスクリプトの説明](JL/doc/readme_JL.txt)、[修正内容](修正内容.txt) を参照してください。

## 謝辞

オリジナルの作成者であるYobi氏、Linuxに移植されたsogaani氏に感謝いたします。

## 更新履歴

- Yobi氏のv5.1.1に追従。公式のLinux対応を採用し、従来の互換処理と独自Makefileを廃止。
- Yobi氏のv4.1.0に追従。
- Yobi氏のv4.0.1に追従。
- Yobi氏のv4.0.0に追従（Nekopanda氏のv3.0.6nも適用）。
- sogaani氏のMakefileを修正し、Linuxでビルド可能に変更。
