# 概要 
退屈な簿記の仕訳勉強をゲーム感覚で学ぶアプリです。しかも、自分の好みの内容、テーマ、ストーリーで遊べます！  


# 初めに
リンクをタップするとブラウザーで開きますので、PCやスマホのホーム画面に追加し使用してください。  


# 基本的な使い方
画面上にある問題の解答を、問題下の解答欄に勘定科目と金額を入力し、その下にある「EXECUTEハッキング実行する」をクリックすると解答の正誤判定を解説が表示されます。次の問題、前の問題へ移動するときは、ボタンを押下、またはPCの矢印⇢←でも移動できます。仕訳が複数行となるときは解答行のすぐ下にある「*パラメータを追加」を押下すると仕訳入力行が新規に追加されます。  


# 問題の追加、テーマの変更方法 
①下記のプロンプトをコピー。②お使いのAIの入力欄へペースト。③「希望の世界観」らんに、変更したい内容を具体的に入力し送信してコードを出力する。④出力されたコードをコピー。⑤アプリ画面下部にある「クラスター設定をインポートJSON」の▼部分をクリック。⑥開いた窓に、先ほどコピーしたコードをペーストし送信。これで新規設定になります。  
# 元に戻すとき
画面一番下「※プロトコルを初期化（ファクトリーリセット）」という部分を押下する。  


# 新規問題、テーマを変更する方法
お使いのAIにもよりますが、インタラクティブAI（対話形式）を活用しているとして設定しています。細かくあれこれ提案してみると案外全部希望の通りになることもありますので、試してみると良いと思います。（例：簿記のレベル：簿記3級レベル、簿記2級レベル、簿記3級~2級レベル、問題数を15問、20問にする、レベル１から５へストーリーでつなげる、押し活の熱意を込める、コレ界隈の人たちをうならせる世界観を構築する、など）  
# コツ
好きな小説や映画・コミックのストーリーの世界観で、簿記の仕訳問題を解いたり、青空文庫にある小説のストーリーで問題を作ってみる、なども飽きずに続けられると思います。ただし、個人での使用の場合での活用に限定し、著作権にはご注意ください。  


# 退屈な仕訳問題をエンタメに！！

## ここからはプロンプトです。コピーしてお使いくださいませ

以下の【骨格コード】をもとに、指定する【希望の世界観】に合わせたデザイン・演出にカスタマイズしたHTML完全版を出力してください。

【希望の世界観】
<!--この（ ）内に変更したいテーマ・世界観、問題数、問題レベルを記入する-->

（例：ネオンが光るサイバーパンク風 / レトロなゴシックホラー風 / ドット絵ファンタジー風 / パステル調のアイドル推し活風）

【カスタマイズしてほしい箇所】
1. CSSのカラーパレット（:root内の各変数）を世界観に合わせた配色に変更すること。
2. アプリ名（#app-title）、ロゴ絵文字（#app-logo）、判定ボタン（#submit-btn）の文言を世界観にマッチしたものに変えること（例: 「詠唱する」「打鍵する」「ハッキングする」など）。
3. 正解時に舞い上がる絵文字配列（RISING_EFFECT_SYMBOLS）を、世界観を象徴する絵文字に差し替えること。
4. HTMLの基本構造（入力フォームや判定ロジック、JSON読み込み機能）は壊さず維持すること。


【骨格コード】この下は変更しないでください


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

