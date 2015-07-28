checklist_merge
====

コミックマーケット DVD-ROM 版カタログのチェックリストについて、複数のチェックリストを1つのリストにマージするためのツールです。

## Requirement

Perl 5.x が動作する環境、なおかつ以下のモジュールが必要
* Text::CSV_XS

## Install

    $ git clone https://github.com/CRUSADER-jp/checklist_merge.git

## Usage

あらかじめ、チェックリストのファイル名を以下のようにしておきます。

`C87_hoge.csv`

ファイル名の内、アンダースコアで区切られた後の部分(この場合はhoge)が、チェックリストの識別名になります。チェックリストを作った人の名前にしておくとよいかと。

その上で、以下のように実行します。

`perl checklist_merge C87_hoge.csv C87_fuga.csv C87_piyo.csv`

すると、チェックリストがマージされ、カレントディレクトリにmerged.csvという名前で出力されます。  
メモ欄については、頭に識別名の頭文字が付与されます。複数名が同一のサークルをチェックしていた場合は、それぞれのメモ欄の内容を結合して保存します。

<TODO: マージ前後のわかりやすい比較画像を載せる>

## Author

CRUSADER crusader1jp[at]gmail[dot]com
