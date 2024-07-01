# https://github.com/tailwindlabs/tailwindcss/issues/13931

Steps: Add this to your VSCode settings.json file

```
"[elm]": {
    "tailwindCSS.experimental.classRegex": [
      "\\bclass[\\s(<|]+\"([^\"]*)\"",
      "\\bclass[\\s(]+\"[^\"]*\"[\\s+]+\"([^\"]*)\"",
      "\\bclass[\\s<|]+\"[^\"]*\"\\s*\\+{2}\\s*\" ([^\"]*)\"",
      "\\bclass[\\s<|]+\"[^\"]*\"\\s*\\+{2}\\s*\" [^\"]*\"\\s*\\+{2}\\s*\" ([^\"]*)\"",
      "\\bclass[\\s<|]+\"[^\"]*\"\\s*\\+{2}\\s*\" [^\"]*\"\\s*\\+{2}\\s*\" [^\"]*\"\\s*\\+{2}\\s*\" ([^\"]*)\"",
      "\\bclassList[\\s\\[\\(]+\"([^\"]*)\"",
      "\\bclassList[\\s\\[\\(]+\"[^\"]*\",\\s[^\\)]+\\)[\\s\\[\\(,]+\"([^\"]*)\"",
      "\\bclassList[\\s\\[\\(]+\"[^\"]*\",\\s[^\\)]+\\)[\\s\\[\\(,]+\"[^\"]*\",\\s[^\\)]+\\)[\\s\\[\\(,]+\"([^\"]*)\""
    ]
},
"editor.quickSuggestions": {
"strings": true
},
"tailwindCSS.includeLanguages": {
"elm": "html"
},
```

Install bradlc.vscode-tailwindcss 0.10.5.

You should be able to get suggestions inside of `src/Main.elm`.

Now upgrade to version 0.12.x. No suggestions anymore.