```html
!DOCTYPE html>
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

      cursor: pointer;

      font-weight: bold;

    }

    .btn-add {

      width: 100%;

      padding: 6px;

      background: #ffffff;

      border: 1px dashed var(--border);

      color: var(--text-muted);

      border-radius: 6px;

      font-size: 0.8rem;

      cursor: pointer;

      font-weight: bold;

    }

    .btn-submit {

      width: 100%;

      padding: 14px;

      background: var(--primary);

      color: white;

      border: none;

      border-radius: 10px;

      font-size: 1rem;

      font-weight: bold;

      cursor: pointer;

      box-shadow: 0 3px 8px rgba(37, 99, 235, 0.3);

      transition: background 0.15s ease;

    }

    .btn-submit:hover { background: var(--primary-hover); }



    .result-box {

      display: none;

      margin-top: 14px;

      padding: 14px;

      border-radius: 10px;

      font-size: 0.9rem;

      line-height: 1.6;

    }

    .result-box.correct { background: var(--correct-bg); border: 1px solid #86efac; color: var(--correct-text); }

    .result-box.wrong { background: var(--wrong-bg); border: 1px solid #fca5a5; color: var(--wrong-text); }

    

    .nav-buttons { display: flex; gap: 10px; margin-top: 14px; }

    .nav-btn {

      flex: 1;

      padding: 10px;

      background: #e2e8f0;

      color: var(--text-main);

      border: none;

      border-radius: 8px;

      font-weight: bold;

      cursor: pointer;

    }

    .clear-card { display: none; text-align: center; padding: 24px 16px; }

    .btn-review, .btn-restart {

      width: 100%;

      padding: 12px;

      border: none;

      border-radius: 8px;

      font-weight: bold;

      cursor: pointer;

      margin-bottom: 8px;

    }

    .btn-review { background: #f59e0b; color: white; }

    .btn-restart { background: #475569; color: white; }



    details {

      margin-top: 20px;

      border-top: 1px dashed var(--border);

      padding-top: 14px;

    }

    summary { cursor: pointer; font-size: 0.8rem; color: var(--text-muted); font-weight: bold; }

    textarea {

      width: 100%;

      height: 90px;

      margin-top: 10px;

      padding: 10px;

      border: 1px solid var(--border);

      border-radius: 8px;

      font-family: monospace;

      font-size: 0.8rem;

    }

    .load-btn {

      width: 100%;

      margin-top: 8px;

      padding: 10px;

      background: var(--primary);

      color: white;

      border: none;

      border-radius: 8px;

      font-weight: bold;

      cursor: pointer;

    }

    .reset-link {

      display: block;

      margin-top: 18px;

      text-align: center;

      font-size: 0.75rem;

      color: var(--text-muted);

      cursor: pointer;

      text-decoration: underline;

    }



    .shake-animation {

      animation: dmgShake 0.45s cubic-bezier(.36,.07,.19,.97) both;

    }

    @keyframes dmgShake {

      10%, 90% { transform: translate3d(-3px, 0, 0); }

      20%, 80% { transform: translate3d(5px, 0, 0); }

      30%, 50%, 70% { transform: translate3d(-7px, 0, 0); }

      40%, 60% { transform: translate3d(7px, 0, 0); }

    }



    .rising-item {

      position: fixed;

      bottom: -30px;

      z-index: 9999;

      pointer-events: none;

      user-select: none;

      opacity: 0;

      animation: riseMagic ease-out forwards;

    }

    @keyframes riseMagic {

      0% { transform: translateY(0) scale(0.4) rotate(0deg); opacity: 0; }

      15% { opacity: 0.95; }

      50% { transform: translateY(-50vh) translateX(var(--drift, 20px)) scale(1.1) rotate(180deg); opacity: 0.9; }

      85% { opacity: 0.7; }

      100% { transform: translateY(-110vh) translateX(calc(var(--drift, 20px) * -1)) scale(1.3) rotate(360deg); opacity: 0; }

    }

  </style>

</head>

<body>



<div class="container" id="mainContainer">

  <div class="header">

    <div class="logo-area">

      <div class="logo-icon" id="app-logo">📘</div>

      <div>

        <h1 class="logo-title" id="app-title">ストーリー簿記ドリル</h1>

        <div style="font-size:0.7rem; color:var(--text-muted);" id="sub-title">〜 基礎仕訳演習 〜</div>

      </div>

    </div>

    <span class="status-badge" id="status-tag">演習中</span>

  </div>



  <div class="stage-tabs">

    <button type="button" class="stage-btn active" id="tab-0" onclick="switchStage(0)">Stage 1</button>

    <button type="button" class="stage-btn" id="tab-1" onclick="switchStage(1)">Stage 2</button>

    <button type="button" class="stage-btn" id="tab-2" onclick="switchStage(2)">Stage 3</button>

    <button type="button" class="stage-btn" id="tab-3" onclick="switchStage(3)">Stage 4</button>

    <button type="button" class="stage-btn" id="tab-4" onclick="switchStage(4)">Stage 5</button>

  </div>



  <div class="quest-progress">

    <div style="display:flex; justify-content:space-between; font-size:0.75rem; font-weight:bold;">

      <span id="stage-badge-text">Stage 1</span>

      <span id="progress-text">第 1 問</span>

    </div>

    <div class="progress-track">

      <div class="progress-fill" id="progress-fill"></div>

    </div>

  </div>



  <div id="quiz-area">

    <div class="card">

      <div class="question-label" id="q-number">QUESTION // 01</div>

      <p class="story-text" id="story-display">読み込み中...</p>

    </div>



    <div class="split-container">

      <div class="side-column">

        <div class="side-title">借方 (Debit)</div>

        <div id="debit-rows"></div>

        <button type="button" class="btn-add" onclick="addRow('debit')">＋ 行を追加</button>

      </div>

      <div class="side-column credit">

        <div class="side-title">貸方 (Credit)</div>

        <div id="credit-rows"></div>

        <button type="button" class="btn-add" onclick="addRow('credit')">＋ 行を追加</button>

      </div>

    </div>



    <button type="button" class="btn-submit" id="submit-btn" onclick="checkAnswer()">仕訳を判定する</button>

    <div id="result-display" class="result-box"></div>



    <div class="nav-buttons">

      <button type="button" class="nav-btn" onclick="prevQuestion()">◀ 前へ</button>

      <button type="button" class="nav-btn" id="next-btn" onclick="nextQuestion()">次へ ▶</button>

    </div>

  </div>



  <div id="clear-area" class="clear-card">

    <h2 id="clear-heading">ステージクリア！</h2>

    <div id="complete-badge-area"></div>

    <p id="score-text" style="line-height:1.6; color:var(--text-muted);"></p>

    <div id="review-btn-area"></div>

    <button type="button" class="btn-restart" onclick="startFreshStage()">このステージを最初からやり直す</button>

  </div>



  <details>

    <summary>📥 追加問題データを取り込む (JSON)</summary>

    <textarea id="json-input" placeholder="AIで作成したJSON配列をここに貼り付けると、現在のステージを上書きできます"></textarea>

    <button type="button" class="load-btn" onclick="loadCustomData()">問題データを更新</button>

  </details>



  <span class="reset-link" onclick="forceReset()">※ データを初期化して元の問題に戻す</span>

</div>

<script>

// ==================================================

// ★ 演出絵文字設定エリア

// 配列内の文字をお好きな絵文字（例: 🔥, 💀, 🎀など）に変えられます

// ==================================================

const RISING_EFFECT_SYMBOLS = ["✨", "⭕", "🎉", "🌟", "💡", "📘"];



// ==================================================

// 内蔵初期問題データ（基礎問題 5ステージ構成）

// ==================================================

const STAGES = [

  {

    title: "Stage 1：商品売買と現金の基礎",

    questions: [

      {

        "story": "商品 100,000円を仕入れ、代金は現金で支払った。（仕入）（現金）",

        "debit": [{ "account": "仕入", "amount": 100000 }],

        "credit": [{ "account": "現金", "amount": 100000 }],

        "explanation": "費用（Expense）である「仕入」を借方に計上し、資産（Asset）である「現金」の減少を貸方に記入します。"

      },

      {

        "story": "商品 150,000円を売り上げ、代金は掛けとした。（売掛金）（売上）",

        "debit": [{ "account": "売掛金", "amount": 150000 }],

        "credit": [{ "account": "売上", "amount": 150000 }],

        "explanation": "資産（Asset）である債権「売掛金」を借方に計上し、収益（Revenue）である「売上」を貸方に記入します。"

      },

      {

        "story": "売掛金 150,000円が普通預金口座に振り込まれた。（普通預金）（売掛金）",

        "debit": [{ "account": "普通預金", "amount": 150000 }],

        "credit": [{ "account": "売掛金", "amount": 150000 }],

        "explanation": "資産（Asset）である「普通預金」の増加を借方に記入し、資産「売掛金」の消滅を貸方に記入します。"

      }

    ]

  },

  {

    title: "Stage 2：固定資産と付随費用",

    questions: [

      {

        "story": "事務用パソコン（備品）200,000円を購入し、設定費用 20,000円とともに代金は普通預金から支払った。（備品）（普通預金）",

        "debit": [{ "account": "備品", "amount": 220000 }],

        "credit": [{ "account": "普通預金", "amount": 220000 }],

        "explanation": "付随費用を取得原価に含めるため、資産（Asset）の「備品」220,000円を借方に計上します。"

      },

      {

        "story": "業務用の営業車両（車両運搬具）800,000円を購入し、納車費用 30,000円を加えた代金を当座預金口座から小切手を振り出して支払った。（車両運搬具）（当座預金）",

        "debit": [{ "account": "車両運搬具", "amount": 830000 }],

        "credit": [{ "account": "当座預金", "amount": 830000 }],

        "explanation": "付随費用を含めた「車両運搬具」830,000円を借方に計上し、小切手振出による「当座預金」の減少を貸方に記入します。"

      }

    ]

  },

  {

    title: "Stage 3：手付金と複合仕訳",

    questions: [

      {

        "story": "商品 300,000円を仕入れ、内金として支払っていた手付金 50,000円を充当し、残額は掛けとした。（仕入）（前払金）（買掛金）",

        "debit": [{ "account": "仕入", "amount": 300000 }],

        "credit": [{ "account": "前払金", "amount": 50000 }, { "account": "買掛金", "amount": 250000 }],

        "explanation": "費用（Expense）の「仕入」300,000円を借方に記入し、資産「前払金」50,000円と負債（Liability）「買掛金」250,000円を貸方に記入する複合仕訳です。"

      },

      {

        "story": "商品 400,000円を売り上げ、代金のうち 150,000円は現金で受け取り、残額は掛けとした。（現金）（売掛金）（売上）",

        "debit": [{ "account": "現金", "amount": 150000 }, { "account": "売掛金", "amount": 250000 }],

        "credit": [{ "account": "売上", "amount": 400000 }],

        "explanation": "収益（Revenue）の「売上」400,000円を貸方に計上し、資産（Asset）の「現金」150,000円と「売掛金」250,000円を借方に記入する複合仕訳です。"

      }

    ]

  },

  {

    title: "Stage 4：手形と資金調達",

    questions: [

      {

        "story": "銀行から 500,000円を借り入れ、当座預金口座に入金された。（当座預金）（借入金）",

        "debit": [{ "account": "当座預金", "amount": 500000 }],

        "credit": [{ "account": "借入金", "amount": 500000 }],

        "explanation": "資産（Asset）の「当座預金」増加を借方に記入し、負債（Liability）の「借入金」を貸方に計上します。"

      },

      {

        "story": "売掛金の回収として得意先振出の約束手形 200,000円を受け取った。（受取手形）（売掛金）",

        "debit": [{ "account": "受取手形", "amount": 200000 }],

        "credit": [{ "account": "売掛金", "amount": 200000 }],

        "explanation": "手形債権である資産（Asset）の「受取手形」を借方に計上し、資産「売掛金」の消滅を貸方に記入します。"

      }

    ]

  },

  {

    title: "Stage 5：決算と総合問題",

    questions: [

      {

        "story": "当期の建物に対する減価償却費 60,000円を直接法で計上した。（減価償却費）（建物）",

        "debit": [{ "account": "減価償却費", "amount": 60000 }],

        "credit": [{ "account": "建物", "amount": 60000 }],

        "explanation": "費用（Expense）である「減価償却費」を借方に計上し、資産「建物」を直接減額します。"

      },

      {

        "story": "期末の売掛金残高に対して 10,000円の貸倒引当金を計上した。（貸倒引当金繰入）（貸倒引当金）",

        "debit": [{ "account": "貸倒引当金繰入", "amount": 10000 }],

        "credit": [{ "account": "貸倒引当金", "amount": 10000 }],

        "explanation": "費用（Expense）の「貸倒引当金繰入」を借方に記入し、評価性引当金の「貸倒引当金」を貸方に計上します。"

      }

    ]

  }

];

// ==================================================

// アプリ共通ロジック

// ==================================================

let currentStageIndex = 0;

let currentQuestions = [];

let currentIndex = 0;

let correctCount = 0;

let wrongList = [];

let answeredSet = new Set();

let isReviewMode = false;



function init() {

  const savedStage = localStorage.getItem("boki_template_current_stage");

  currentStageIndex = savedStage ? parseInt(savedStage, 10) : 0;

  if (currentStageIndex < 0 || currentStageIndex >= STAGES.length) currentStageIndex = 0;

  loadStage(currentStageIndex);

}



function switchStage(stageIdx) {

  if (stageIdx === currentStageIndex && !isReviewMode) return;

  loadStage(stageIdx);

}



function loadStage(stageIdx) {

  currentStageIndex = stageIdx;

  localStorage.setItem("boki_template_current_stage", currentStageIndex);



  for (let i = 0; i < STAGES.length; i++) {

    const btn = document.getElementById(`tab-${i}`);

    if (btn) {

      if (i === stageIdx) btn.classList.add("active");

      else btn.classList.remove("active");

    }

  }



  const stageObj = STAGES[stageIdx];

  document.getElementById("stage-badge-text").textContent = stageObj.title;

  document.getElementById("sub-title").textContent = `〜 ${stageObj.title} 〜`;



  const keyPrefix = `boki_template_st${stageIdx}_`;

  let stageData = stageObj.questions;

  try {

    const customData = localStorage.getItem(`${keyPrefix}data`);

    if (customData) {

      const parsed = JSON.parse(customData);

      if (Array.isArray(parsed) && parsed.length > 0) stageData = parsed;

    }

  } catch(e) {}



  currentQuestions = [...stageData];

  currentIndex = 0;

  correctCount = 0;

  wrongList = [];

  isReviewMode = false;

  answeredSet.clear();



  document.getElementById("quiz-area").style.display = "block";

  document.getElementById("clear-area").style.display = "none";

  loadQuestion(0);

}



function createRowHTML(account = "", amount = "") {

  const div = document.createElement("div");

  div.className = "entry-row";

  div.innerHTML = `

    <input type="text" placeholder="科目" value="${account}">

    <input type="number" placeholder="金額" value="${amount}">

    <button type="button" class="btn-remove" onclick="removeRow(this)">✕</button>

  `;

  return div;

}



function addRow(side) {

  const container = document.getElementById(`${side}-rows`);

  if (container) container.appendChild(createRowHTML());

}



function removeRow(btn) {

  const row = btn.closest(".entry-row");

  if (row && row.parentElement && row.parentElement.children.length > 1) {

    row.remove();

  } else {

    alert("最低1行は必要です。");

  }

}



function loadQuestion(index) {

  if (!currentQuestions || currentQuestions.length === 0) return;

  if (index < 0 || index >= currentQuestions.length) index = 0;

  currentIndex = index;



  const tag = document.getElementById("status-tag");

  if (isReviewMode) {

    tag.textContent = "復習モード";

    tag.className = "status-badge review";

  } else {

    tag.textContent = "演習中";

    tag.className = "status-badge";

  }



  const prefix = isReviewMode ? "復習" : `Stage ${currentStageIndex + 1}`;

  document.getElementById("q-number").textContent = `${prefix} // ${index + 1} / ${currentQuestions.length}`;

  document.getElementById("story-display").textContent = currentQuestions[index].story;



  document.getElementById("debit-rows").innerHTML = "";

  document.getElementById("credit-rows").innerHTML = "";

  addRow("debit");

  addRow("credit");



  const res = document.getElementById("result-display");

  res.style.display = "none";

  res.className = "result-box";

  document.getElementById("submit-btn").style.display = "block";



  const nextBtn = document.getElementById("next-btn");

  nextBtn.textContent = (currentIndex === currentQuestions.length - 1) ? "結果を見る" : "次へ ▶";



  const percent = Math.round(((index + 1) / currentQuestions.length) * 100);

  document.getElementById("progress-fill").style.width = percent + "%";

  document.getElementById("progress-text").textContent = `${index + 1} / ${currentQuestions.length} 問 (${percent}%)`;

}



