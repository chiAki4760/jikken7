# 概要=退屈な簿記の仕訳勉強をゲーム感覚で学ぶアプリです。しかも、自分の好みの内容、テーマ、ストーリーで遊べます！  


#初めに＝リンクをタップするとブラウザーで開きますので、PCやスマホのホーム画面に追加し使用してください。  


#基本的な使い方＝画面上にある問題の解答を、問題下の解答欄に勘定科目と金額を入力し、その下にある「EXECUTEハッキング実行する」をクリックすると解答の正誤判定を解説が表示されます。次の問題、前の問題へ移動するときは、ボタンを押下、またはPCの矢印⇢←でも移動できます。仕訳が複数行となるときは解答行のすぐ下にある「*パラメータを追加」を押下すると仕訳入力行が新規に追加されます。  


#問題の追加/テーマの変更方法＝①下記のプロンプトをコピー。②お使いのAIの入力欄へペースト。③「希望の世界観」らんに、変更したい内容を具体的に入力し送信してコードを出力する。④出力されたコードをコピー。⑤アプリ画面下部にある「クラスター設定をインポートJSON」の▼部分をクリック。⑥開いた窓に、先ほどコピーしたコードをペーストし送信。これで新規設定になります。  
#元に戻すとき＝画面一番下「※プロトコルを初期化（ファクトリーリセット）」という部分を押下する。  


#新規問題＆テーマを変更する際には、お使いのAIにもよりますが、インタラクティブAI（対話形式）を活用しているとして設定しています。細かくあれこれ提案してみると案外全部希望の通りになることもありますので、試してみると良いと思います。（例：簿記のレベル：簿記3級レベル、簿記2級レベル、簿記3級~2級レベル、問題数を15問、20問にする、レベル１から５へストーリーでつなげる、押し活の熱意を込める、コレ界隈の人たちをうならせる世界観を構築する、など）  
#好きな小説や映画・コミックのストーリーの世界観で、簿記の仕訳問題を解いたり、青空文庫にある小説のストーリーで問題を作ってみる、なども飽きずに続けられると思います。ただし、個人での使用の場合での活用に限定し、著作権にはご注意ください。  


#退屈な仕訳問題をエンタメに！！

<!--ここからプロンプトです。コピーしてお使いくださいませ-->

以下の【骨格コード】をもとに、指定する【希望の世界観】に合わせたデザイン・演出にカスタマイズしたHTML完全版を出力してください。

【希望の世界観】
<!--この（ ）内に変更したいテーマ・世界観、問題数、問題レベルを記入する-->
（例：ネオンが光るサイバーパンク風 / レトロなゴシックホラー風 / ドット絵ファンタジー風 / パステル調のアイドル推し活風）

【カスタマイズしてほしい箇所】

1. CSSのカラーパレット（:root内の各変数）を世界観に合わせた配色に変更すること。

2. アプリ名（#app-title）、ロゴ絵文字（#app-logo）、判定ボタン（#submit-btn）の文言を世界観にマッチしたものに変えること（例: 「詠唱する」「打鍵する」「ハッキングする」など）。

3. 正解時に舞い上がる絵文字配列（RISING_EFFECT_SYMBOLS）を、世界観を象徴する絵文字に差し替えること。

4. HTMLの基本構造（入力フォームや判定ロジック、JSON読み込み機能）は壊さず維持すること。



【骨格コード】<!--この下は変更しないでください-->

