# GitHub Pagesで個人Webサイトを作る
* 青森大学ソフトウェア情報学部教員向けハンズオン

---

## 概要

### GitHub Pagesとは
* Git
    - <https://git-scm.com/>
    - 分散バージョン管理システム
    - リポジトリ(保管庫)を作り、そこに指定した瞬間のファイルの内容をコミット(収納)し、記録していく
* GitHub
    - <https://github.com/>
    - インターネット上にリポジトリを作り、公開できるサービス
    - さまざまなソフトの公開に利用されている
    - 1ファイルのサイズの上限は100MB。50MBを越えると警告が出る
* GitHub Pages
    - <https://pages.github.com/>
    - GitHubのリポジトリの内容を、Webページとして公開できるサービス

### 今回の講習
* GitHub Pagesを、Webインターフェイスから使用して、個人のWebサイトを公開

### GitHub Pages利用の流れ
1. はじめて使うときに、リポジトリ(保管庫)を作る
2. 必要に応じて、リポジトリの中にフォルダを作る
3. ファイルを作る/編集する/削除する
4. リポジトリにコミット(収納)して、公開する

---

## 事前準備: GitHubにアカウントを作る

### 1. GitHubにアクセスする
* ブラウザで<https://github.com/>へ

### 2. ユーザー登録へすすむ
* [Sign up for GitHub]をクリックする

### 3. アカウント情報を入力する
* 以下の情報を入力
    - Username  
      WebサイトのURLが「https://ユーザー名.github.io/」になりますので、適切に選んでください。  
      また、GitHubに既に存在しているユーザー名は使用できません。
    - Email Address
    - Password
* [Create an account]をクリック

### 4. 料金プランを選択する
* [Unlimited public repositories for free.]を選択
* [Continue]をクリック

### 5. 経歴を設定する
* How would you describe your level of programming experience?  
  例: [Very experienced]
* What do you plan to use GitHub for?  
  例: [School projects], [Research]
