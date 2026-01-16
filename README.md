# 中野第二自治会 ホームページ

## 📋 概要

中野第二自治会の公式ホームページです。地域の防災情報を中心に、住民の皆様に役立つ情報を発信しています。

## 🎯 特徴

- **高齢者に優しいデザイン**: 大きな文字(18px以上)、高コントラスト、シンプルなレイアウト
- **完全日本語対応**: すべてのコンテンツが日本語
- **レスポンシブデザイン**: スマートフォンでも見やすい
- **素人でも更新可能**: HTMLの基本編集だけで更新できる

## 📂 ファイル構成

```
nakano-jichikai-website/
├── index.html          # トップページ
├── bousai.html         # 防災情報ページ
├── download.html       # 資料ダウンロードページ
├── links.html          # 外部リンク集
├── news.html           # お知らせページ
├── contact.html        # お問い合わせページ
├── css/
│   └── style.css       # スタイルシート
└── README.md           # このファイル
```

## 🚀 使い方

### 1. サイトの公開

#### 方法A: 無料ホスティングサービスを使う(推奨)

**GitHub Pages (完全無料)**
1. GitHubアカウントを作成: https://github.com
2. 新しいリポジトリを作成
3. すべてのファイルをアップロード
4. Settings → Pages → Sourceを「main branch」に設定
5. 数分でサイトが公開されます

**Netlify (完全無料)**
1. Netlifyアカウントを作成: https://www.netlify.com
2. 「New site from Git」またはドラッグ&ドロップでアップロード
3. 自動的にサイトが公開されます

#### 方法B: レンタルサーバーを使う

1. レンタルサーバーを契約(さくら、ロリポップなど)
2. FTPソフト(FileZilla)でファイルをアップロード
3. サーバーのURLにアクセスして確認

### 2. 連絡先情報の更新

すべてのページのフッター部分とcontact.htmlページで、以下の情報を実際のものに変更してください:

```html
<!-- 変更が必要な箇所 -->
〒164-0001
東京都中野区○○町○-○-○  ← 実際の住所
TEL: 03-XXXX-XXXX          ← 実際の電話番号
Email: info@nakano2-jichikai.example.com  ← 実際のメールアドレス
```

### 3. お知らせの更新方法

**手順:**

1. `news.html`をテキストエディタで開く
2. 既存の記事をコピー
3. 日付、タイトル、本文を変更
4. 新しい記事を一番上に配置
5. 保存してサーバーにアップロード

**記事のテンプレート:**

```html
<article class="news-article">
    <div class="news-header">
        <span class="news-badge new">新着</span>
        <span class="news-date">2026年X月X日</span>
    </div>
    <h2>記事のタイトル</h2>
    <div class="news-content">
        <p>記事の本文をここに書きます。</p>
    </div>
</article>
```

### 4. 防災資料のアップロード方法

#### 方法1: Google Drive を使う(最も簡単)

1. **Google Driveにアクセス**: https://drive.google.com
2. **資料をアップロード**: PDFファイルをドラッグ&ドロップ
3. **共有リンクを取得**:
   - ファイルを右クリック → 「共有」
   - 「リンクを知っている全員」に変更
   - 「リンクをコピー」
4. **HTMLを編集**:

```html
<!-- download.html の該当箇所を編集 -->
<a href="https://drive.google.com/file/d/YOUR-FILE-ID/view" 
   class="btn btn-primary" target="_blank">
    ダウンロード(PDF)
</a>
```

#### 方法2: サーバーに直接アップロード

1. `downloads`フォルダを作成
2. PDFファイルをアップロード
3. HTMLのリンクを変更:

```html
<a href="downloads/bousai_manual.pdf" 
   class="btn btn-primary" download>
    ダウンロード(PDF)
</a>
```

### 5. お問い合わせフォームの設定

静的HTMLではフォームが機能しません。以下のいずれかの方法で対応してください:

#### 方法A: Googleフォームを使う(推奨)

1. https://forms.google.com でフォームを作成
2. 質問を追加(お名前、メール、お問い合わせ内容など)
3. 「送信」→ 埋め込みコード(< >アイコン)をクリック
4. HTMLコードをコピー
5. `contact.html`の`<form>`タグ全体を、コピーしたコードで置き換え

#### 方法B: メールリンクを使う(簡易版)

フォームを削除して、代わりに大きなメールボタンを配置:

```html
<div class="button-center">
    <a href="mailto:info@nakano2-jichikai.example.com" 
       class="btn btn-primary btn-large">
        メールで問い合わせ
    </a>
</div>
```

### 6. Googleマップの埋め込み

1. Google Mapsで場所を検索
2. 「共有」→「地図を埋め込む」
3. HTMLコードをコピー
4. `contact.html`の地図プレースホルダー部分に貼り付け

```html
<iframe 
    src="https://www.google.com/maps/embed?pb=..." 
    width="100%" 
    height="450" 
    style="border:0;" 
    allowfullscreen="" 
    loading="lazy">
</iframe>
```

## 🛠️ カスタマイズ

### 色の変更

`css/style.css`を編集:

```css
/* メインカラー */
background: linear-gradient(135deg, #4a90e2 0%, #357abd 100%);
/* 上記の #4a90e2 と #357abd を好みの色に変更 */
```

### フォントサイズの変更

```css
body {
    font-size: 18px;  /* この数値を変更 */
}
```

## 📱 推奨ツール

### テキストエディタ
- **Visual Studio Code** (無料): https://code.visualstudio.com/
- **Notepad++** (無料): https://notepad-plus-plus.org/

### FTPクライアント
- **FileZilla** (無料): https://filezilla-project.org/

### 画像編集
- **Canva** (無料): https://www.canva.com/
- **GIMP** (無料): https://www.gimp.org/

## 🔄 月次更新チェックリスト

- [ ] お知らせページに新しい情報を追加
- [ ] 古いお知らせから「新着」バッジを削除
- [ ] トップページの「最新のお知らせ」を更新
- [ ] 連絡先情報に変更がないか確認
- [ ] リンク切れがないかチェック

## 💡 ヒント

### 定期更新のコツ

- **月に1回**: お知らせページを更新
- **四半期に1回**: 防災情報を見直し
- **年に1回**: 防災マニュアルを更新
- **随時**: リンク切れをチェック

### バックアップ

定期的にすべてのファイルをバックアップしてください。

### セキュリティ

- メールアドレスや電話番号は必要最小限に
- 個人情報は掲載しない
- 定期的にサイトの状態を確認

## ❓ よくある質問

**Q: HTMLを編集するのが難しいです**
A: Visual Studio Codeなどのエディタを使うと、色分け表示されて編集しやすくなります。

**Q: 画像を追加したいのですが?**
A: `images`フォルダを作成し、画像をアップロード後、以下のように記述します:
```html
<img src="images/photo.jpg" alt="説明文">
```

**Q: 独自ドメインは取得できますか?**
A: はい。お名前.comなどのドメイン取得サービスで購入できます(年間1,000円程度)。

**Q: スマホで見ると表示が崩れます**
A: レスポンシブデザインに対応していますが、ブラウザのキャッシュを削除してみてください。

## 📞 サポート

このウェブサイトに関するご質問は、自治会の担当者までお問い合わせください。

---

## 📄 ライセンス

このウェブサイトは中野第二自治会が管理しています。

**制作日**: 2026年1月16日  
**最終更新**: 2026年1月16日

---

**中野第二自治会**  
地域の安全・安心を守ります 🏘️