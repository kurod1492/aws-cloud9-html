# AWS Cloud9 開発環境で HTML を作成する

## HTML ファイルの作成

Cloud9 のメニューバーの「File」をクリックすると「New File」という選択肢があるのでクリックします。
「Untitled1」というタブが開きます(数字は新規ファイルを開いている数によって変わる場合があります)。
サンプルとして、以下の HTML コードを記述します。

    <!DOCTYPE html>
    <html lang="ja">
        <head>
            <meta charset="UTF-8">
            <title>HTMLサンプル</title>
        </head>
        <body>
            <h1>HTMLサンプル</h1>
            <p>HTMLのサンプルです。</p>
        </body>
    </html>

記述できたら保存します。

メニューバーの File から Save をクリックします。
Filename という欄にファイル名を入力します。ここでは index.html とします。
保存場所を決めます。html-sample というフォルダを作って保存することにします。
Folder という欄に「/html-sample」と入力します。
Save をクリックします。
左側のディレクトリツリーに「html-sample」というディレクトリが追加され、
その中に index.html というファイルが作成されることを確認します。

## HTML のプレビュー

Cloud9 には、作成した HTML ファイルをプレビューする機能があります。
作成した index.html を開いている状態で、メニューバーの Preview から Preview index.html をクリックします。
そうすると、新しいタブが開いて、その中に index.html の内容が表示されます。

index.html の内容を更新したときは、index.html の内容が表示されているタブの左上に Refresh というボタンがあるのでそれをクリックします。

試しに、「<body>」 と 「<p>HTMLのサンプルです。</p>」 の間に「<h1>HTMLサンプル</h1>」という行を挿入して保存します。
Refresh をクリックすると index.html を表示内容が更新されます。

## CSS の作成

HTML にデザインを適用する場合、CSS を利用します。

CSS ファイルを作成します。

左側のディレクトリツリーの html-sample を右クリックして、New File をクリックします。

新しいファイルのアイコンが追加され、ファイル名が「Untitled」と表示されていますが変更できる状態になります。
ファイル名に「default.css」と入力してエンターキーを押します。

default.css をダブルクリックして開きます。

試しに p 要素の文字を青に変えてみます。default.css に以下の内容を記述します。

    p {color:blue;}

記述したら保存します。

index.html に default.css を参照する記述を追記します。

index.html を開き、<meta charset="UTF-8"> と <title>HTMLサンプル</title> の間に以下の行を挿入します。

    <link rel="stylesheet" type="text/css" href="default.css">

挿入したら保存します。
保存したら index.html を表示しているタブの Refresh をクリックします。
「HTMLのサンプルです。」の文字色が青に変わったらうまくいっています。
