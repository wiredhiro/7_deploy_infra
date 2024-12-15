デプロイとインフラの基礎を学んでいこう！
ここでは、初心者向けに、簡単なNode.jsアプリをクラウド環境にデプロイする手順と、インフラの基礎をわかりやすく説明するね。

デプロイとインフラの基礎知識
	1.	デプロイ (Deployment)
	•	作成したアプリケーションを公開環境にアップロードして、誰でもアクセスできるようにすること。
	•	一般的なデプロイ先：
	•	Vercel/Heroku（簡単に利用できるクラウドサービス）
	•	AWS/GCP/Azure（柔軟性が高いが学習コストが少し高い）
	2.	インフラ (Infrastructure)
	•	アプリケーションを動かすための環境（サーバー、ネットワーク、ストレージなど）のこと。
	•	例: サーバーの設定、ロードバランサー、データベース接続など。

簡単なデプロイ方法: Renderを使う
    Render は初心者でも簡単に使えるクラウドサービスで、無料でNode.jsアプリをデプロイできるよ。

1. Renderのセットアップ
	1.	Renderに登録
	    •	Render公式サイト にアクセスしてアカウントを作成（GitHubアカウントで登録可能）。
	2.	GitHubリポジトリを準備
        •	作成したプロジェクトをGitHubにアップロードしておく。
        •	ターミナルで以下を実行：
            git init
            git add .
            git commit -m "initial commit"
            git branch -M main
            git remote add origin <GitHubリポジトリのURL>
            git push -u origin main
2. アプリをRenderにデプロイ
    1.	Renderにログインして、「New +」→「Web Service」を選択。
    2.	GitHubリポジトリを選択。
    3.	設定を入力：
        •	Branch: main
        •	Start Command: node index.js
        •	その他はデフォルトでOK。
    4.	「Create Web Service」をクリックすると、デプロイが始まる。
    5.	数分後、URLが表示されるので、ブラウザでアクセスして確認！
