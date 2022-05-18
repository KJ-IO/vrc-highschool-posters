# vrc-highschool-posters

2022/5/18

ポスター更新手順のメモ by イオさん

ffmpegがインストールされていない場合はインストールする
https://jp.videoproc.com/edit-convert/how-to-download-and-install-ffmpeg.htm

①掲載したいポスターを16枚選ぶ。画像は右側が上になるように回転しておく。  
また、jpgファイルはpngファイルに変換しておく（jpgのままだと正常に変換できない）。  
②授業スライドと同様に16枚を全選択してzip化する  
③あさげサーバーにアクセスし、左側メニューの「ツール→アトラス化ツール」を開く  
④②で作成したzipファイルをアップロードし、以下の設定を入力してダウンロードボタンをクリック  
１ページの幅：1024  
１ページの高さ：724  
横のページ数：4  
縦のページ数：4  
※「名前を付けて保存」ダイアログが表示された場合はファイル名を変えずに保存すること。  
⑤画像ファイルがダウンロードされたら、DL先のフォルダを開く  
⑥フォルダ内でShiftキーを押しながら右クリックし、「PowerShellウィンドウをここで開く」をクリック  
⑦起動したPowerShellに以下のコマンドをコピペしてEnter  
ffmpeg -framerate 1 -i atlas.png -c:v libx264 -r 30 -t 0.33 -pix_fmt yuv420p -s 4096x2896 posters.mp4  
⑧mp4ファイルが生成されるので、ローカルリポジトリのvrc-highschool-posters.git/posters/posters.mp4 に上書きコピーしてコミット&Push  