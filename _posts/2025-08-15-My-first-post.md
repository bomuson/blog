---
layout: post
title: "GitHubでブログを始める手順"
date: 2025-08-15
---

# はじめに

ブログをやるにあたって、GitHubを使えば無料でできるということはかなり前から知っていました。ついにそれを実現できる日が来ました。

基本的にはChatGPTが使えるようになったから、かなり取り組みやすくなったというのがあります。
以下、私が実際にできるようになったChatGPT案内文です。

---
GitHubを使ってブログを運営する場合、代表的な方法は **GitHub Pages + 静的サイトジェネレーター** を組み合わせるやり方です。手順を段階的に整理して説明します。

---

## **ステップ1：GitHubアカウント作成**

1. [GitHub公式サイト](https://github.com/)にアクセス
    
2. 「Sign up」でアカウント作成
    
3. ユーザー名・メールアドレス・パスワードを設定
    
4. プランは無料プランでOK
    

> ⚡ 補足：GitHub Pagesは無料で使えます

---

## **ステップ2：リポジトリ作成**

1. GitHubにログイン後、「New repository」をクリック
    
2. リポジトリ名を決める
    
    - 例：`my-blog`
        
    - **注意**：ユーザー名.github.io にするとユーザーサイトとして公開されます
        
3. 「Public」にチェック（無料で公開する場合）
    
4. 「Add a README」にチェック（初期ファイル作成用）
    
5. 「Create repository」をクリック
    

---

## **ステップ3：静的サイトジェネレーターの選定**

ブログをGitHub Pagesで運営するには、HTMLを手書きするより **静的サイトジェネレーター（SSG）** が便利です。  
代表的なもの：

- **Jekyll**（GitHub公式サポート）
    
- **Hugo**（高速・多機能）
    
- **Gatsby**（Reactベース）
    

> 初心者には **Jekyll** が最も簡単です。

---

## **ステップ4：ローカル環境準備**

1. **Git** をインストール（[公式サイト](https://git-scm.com/)）
    
2. **Ruby**（Jekyllの場合）をインストール
    
3. ターミナルでリポジトリをクローン
    

```bash
git clone https://github.com/ユーザー名/リポジトリ名.git
cd リポジトリ名
```

4. Jekyllプロジェクトを作成
    

```bash
jekyll new . --force
```

5. ローカルで確認
    

```bash
bundle exec jekyll serve
```

ブラウザで `http://localhost:4000` にアクセス

---

## **ステップ5：ブログ記事の作成**

- `_posts` フォルダに Markdown ファイルで記事を追加
    
    - ファイル名例：`2025-08-15-my-first-post.md`
        
    - 記事冒頭に Front Matter を追加
        

```yaml
---
layout: post
title: "初めての記事"
date: 2025-08-15
---
本文を書きます
```

---

## **ステップ6：GitHubに反映**

1. 変更をステージング
    

```bash
git add .
```

2. コミット
    

```bash
git commit -m "初めての記事を追加"
```

3. プッシュ
    

```bash
git push origin main
```

---

## **ステップ7：GitHub Pagesで公開**

1. GitHubでリポジトリを開く
    
2. 「Settings」 → 「Pages」
    
3. **Branch** を `main`、**Folder** を `/root` に設定
    
4. 「Save」
    
5. 数分で `https://ユーザー名.github.io/リポジトリ名/` にアクセス可能
    

---

## **ステップ8：運用のポイント**

- 記事は Markdown で管理
    
- デザイン変更はテーマファイルを変更
    
- GitHubで管理するので、履歴やバックアップも自動で保持
    
- GitHub Actionsで自動デプロイも可能
    

---

💡 **おすすめの流れ**

- 最初は Jekyll + GitHub Pages でシンプルに始める
    
- 慣れてきたらテーマやプラグインを導入してカスタマイズ
    

---

