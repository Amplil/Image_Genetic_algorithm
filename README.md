# 遺伝的アルゴリズムで画像つくるやつ
 動作の流れ
1. プログラムファイルのダウンロード。コマンドラインにてプログラムフォルダへ移動
1. gen0.py を走らせると0世代目のデータが128種書かれたファイル gen0.txtができます
1. ui_select.py を走らせます。tmp.png というファイルが生成されます。
1. ui_show.py を走らせると、1秒間隔でtmp.png が更新されます
  （要：Chromeのダウンロード & chromedriverのバージョン合わせ）
1. ui_select.py の実行画面で、tmp.png のどちらが目標の画像に近いか選んで入力。（左の場合「j」、右の場合「k」）
1. 64回の選択を終えると、select1.txt という今まで選択したgen0.txtのインデックス番号が記録されたファイルが生成されます。
1. もういちどui_select.py を走らせ、画像を選びます。
1. 4~6の作業を select5.txtが生成されるまで繰り返します。
1. crossing.py を走らせます。select5.txt に基づき次世代のデータが128種生成されます。
1. 2~8の作業を気が済むまで繰り返します。
