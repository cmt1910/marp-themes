# marp-themes

Marp用のカスタムテーマです。Marp for VS Code バージョン3.2.0で動作確認をしています。

## 使用方法

以下の方法のいずれかを使用してテーマを適用することができます。

- リモートのCSSを参照 (推奨)
- 手動インストール

> [!NOTE]
> Marp CLIではリモートのURLを参照することができないため、手動インストールでCSSを配置してください。

### リモートのCSSを参照 (推奨)

VS Codeに拡張機能Marp for VS Codeを導入したうえで、以下のようにディレクトリを構成します。

```text
marp-project
├ slide.md // スライドになるMarkdownファイル
└ .vscode
　 └ settings.json
```

#### settings.json

settings.jsonには使用するテーマが記述されたCSSファイルのURLを追記します。

```json
{
    "markdown.marp.themes": [
        "https://cmt1910.github.io/marp-themes/<ファイルパス>"
    ],
}
```

#### slide.md

Markdownファイルの先頭に以下のように使用するテーマ名を記述します。

```markdown
---
marp: true
theme: テーマ名
---

# タイトル...
```

### 手動インストール

VS Codeに拡張機能Marp for VS Codeを導入したうえで、以下のようにディレクトリを構成します。

```text
marp-project
├ slide.md // スライドになるMarkdownファイル
├ theme
│ └ theme.css // 使用するテーマが記述されたCSSファイル
└ .vscode
　 └ settings.json
```

#### settings.json

settings.jsonには使用するテーマが記述されたCSSファイルのパスを追記します。

```json
{
    "markdown.marp.themes": [
        "./themes/theme.css"
    ],
}
```

#### slide.md

Markdownファイルの先頭に以下のように使用するテーマ名を記述します。

```markdown
---
marp: true
theme: テーマ名
---

# タイトル...
```