<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ストーリー簿記ドリル // テンプレート</title>
  <style>
    * { box-sizing: border-box; }

    /* ==================================================

       ★ テーマカラー設定エリア

       ここを変えるだけで一括着せ替えできます

    ================================================== */
    :root {

      --primary: #2563eb;       /* メインカラー（決定ボタン・進捗など） */
      --primary-hover: #1d4ed8; /* ボタンホバー時の色 */
      --bg-body: #f8fafc;       /* 画面全体の背景色 */
      --card-bg: #ffffff;       /* カードの背景色 */
      --text-main: #0f172a;     /* 基本の文字色 */
      --text-muted: #64748b;    /* 補足・薄い文字色 */
      --border: #cbd5e1;        /* 枠線の色 */
      --debit-border: #3b82f6;  /* 借方枠のアクセントカラー */
      --credit-border: #ef4444; /* 貸方枠のアクセントカラー */
      --correct-bg: #dcfce7;    /* 正解時の背景色 */
      --correct-text: #166534;  /* 正解時の文字色 */
      --wrong-bg: #fee2e2;      /* 不正解時の背景色 */
      --wrong-text: #991b1b;    /* 不正解時の文字色 */

    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: -apple-system, BlinkMacSystemFont, "Hiragino Kaku Gothic ProN", "Yu Gothic", sans-serif;
      color: var(--text-main);
      background-color: var(--bg-body);
      padding: 16px;
      overflow-x: hidden;
    }
    .container {
      width: 100%;
      max-width: 680px;
      margin: 0 auto;
      background: var(--card-bg);
      border: 2px solid var(--border);
      border-radius: 16px;
      padding: 20px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
      position: relative;
    }
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-bottom: 12px;
      border-bottom: 1px solid var(--border);
      margin-bottom: 14px;
    }
    .logo-area { display: flex; align-items: center; gap: 10px; }
    .logo-icon { font-size: 1.8rem; line-height: 1; }
    .logo-title { margin: 0; font-size: 1.1rem; color: var(--primary); font-weight: 800; }
    .status-badge {
      background: var(--primary);
      color: white;
      padding: 4px 10px;
      border-radius: 999px;
      font-size: 0.72rem;
      font-weight: bold;
    }
    .status-badge.review { background: #f59e0b; color: #ffffff; }
    .stage-tabs {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 6px;
      margin-bottom: 14px;
    }
    @media (max-width: 480px) {
      .stage-tabs { grid-template-columns: repeat(3, 1fr); }
    }
    .stage-btn {
      padding: 8px 4px;
      border: 1px solid var(--border);
      border-radius: 8px;
      background: #ffffff;
      font-size: 0.72rem;
      font-weight: bold;
      color: var(--text-muted);
      cursor: pointer;
      text-align: center;
      line-height: 1.25;
      transition: all 0.15s ease;
    }
    .stage-btn.active {
      background: var(--primary);
      color: white;
      border-color: var(--primary);
      box-shadow: 0 2px 6px rgba(37, 99, 235, 0.3);
    }
    .quest-progress {
      margin-bottom: 16px;
      padding: 10px 14px;
      background: #f1f5f9;
      border-radius: 10px;
    }
    .progress-track {
      height: 8px;
      width: 100%;
      background: #e2e8f0;
      border-radius: 999px;
      overflow: hidden;
      margin-top: 6px;
    }
    .progress-fill {
      width: 0%;
      height: 100%;
      background: var(--primary);
      transition: width 0.3s ease;
    }
    .card {
      background: #ffffff;
      border: 1px solid var(--border);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 14px;
      box-shadow: 0 1px 3px rgba(0,0,0,0.02);
    }
    .question-label {
      display: inline-block;
      background: var(--primary);
      color: white;
      padding: 3px 8px;
      border-radius: 4px;
      font-size: 0.72rem;
      font-weight: bold;
      margin-bottom: 8px;
    }
    .story-text { margin: 0; font-size: 0.95rem; line-height: 1.65; }
    .split-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 12px;
      margin-bottom: 14px;
    }
    @media(max-width: 560px) { .split-container { grid-template-columns: 1fr; } }
    .side-column {
      padding: 12px;
      background: #f8fafc;
      border: 1.5px solid var(--debit-border);
      border-radius: 10px;
    }
    .side-column.credit { border-color: var(--credit-border); }
    .side-title { text-align: center; margin-bottom: 8px; font-weight: bold; font-size: 0.85rem; }
    .entry-row { display: flex; gap: 6px; margin-bottom: 8px; }
    .entry-row input {
      padding: 8px;
      border: 1px solid var(--border);
      border-radius: 6px;
      font-size: 0.9rem;
      background: #ffffff;
      color: var(--text-main);
      width: 100%;
    }
    .entry-row input[type="text"] { flex: 1.3; }
    .entry-row input[type="number"] { flex: 1; }
    .entry-row input:focus { outline: none; border-color: var(--primary); }
    .btn-remove {
      background: #fee2e2;
      border: 1px solid #fca5a5;
      border-radius: 6px;
      color: #b91c1c;


