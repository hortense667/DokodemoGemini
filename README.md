# DokodemoGemini

This software allows you to call Gemini LLM from within any application.  
(c) 2025 Satoshi Endo  
https://x.com/hortense667
https://ascii.jp/serialarticles/1225476/

## 説明

1. **DokodemoGemini**  
DokodemoGPT02のGemini版です。GeminiのAPIは無料枠があるのでその範囲内であれば無料で使えます。リリース直後はレスポンスが遅かったのですが、モデルを「Gemini 2.5 flash lite」に変更したことでDokodemoGPTに遜色ないスピードになりました。

2. **環境変数の設定**  
- **GeminiのAPIキー**  
  GeminiのAPIキーを取得し、以下の環境変数をセットしてください。  
  `GEMINI_API_KEY`

3. DokodemoGemini.zipの解凍
DokodemoGeminiのリポジトリの「リリース」からdokodemogemini.zipをダウンロード。
適切なフォルダに展開してください。
DokodemoGeminiahk.exeを実行するとどこでもGeminiがいつでも使える状態となります。
解凍ファイルのdistとフォルダとその中身は、DokodemoGeminiahk.exeのあるフォルダにそのまま置いてください。

## 使い方の手順

1. **DokodemoGeminiahk.exeの実行**  
実行するとトレイにAutoHotKeyの「H」アイコンが現れます。

2. **LLMの召喚の仕方**  
2-1. アプリで範囲選択  
エディタやGmail、Wordなどほとんどのアプリの編集画面で利用可能です。  
LLMで処理したいテキストを範囲選択してください。

2-2. プロンプトの入力  
`Win-Ctrl-o`を押すとプロンプト入力ウィンドウが現れるので、プロンプトを入力します。  
例：「読みやすく書き換えて」「要約して」「英訳して」「誤字・脱字をチェック」など 。
※「どんな人？/w」などと最後に「/w」をつけるとWeb検索して最初の3つのサイトの冒頭1000文字を参考に答えます（テスト中）。
※長いプロンプトを与える場合は姉妹ソフトDokodemoPromptがあります。

3. **内容確認**  
「これでよいですか？」というウィンドウが表示されます。  
- 「はい」：結果に置き換えられる  
- 「いいえ」：変更なし  
- 「キャンセル」：元の文に続いて結果を入力

## Macでの使用
1. **AutoHotKey以外のスニペットツールを用意**
そのツールからDokodemoGemini.pyを呼び出すように設定すればよい。
したがって、Pythonの動作環境が必要となります。
スニペットツールからはプロンプトがDokodemoGemini.pyにクリップボードで渡され、DokodemoGemini.pyからはやはりクリップボード経由で結果がスニペットツールに戻されるだけである。
2. **専用のPythonコードの提供**
容易にMacで使うためのMac版DokodemoLLMを提供することにしました。若干使い勝手が変わる可能性がありますが近々提供予定です。


