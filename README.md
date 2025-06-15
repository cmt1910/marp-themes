# marp-themes

Marp用のカスタムテーマです。Marp for VS Code バージョン3.2.0で動作確認をしています。

## 使用方法

VS Codeに拡張機能Marp for VS Codeを導入したうえで、以下のようにディレクトリを構成します。

```text
marp-project
├ slide.md // スライドになるMarkdownファイル
├ theme
│ └ theme.css // 使用するテーマが記述されたCSSファイル
└ .vscode
　 └ settings.json
```

### settings.json

settings.jsonには使用するテーマが記述されたCSSファイルのパスを追記します。

```json
{
    "markdown.marp.themes": [
        "./themes/theme.css"
    ],
}
```

### slide.md

Markdownファイルの先頭に以下のように使用するテーマ名を記述します。

```markdown
---
marp: true
theme: テーマ名
---

# タイトル...
```
