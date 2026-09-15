# 『現場で使える製造業の画像検査自動化』全面改訂版の教材

西城戸 亮 著『現場で使える製造業の画像検査自動化：Python／OpenCVで作る実践サンプルと運用ノウハウ』第2版の実習用ファイルです。Pythonの基本操作を理解した読者を対象にしています。

## 教材ZIPをダウンロードする

**[教材ZIPをダウンロード（約169 MB）](https://github.com/sunnishi/opencv-inspection-book-2e-materials/releases/download/v2.0.0/opencv_inspection_code.zip)**

- 対応する教材：全面改訂版・2026年9月15日制作、v2.0.0
- ファイル名：`opencv_inspection_code.zip`
- [この版の配布ページ](https://github.com/sunnishi/opencv-inspection-book-2e-materials/releases/tag/v2.0.0)

ダウンロードにGitHubアカウントは不要です。配布ページの「Assets」から取得する場合は、`opencv_inspection_code.zip`を選んでください。自動表示される「Source code (zip)」と「Source code (tar.gz)」には、実習用の写真やコード一式は入っていません。

ZIPを展開し、`inspection.py`、`config.json`、`requirements.txt`、`samples`、`lessons`があるフォルダーを開きます。環境によって同名フォルダーが二重になる場合は、これらのファイルがある内側を使います。最初は書籍の第5章と、教材内の`README.md`に沿って進めてください。

## 収録内容

| 学ぶ内容 | 教材内の場所 |
| --- | --- |
| 第5章：画像読込みから判定・記録までの六段階実習 | `lessons` |
| キズ・異物、個数、幅、位置ずれ、色、QRコードの検査 | `inspection.py`、`config.json`、`samples` |
| 第20章：実写基板50枚による失敗・改善・評価 | `real_case` |
| 27ケースの一括検証と24の自動試験 | `verify.py`、`tests` |
| 書き込み式の帳票 | `templates` |

第20章の実写写真、分割表、固定済み設定・モデル、制作時の保存結果もZIPに収録しています。書籍本文のEPUB・PDFは配布物に含みません。

## 実行環境と検証範囲

制作時の環境はmacOS、Python 3.10.19、OpenCV 5.0.0、NumPy 2.2.6です。正確な版は教材内の`environment-tested.json`、検証内容は`VERIFICATION.md`を参照してください。

実写事例の固定評価用20枚では、正常10枚中3枚をNG、異常10枚中4枚をOKと判定しています。この結果を再現して、失敗の原因や評価方法を学ぶ教材です。工場での性能や採用可否を保証するものではありません。Windows実機、カメラ・PLC接続は未検証です。

## 利用条件と出典

収録コードは、自分の検査に合わせて改変・利用できます。依存ライブラリや別途取得するモデル・データは、それぞれの配布元の条件に従います。

実写画像・公式注釈はVisA、Zou et al.（2022）、CC BY 4.0です。出典、加工内容、条件は、ZIP内の`real_case/ATTRIBUTION.md`、`real_case/LICENSE-DATASET.txt`、`real_case/NOTICE.txt`に記載しています。写真とその加工物を再利用するときは、これらの帰属情報とライセンスを保持してください。

## ダウンロードしたファイルを確認する

[SHA256SUMS.txt](SHA256SUMS.txt)の値と照合できます。ZIP内にはファイルごとの一覧`PACKAGE_MANIFEST.json`も収録しています。

不具合や誤記は[Issues](https://github.com/sunnishi/opencv-inspection-book-2e-materials/issues)へお知らせください。使用OS、実行したコマンド、表示されたエラー、教材の版を添えると状況を確認しやすくなります。