function getEntries(side) {

  const container = document.getElementById(`${side}-rows`);

  if (!container) return [];

  const rows = container.children;

  const entries = [];

  for (let row of rows) {

    const inputs = row.querySelectorAll("input");

    if (inputs.length >= 2) {

      const account = inputs[0].value.trim();

      const amount = parseInt(inputs[1].value, 10);

      if (account && !isNaN(amount)) entries.push({ account, amount });

    }

  }

  return entries;

}



function spawnRisingMagic() {

  const totalItems = 25;

  for (let i = 0; i < totalItems; i++) {

    const item = document.createElement("div");

    item.className = "rising-item";

    item.textContent = RISING_EFFECT_SYMBOLS[Math.floor(Math.random() * RISING_EFFECT_SYMBOLS.length)];

    item.style.left = (Math.random() * 92 + 4) + "vw";

    

    const driftX = (Math.random() * 80 - 40) + "px";

    item.style.setProperty("--drift", driftX);



    const size = Math.random() * 16 + 20;

    const duration = Math.random() * 1.5 + 2.0;

    const delay = Math.random() * 0.4;



    item.style.fontSize = size + "px";

    item.style.animationDuration = duration + "s";

    item.style.animationDelay = delay + "s";



    document.body.appendChild(item);

    setTimeout(() => { item.remove(); }, (duration + delay) * 1000);

  }

}



