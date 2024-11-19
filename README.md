<a href="https://colab.research.google.com/github/uzusio/whisper_tool.ipynb/blob/main/whisper_tool.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

# 音声文字起こしツール for whisper


---


## 概要
OpenAIの[whisper](https://github.com/openai/whisper)を使用した音声文字起こしツールです。Google Colabの無料環境で動作し、簡単な初期設定だけで高精度な文字起こしが可能です。


---


## 使い方

1.   編集->ノートブックの設定->ハードウェア アクセラレータ から「T4 GPU」を選択してください

2.   初期設定を入力してください
     - **INPUT_MEDIA_PATH**:  
       - `ファイルから読み込み`: 対象ファイルのパスを記入（例: `/content/hogehoge.mp3`）。  
       - `URLから読み込み`: 動画や音声のURLを記入（例: `http://example.com/video`）。  
     - **MODEL_TYPE**:  
       文字起こしの精度を指定します。高精度な`large-v3`を推奨。  
     - **srt_output**:  
       字幕ファイル（.srt形式）の生成を有効化したい場合にチェックを入れてください。

3. **セルを実行**
   - 初期設定を入力後、以降のセルを上から順に実行してください。または「ランタイム」→「以降のセルを実行」でまとめて実行可能です。

## リリースノート

### 2024.11.19
- UIを修正
- 一部ライブラリのバージョンを固定
- URLから動画をダウンロードできるように修正

### 2024.3.5
- Whisperを**faster-whisper**に切り替え、高速化。
- Papago翻訳APIの仕様変更に伴い一時的に選択肢から削除。
- マイク入力機能を削除。

### 2023.1.13
- マイクからの入力機能を追加。
- Google翻訳およびPapago翻訳を追加。
- Web上の動画をダウンロードする機能を追加。
