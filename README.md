# 『現場で使える製造業の画像検査自動化』全面改訂版の教材

西城戸 亮 著『現場で使える製造業の画像検査自動化：Python／OpenCVで作る実践サンプルと運用ノウハウ』第2版の実習用ファイルです。Pythonの基本操作を理解した読者を対象にしています。

## 教材ZIPをダウンロードする

**[教材ZIPをダウンロード（約218 MB）](https://github.com/sunnishi/opencv-inspection-book-2e-materials/releases/download/v2.1.0/opencv_inspection_code.zip)**

- 最新の教材：v2.1.0（2026年10月18日）
- ファイル名：`opencv_inspection_code.zip`
- [この版の配布ページ](https://github.com/sunnishi/opencv-inspection-book-2e-materials/releases/tag/v2.1.0)

ダウンロードにGitHubアカウントは不要です。配布ページの「Assets」から取得する場合は、`opencv_inspection_code.zip`を選んでください。自動表示される「Source code (zip)」と「Source code (tar.gz)」には、実習用の写真やコード一式は入っていません。

ZIPを展開し、`inspection.py`、`config.json`、`requirements.txt`、`samples`、`lessons`があるフォルダーを開きます。環境によって同名フォルダーが二重になる場合は、これらのファイルがある内側を使います。最初は書籍の「はじめに」のクイックスタートか第5章、教材内の`README.md`に沿って進めてください。

### 以前の版（v2.0.0）

2026年9月15日版の書籍に対応する教材は、[v2.0.0の配布ページ](https://github.com/sunnishi/opencv-inspection-book-2e-materials/releases/tag/v2.0.0)に残しています。v2.1.0はv2.0.0のファイルと結果を変更せずに追加しているため、どちらの版の書籍でもv2.1.0を使えます。

## 収録内容

| 学ぶ内容 | 教材内の場所 |
| --- | --- |
| 第5章：画像読込みから判定・記録までの六段階実習 | `lessons/01〜06` |
| 第5章：USBカメラで撮って判定する実習7 | `lessons/07_camera.py` |
| キズ・異物、個数、幅、位置ずれ、色、QRコードの検査 | `inspection.py`、`config.json`、`samples` |
| 第15章：保存した結果をHTMLの一覧にする | `report_html.py` |
| 第20章：実写基板による失敗・改善・評価（三回の改善ラウンド） | `real_case` |
| 27ケースの一括検証と43の自動試験 | `verify.py`、`tests` |
| 書き込み式の帳票 | `templates` |

第20章の実写写真160枚、分割表、固定済み設定・モデル、制作時の保存結果もZIPに収録しています。書籍本文のEPUB・PDFは配布物に含みません。

## v2.1.0の変更点

- 追加：`lessons/07_camera.py`（第5章の実習7：USBカメラ）
- 追加：`report_html.py`（第15章：結果をHTMLの一覧にする）
- 追加：`real_case/run_case_v2.py`、`run_case_v3.py`、`patchcore_case.py`、`download_weights.py`（第20章の改善ラウンド）
- 追加：VisA PCB1の実写110枚（CC BY 4.0。出典とハッシュは`selection_v2.json`・`selection_v3.json`）
- 追加：`requirements-patchcore.txt`（第3ラウンドのPatchCoreを動かす場合だけ必要）
- 自動試験：24件 → 43件
- v2.0.0のファイルと結果は変更していません。

## 実行環境と検証範囲

制作時の環境はmacOS、Python 3.10.19、OpenCV 5.0.0、NumPy 2.2.6です。第20章のPatchCore（任意）はPyTorch 2.14.0、torchvision 0.29.0で確認しました。正確な版は教材内の`environment-tested.json`、検証内容は`VERIFICATION.md`を参照してください。

ResNet18の学習済み重みはZIPに含めていません。PatchCoreを試す場合は`python real_case/download_weights.py`で公式配布元から取得してください。PyTorchがない環境では、PatchCoreの試験は自動でスキップされます。

実写事例の結果は公開画像の画像単位のラベル一致で、失敗の原因や評価方法を学ぶための教材です。工場での性能や採用可否を保証するものではありません。Windows実機、実機カメラ（実習7）、PLC接続は未検証です。

## 正誤表

| 対象の書籍 | 場所 | 誤 | 正 |
| --- | --- | --- | --- |
| 2026年9月15日版 | 第10章「規格境界に確認の帯を設ける」 | 規格の外にある測定値もREVIEWになることの説明がない | 理由と、外側の帯をなくす別の設計を追記（2026年10月18日版） |
| 2026年9月15日版 | 付録D-3 | OpenCVの資料へのリンクが4.x版である理由の説明がない | 動作確認は5.0.0で、本書で使う関数の使い方は両版で共通、と追記 |
| 2026年9月15日版 | 第12章の見出し | Cannyは境界候補を細い線へする | Cannyは境界候補を細い線にする |

## 利用条件と出典

収録コードは、自分の検査に合わせて改変・利用できます。依存ライブラリや別途取得するモデル・データは、それぞれの配布元の条件に従います。

実写画像・公式注釈はVisA、Zou et al.（2022）、CC BY 4.0です。出典、加工内容、条件は、ZIP内の`real_case/ATTRIBUTION.md`、`real_case/LICENSE-DATASET.txt`、`real_case/NOTICE.txt`に記載しています。写真とその加工物を再利用するときは、これらの帰属情報とライセンスを保持してください。

## ダウンロードしたファイルを確認する

[SHA256SUMS.txt](SHA256SUMS.txt)の値と照合できます。ZIP内にはファイルごとの一覧`PACKAGE_MANIFEST.json`も収録しています。

## 質問・不具合の報告

本文の誤りや、教材が動かない場合は、[Issues](https://github.com/sunnishi/opencv-inspection-book-2e-materials/issues)から報告してください。使用OS、Pythonの版、教材の版、実行したコマンド、表示されたメッセージを添えると状況を確認しやすくなります。製品の画像や社内の情報は書き込まないでください。

## 動画で学ぶ

画面の操作を動画で見ながら進めたい方には、著者のUdemy講座「[Codex × OpenCV：画像検査システム開発入門](https://www.udemy.com/course/codex-opencv/)」があります。