function triggerShake() {

  const container = document.getElementById("mainContainer");

  container.classList.remove("shake-animation");

  void container.offsetWidth;

  container.classList.add("shake-animation");

  setTimeout(() => { container.classList.remove("shake-animation"); }, 500);

}



function checkAnswer() {

  const q = currentQuestions[currentIndex];

  const userDebit = getEntries("debit");

  const userCredit = getEntries("credit");



  const normalize = d => Array.isArray(d) ? d : [d];

  const cDebit = normalize(q.debit);

  const cCredit = normalize(q.credit);



  const matchSide = (u, c) => {

    if (u.length !== c.length) return false;

    const sU = [...u].sort((a,b) => a.account.localeCompare(b.account) || a.amount - b.amount);

    const sC = [...c].sort((a,b) => a.account.localeCompare(b.account) || a.amount - b.amount);

    return sU.every((v, i) => v.account === sC[i].account && v.amount === sC[i].amount);

  };



  const isOk = matchSide(userDebit, cDebit) && matchSide(userCredit, cCredit);

  const res = document.getElementById("result-display");

  res.style.display = "block";



  if (isOk) {

    spawnRisingMagic();

    res.className = "result-box correct";

    res.innerHTML = `<strong>正解！</strong><br>${q.explanation}`;

    if (!answeredSet.has(currentIndex)) {

      correctCount++;

      if (isReviewMode) wrongList = wrongList.filter(item => item.story !== q.story);

      answeredSet.add(currentIndex);

    }

  } else {

    triggerShake();

    res.className = "result-box wrong";

    const dStr = cDebit.map(d => `(${d.account}: ${d.amount.toLocaleString()}円)`).join(" ");

    const cStr = cCredit.map(c => `(${c.account}: ${c.amount.toLocaleString()}円)`).join(" ");

    res.innerHTML = `<strong>不正解</strong><br>正解 借方: ${dStr}<br>正解 貸方: ${cStr}<br><br>${q.explanation}`;

    if (!answeredSet.has(currentIndex)) {

      if (!wrongList.some(item => item.story === q.story)) wrongList.push(q);

      answeredSet.add(currentIndex);

    }

  }

}



