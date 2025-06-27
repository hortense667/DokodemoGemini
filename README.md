# DokodemoGemini

This software allows you to call Gemini LLM from within any application.  
(c) 2025 Satoshi Endo  
https://x.com/hortense667
https://ascii.jp/serialarticles/1225476/

## Overview
This software allows you to call Gemini and input results in most text input scenes of Windows software. It is written using the snippet tools AutoHotKey and Python. Both have been compiled into executables, so you can start using them right away after setting up API keys and other configurations. Initially, the response was slow after the release, but by changing the model to "Gemini 2.5 flash lite," the speed is now comparable to DokodemoGPT.

## Usage Instructions

1. **Run DokodemoGeminiahk.exe**  
When you run it, an AutoHotKey "H" icon will appear in the tray. If it is already running, please exit it before executing again.

2. **How to Call Gemini**  
2-1. Select a range in the text input area of the software  
Select the portion you want to pass to Gemini in the editing screen of most applications like editors, Gmail, or Word.

2-2. Input the prompt  
Press `Win-Ctrl-o` to bring up the prompt input window, then enter your prompt.  
Examples: "Rewrite for readability," "Summarize," "Translate to English," "Check for typos and omissions," etc.  
* Adding "/w" at the end of prompts like "What kind of person?/w" will perform a web search and answer based on the first 1000 characters of the first three sites.  
You can also use the up and down arrow keys in the prompt input window to access previously entered prompts. You can use them as they are or edit them. Clicking the "v" on the right side of the input field will also display a list. Once you decide on your prompt, click "OK."

3. **Confirm Content**  
After a few seconds to several tens of seconds, a window will appear asking, "Is this okay?"  
- "Yes": The result will replace the original.  
- "No": No changes will be made.  
- "Cancel": The result will be input following the original text.

## Necessary Settings for Operation

1. **Set Environment Variables**  
- **Gemini API Key**  
  Obtain the Gemini API key and set the following environment variable:  
  `GEMINI_API_KEY`

2. **Unzip DokodemoGemini.zip**  
Download dokodemogemini.zip from the "Release" section of the DokodemoGemini repository.  
Extract it to an appropriate folder.  
Running DokodemoGeminiahk.exe in the extracted folder will enable you to use Gemini anywhere at any time.  
Please keep the "dist" folder and its contents in the same folder as DokodemoGeminiahk.exe.

3. **Register for Automatic Execution**  
Register a shortcut for DokodemoGpt02ahk.exe in the Windows startup menu.

## Shortcut Modification
1. Modify DokodemoGemniahk.ahk  
"^#g::" is the trigger for Ctrl-Win-g.  
Rewrite this, compile it from AutoHotKey Dash, and create a new DokodemoGeminiahk.exe.  
AutoHotKey Dash can be used after installing AutoHotKey.

## Using on Mac
1. **Prepare a Snippet Tool Other than AutoHotKey**  
Create a script that calls DokodemoGemini.py from that tool.  
Thus, a Python environment will be required.  
The prompt will be passed to DokodemoGemini.py via the clipboard from the snippet tool, and the results will be returned to the snippet tool again via the clipboard. Please refer to the source code for more details.

## 概要
Windowsのほとんどのソフトウェアのテキストを入力するシーンでGeminiを呼び出して結果を入力できるソフトウェアです。スニペットツールのAutoHotKeyとPythonを使って書かれています。どちらもexe化してあるので、APIキーなどの設定をすればすぐに使いはじめることができます。リリース直後はレスポンスが遅かったのですが、モデルを「Gemini 2.5 flash lite」に変更したことでDokodemoGPTに遜色ないスピードになりました。

## 使い方の手順

1. **DokodemoGeminiahk.exeの実行**  
実行するとトレイにAutoHotKeyの「H」アイコンが現れます。すでに実行中のときはそれを終了してから実行してください。

2. **Geminiの呼び出し方**  
2-1. ソフトウェアのテキスト入力エリアで範囲選択  
エディタやGmail、Wordなどほとんどのアプリの編集画面でGemini に渡したい部分を範囲選択してください。

2-2. プロンプトの入力  
`Win-Ctrl-o`を押すとプロンプト入力ウィンドウが現れるので、プロンプトを入力します。  
例：「読みやすく書き換えて」「要約して」「英訳して」「誤字・脱字をチェック」など 。
※「どんな人？/w」などと最後に「/w」をつけるとWeb検索して最初の3つのサイトの冒頭1000文字を参考に答えます。
またプロンプト入力ウィンドウでカーソル上下キーを押すことで過去に入力したプロンプトが出てきます。そのまま使ってもよいし編集してもよいです。入力欄の右側の「v」をクリックすることで一覧も表示されます。
プロンプトが決まったら「OK」をクリックします。
なお、過去のプロンプトの履歴は最大100件までDokodemoGPT02ahk.exeを実行したフォルダ上に「prompt_history.txt」というファイルに作成されます。

3. **内容確認**  
数秒から数十秒が経過すると「これでよいですか？」というウィンドウが表示されます。  
- 「はい」：結果に置き換えられる  
- 「いいえ」：変更なし  
- 「キャンセル」：元の文に続いて結果が入力されます。

## 動作のために必要な設定

1. **環境変数の設定**  
- **GeminiのAPIキー**  
  GeminiのAPIキーを取得し、以下の環境変数をセットしてください。  
  `GEMINI_API_KEY`

2. DokodemoGemini.zipの解凍
DokodemoGeminiのリポジトリの「リリース」からdokodemogemini.zipをダウンロード。
適切なフォルダに展開してください。
解答したフォルダの中にあるDokodemoGeminiahk.exeを実行するとどこでもGeminiがいつでも使える状態となります。
解凍ファイルのdistとフォルダとその中身は、DokodemoGeminiahk.exeのあるフォルダにそのまま置いてください。

3. **自動実行のための登録**  
WindowsのスタートアップメニューにDokodemoGpt02ahk.exeのショートカットを登録します。

## ショートカットの変更
1. DokodemoGemniahk.ahkの修正
「^#g::」は、Ctrl-Win-gでの起動です。
ここを書き換えて、AutoHotKey DashからコンバイルしてDokodemoGeminiahk.exeを新しくしてください。
AutoHotKey Dashは、AutoHotKeyをインストールことで使えるようになります。

## Macでの使用
1. **AutoHotKey以外のスニペットツールを用意**
そのツールからDokodemoGemini.pyを呼び出すようにスクリプトを作ってください。
したがって、Pythonの動作環境が必要となります。
スニペットツールからはプロンプトがDokodemoGemini.pyにクリップボードで渡され、DokodemoGemini.pyからはやはりクリップボード経由で結果がスニペットツールに戻されます。詳しくはソースコードをご覧ください。

