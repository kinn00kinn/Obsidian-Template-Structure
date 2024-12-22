---
title: Obsidian Sample Code
published: 2024-12-15
source: https://zenn.dev/kinnkinn/articles/dc4ad7e9404eb2
description: ObsidianのSample Codeを記述する
---
# Obsidian Sample Code

---

## 基本記法
基本的なマークダウン記法です．

### リスト
- 箇条書きリスト
	- 入れ子
1. 順列つきリスト
	1. 入れ子
- [ ] タスクリスト
	- [ ] 入れ子

### 強調
- **太字**
- *イタリック*
- ~~取り消し線~~
- ==マーカー==

### リンク
- 内部リンク:  [[Sample Code]]
- 外部リンク: [Google](https://google.com)

### コードブロック
- インラインコード: `Sample Code`
- ブロックコード:
```markdown
  - 言語名
  - サンプルコード
  
```

```python
print("Hello, World!")
```

---

## テーブル (Advanced Tablesプラグイン)

| 項目   | 値   | 備考         |
| ------ | ---- | ------------ |
| Sample | 100  | サンプルデータ |
| Test   | 200  | テストデータ   |

---

## データビュー (Dataviewプラグイン)

```dataview
TABLE file.name AS Name, file.mtime AS "Last Modified"
FROM "Sample Code"
SORT file.mtime DESC
```

- フォルダ "Folder Name" 内のファイルを一覧表示。
- 最終更新日時でソート。

---

## テンプレート (Templaterプラグイン)
Templaterで実行の設定をしないと実行ができません

- 作成日:  <% tp.date.now() %>
- タイトル: <% tp.file.title %>
- カスタムプロンプト: <% tp.prompt("入力してください:") %>

---

## 数式 (LaTeX)
数学的表現を分かりやすく、かつ実用性を高めるためのセクションです。

### インライン数式
- 実際の文中に組み込む場合に便利です。
- 例: $\sum_{i=1}^n i = \frac{n(n+1)}{2}$

### ブロック数式
- 数式を独立して強調する場合に使用します。
- 例:
$$
E=mc^2
$$

### 応用例: 行列と連立方程式

行列や複雑な式も簡潔に表現できます。

#### **行列表現**

$$
A = 
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$


#### **連立方程式**

$$
\begin{cases}
ax + by = c \\
dx + ey = f
\end{cases}
$$

### カスタム例: カラフルな数式
LaTeX の `\textcolor` を活用して色を追加すると、強調表示に便利です。


$$
\textcolor{red}{E} = \textcolor{blue}{m}c^2
$$


---

## HTMLカスタマイズ

Markdown に HTML を埋め込むことで、デザインの幅を広げます。



### 中央揃え + カラー + サイズ調整
- HTML スタイルを使ってデザインを改善。

<div style="text-align: center; color: blue; font-weight: bold; font-size: 24px;">
    青色 + 大文字
</div>

<br><br>

### 応用: 影付きボックスデザイン
- ボックスの影やパディングを追加して目立たせることが可能です。

<div style="border: 2px solid #444; padding: 20px; border-radius: 10px; box-shadow: 5px 5px 10px rgba(0,0,0,0.2);">
    デザインを高めたボックス
</div>

<br><br>

### モバイル対応: 可変幅のレスポンシブデザイン
- **`width: 100%`** を使って可変幅を実現。

<div style="text-align: center; color: #fff; background-color: #555; padding: 10px; border-radius: 5px; width: 100%;">
    幅可変レスポンシブボックス
</div>