* Which is closest to how you would descibe yourself?  
  例: [I'm a professional]
* What are you interested in?  
  例: Computer Science
* [Submit]をクリック

### 6. メール・アドレスを検証して、登録を完了させる
* [Start a project]をクリックして、プロジェクトをはじめてみようとする
* 「Please verify your email address」と言われる
* メールを確認し、メールの中のリンク「Verify email address」をクリックする
* 登録が完了する

---

## ハンズオン: GitHubページで個人のWebサイトを公開する

### 1. GitHubへアクセスする
* ブラウザでGitHubにアクセスする  
  <https://github.com/>
* サインインしていなければ、サインインする

### 2. リポジトリを作る
* はじめて使うときに行う
* [Start a project]をクリック
    - [Start a project]が表示されていなければ、画面右上の「+」をクリックし「New repository」を選択
* 必要項目を記入
    - [Repository name]に「ユーザー名.github.io」  
      個人のGitHub Pagesを作る場合にこのように設定
    - [Public/Private]は「Public」を選択
* [Create repository]をクリック

### 3. ファイル操作のユーザー・インターフェイスを表示させる
* 何もファイルがないと、インストラクションが表示され、ファイル操作のユーザー・インターフェイスが表示されない
* そこで、とりあえず「README」を作る
    - 「We recommend every repository include a REAMDE, LICENSE, and .gitignore」の[README]の部分をクリック
* ファイルの内容を作成する(実際にはしない)
    - 「README」ファイルの内容を編集できるが、何もしないで、スクロールしてページ下部へ
* ファイルを保存する
    - ページ下部の[Commit new file]の欄に「Create README.md」と記入
    - [Commit new file]をクリック
* ファイル操作のユーザー・インターフェイスが表示される

### 4. HTMLを作る
* [Create new file]をクリック
* ファイルの内容を作成する
    - ファイル名に「index.html」
    - [Edit new file]に以下のようなHTMLを書き込む

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <title>青森太郎のページ</title>
  </head>
  <body>
    <h1>青森太郎のページ</h1>
  </body>
</html>
```

* ファイルを保存する
    - ページ下部の[Commit new file]の欄に「Create index.html」と記入
    -  [Commit new file]をクリック

### 5. 公開されたページの確認
* 画面上部のタブの右端の[Settings]を選択
* [Options]の中の[GitHub Pages]を見ると「Your site is published at https://ユーザー名.github.io/」と表示されている
* ブラウザで「https://ユーザー名.github.io/」にアクセス

### 6. cssフォルダを作成
* フォルダとファイルを作る
    - フォルダには何かしらファイルが必要なので
    - [Create new file]をクリック
    - ファイル名の欄に「css/」と入力するとフォルダが作成され、さらに続けて「README.md」と入力してファイルを作る
* ファイルの内容を作成する(実際にはしない)
    - 「README」ファイルの内容を編集できるが、何もしないで、スクロールしてページ下部へ
* ファイルを保存する
    - ページ下部の[Commit new file]の欄に「Create css/README.md」と記入
    - [Commit new file]をクリック

### 7. cssフォルダにCSSをアップロード
* ファイルを用意  
  以下のようなファイルを「styles.css」という名前で、エンコーディングはUTF-8

```CSS
@charset "UTF-8";

h1 {
  font-size: 32px;
  font-weight: bold;
  color: #666;
}
```

* 作業フォルダの確認
    - 「ユーザー名 / ユーザー名.github.io/」リポジトリの「ユーザー名.github.io/css/」フォルダにいることを確認
* ファイルをアップロードする
    -  [Upload files]をクリック
    - 「Drag files here to add them to your repository Or choose your files」にファイルをドラッグ&ドロップするか、[choose your files]をクリックしてファイルを選択する
* ファイルを保存する
    - ページ下部の[Commit changes]の欄に「Add css/styles.css via upload」と記入
    - [Commit changes]をクリック
* ブラウザで「https://ユーザー名.github.io/css/styles.css」を確認

### 8. WebインターフェイスからHTMLを編集
* 作業フォルダの変更
    - 「ユーザー名 / ユーザー名.github.io」リポジトリのトップのフォルダに戻る
* 「index.html」をクリック
* ファイルの中身が表示されている部分の右上の鉛筆のアイコンをクリック
* ファイルの内容を編集する

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <link rel="stylesheet" href="/css/styles.css">
    <title>青森太郎のページ</title>
  </head>
  <body>
    <h1>青森太郎のページ</h1>
  </body>
</html>
```

* ファイルを保存する
    - ページ下部の[Commit changes]の欄に「Update index.html」、詳細を記入する欄に「Add link to css/styles.css」と記入
    - [Commit changes]をクリック
* ブラウザで「https://ユーザー名.github.io/」を確認

### 9. アップロードしてHTMLを更新
* 最初にアップロードするファイルを作る
* 作業フォルダの確認
    - 「ユーザー名 / ユーザー名.github.io」リポジトリのトップのフォルダにいることを確認
* 「index.html」をクリック
* ファイルの中身が表示されている部分の右上の[Raw」をクリック
* 表示内容をコピーし、編集して、ローカルにファイルを作る  
  具体的には、表示内容をローカルのエディタにペーストする  
  そして、下記のように編集する  
  それを「index.html」という名前で、エンコーディングをUTF-8にして、ファイルに保存する

```HTML
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1">
    <link rel="stylesheet" href="/css/styles.css">
    <title>青森太郎のページ</title>
  </head>
  <body>
    <h1>青森太郎のページ</h1>
    <p>ここは青森太郎のページです。</p>
  </body>
</html>
```

* 作ったファイルをアップロードする
* 作業フォルダの変更
    - 「ユーザー名 / ユーザー名.github.io」リポジトリのトップのフォルダに戻る
* ファイルをアップロードする
    - [Upload files]をクリック
    - 「Drag files here to add them to your repository Or choose your files」にファイルをドラッグ&ドロップするか、「choose your files」をクリックしてファイルを選択する
* ファイルを保存する
    - ページ下部の[Commit changes]の欄に「Update index.html via upload」と記入
    - [Commit changes]をクリック
* ブラウザで「https://ユーザー名.github.io/」を確認

### おわりに
* ファイルは、Webインターフェイスから作成/更新/削除できる
    - アップロードして、作成/更新することもできる
    - 注: ファイルはコミットしないと保存されない(アップロードしたファイルも)
* フォルダには、何らかのファイルを置いておくとよい
    - README.mdなど
* Gitを使うと、より柔軟な操作が可能
    - バージョン管理システムのフル機能が使える
    - 最近のUNIXには付属
    - WindowsやMacではSourceTreeというGUIクライアントが便利