function prevQuestion() { if (currentIndex > 0) loadQuestion(currentIndex - 1); }

function nextQuestion() {

  if (currentIndex < currentQuestions.length - 1) loadQuestion(currentIndex + 1);

  else showClearScreen();

}



function showClearScreen() {

  document.getElementById("quiz-area").style.display = "none";

  const clearArea = document.getElementById("clear-area");

  clearArea.style.display = "block";



  const total = currentQuestions.length;

  const badgeArea = document.getElementById("complete-badge-area");

  const scoreText = document.getElementById("score-text");

  const revArea = document.getElementById("review-btn-area");



  badgeArea.innerHTML = "";

  revArea.innerHTML = "";



  if (wrongList.length === 0) {

    spawnRisingMagic();

    badgeArea.innerHTML = `<div style="display:inline-block; padding:6px 14px; background:#dcfce7; border:1px solid #86efac; border-radius:6px; font-weight:bold; color:#166534; margin-bottom:12px;">全問正解達成！</div>`;

    scoreText.innerHTML = `おめでとうございます！全問正解です。(${total}/${total})`;

  } else {

    scoreText.innerHTML = `${total} 問中 ${correctCount} 問 正解。<br>間違えた問題が ${wrongList.length} 問 あります。`;

    const btn = document.createElement("button");

    btn.className = "btn-review";

    btn.textContent = `間違えた問題だけ復習する (${wrongList.length}問)`;

    btn.onclick = () => {

      isReviewMode = true;

      currentQuestions = [...wrongList];

      currentIndex = 0;

      correctCount = 0;

      answeredSet.clear();

      document.getElementById("quiz-area").style.display = "block";

      clearArea.style.display = "none";

      loadQuestion(0);

    };

    revArea.appendChild(btn);

  }

}



function startFreshStage() {

  loadStage(currentStageIndex);

}



function forceReset() {

  if (confirm("入力したカスタムデータを初期化し、初期状態に戻しますか？")) {

    localStorage.clear();

    location.reload();

  }

}



function loadCustomData() {

  const input = document.getElementById("json-input").value.trim();

  if (!input) {

    alert("JSONデータを入力してください。");

    return;

  }

  try {

    const data = JSON.parse(input);

    if (!Array.isArray(data) || data.length === 0) throw new Error();



    STAGES[currentStageIndex].questions = data;

    localStorage.setItem(`boki_template_st${currentStageIndex}_data`, JSON.stringify(data));

    loadStage(currentStageIndex);

    alert(`Stage ${currentStageIndex + 1} の問題（全${data.length}問）を更新しました！`);

  } catch (e) {

    alert("⚠️ JSONの形式を確認してください。正しく貼り付けられているかチェックをお願いします。");

  }

}



window.addEventListener("DOMContentLoaded", init);

</script>

</body>

</html>
```
