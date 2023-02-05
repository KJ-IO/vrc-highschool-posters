# vrc-highschool-posters

2023/2/6 10期～

１．アトラス化ツール（せとかイオさんが持ってる）で８枚ずつアトラス化する。
→使い方はツール内readmeを参照
config.json設定値は
{
    "unit_width": 1920,
    "unit_height" : 2160,
    "horizontal_element_count" : 4,
    "vertical_element_count" : 2
}
２．Slidenアップローダーでコマ送り動画を作る。
・https://sliden.app/ を開く
・Discordで認証
・「スライドをアップロードする」クリック
・アトラス化ツールでエクスポートした画像を投入
・アップロードできたら右上の『VRChatで再生』でURLをコピー
・URLをそのままブラウザで開き、右クリックでファイルとして保存
３．出来上がった動画をDLしてGithubにPush
vrc-highschool-posters\posters\SeekPosters.mp4として保存し、mainブランチへコミット&プッシュする。