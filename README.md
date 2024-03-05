# 音声文字起こしツール for whisper

<a href="https://colab.research.google.com/github/uzusio/whisper_tool.ipynb/blob/main/whisper_tool.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
---


## 概要
OpenAIの[whisper](https://github.com/openai/whisper)を使用した音声文字起こしツールです。
Google Colabの無料環境で利用可能です。

---


## 使い方

1.   編集->ノートブックの設定->ハードウェア アクセラレータ から「T4 GPU」を選択してください
2.   DIR_PATHに作業フォルダのパスを指定してください
    1.   Colabのデフォルトのディレクトリは`/content`です。
    2.   Driveをマウントして`/content/drive/MyDrive`以下からDrive上のディレクトリを指定できます
    3.   メディアファイルを左ペインのColab環境にドラッグドロップして使用することもできます
3.   初期設定を入力してください
    1.   DIR_PATH: 文字起こしをする音声ファイルを配置するディレクトリです。文字起こしされたテキストファイルも同ディレクトリに出力されます。
         1.    例: `/content`
    2.   INPUT_TYPE: `ファイルから読み込み`, `URLから読み込み`に対応しています
    2.   INPUT_FILE: `ファイルから読み込み`の場合、文字起こしするファイル名を記入してください。
         1.    例: `hogehoge.mp3`, `fugafuga.mkv`
    2.   INPUT_URL: `URLから読み込み`の場合、文字起こしするメディアのURLを記入してください。
    3.   MODEL_TYPE： 文字起こしの精度を選びます。「T4 GPU」でも動作しますので最高品質モデルの`large-v3`をお勧めします。
    4.   srt_output: 字幕ファイル生成に対応しました。出力ファイルを字幕ファイル形式にしたい場合はチェックを入れてください。
4.以降のセルを最後まで実行してください。ランタイム->以降のセルを実行でもOKです。

## リリースノート

### 2023.1.13
・マイクからの入力機能を追加

・Google翻訳とPapago翻訳を追加

・web上の動画をダウンロードする機能を追加

### 2024.3.5

・faster-whisperに切り替え

・Papagoの翻訳APIがNaver Cloudに移ったため一旦選択肢から消去

・マイク入力を削除

