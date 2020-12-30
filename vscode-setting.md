### vscode-setting.js配置
```
{
  // 是否已启用自动刷新
  "git.autorefresh": false,
  // 是否启用了自动提取。
  "git.autofetch": false,
  // 保存时自动格式化代码
  "editor.formatOnSave": true, // 或者"eslint.autoFixOnSave": true,
  // 配置 emmet 兼容 vue 文件
  "emmet.includeLanguages": {
    "vue": "html"
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "html",
    "vue",
  ],
  "eslint.options": {
    "plugins": [
      "html"
    ]
  },
  "eslint.workingDirectories": [
    ".eslintrc.js",
    {
      "mode": "auto"
    }
  ],
  // Enable/disable default JavaScript formatter (For Prettier)
  "javascript.format.enable": true,
  "prettier.singleQuote": true, // 使用带引号替代双引号
  // 点击保存时，根据 eslint 规则自定修复，同时集成 prettier 到 eslint 中
  "prettier.eslintIntegration": true,
  // 窗口时取焦点时自动保存
  "files.autoSave": "onFocusChange",
  /*
  "vetur.format.defaultFormatterOptions": {
    "js-beautify-html": {
      // html 标签中属性的排列格式
      "wrap_attributes": "force-aligned" // auto force
    },
    // "stylusSupremacy.insertSemicolons": false, //#去掉分号
    // "stylusSupremacy.insertBraces": false, //#去掉大括号
    // "stylusSupremacy.insertColons": false, //#去掉冒号
    "stylusSupremacy.insertNewLineAroundImports": false, // import之后是否换行
  },
  */
  "vetur.format.defaultFormatterOptions": {
    "wrap_attributes": "force-expand-multiline",
    "js-beautify-html": {
      "wrap_attributes": "force-expand-multiline",
      "end_with_newline": false
    }
  },
  // vetur 格式化 html 文本的工具选择
  "vetur.format.defaultFormatter.html": "js-beautify-html",
  // 禁用 vetur 格式化 js 内容（已配置 eslint 进行格式化）
  "vetur.format.defaultFormatter.js": "none",
  "window.zoomLevel": 1,
  "[html]": {
    "editor.defaultFormatter": "HookyQR.beautify"
  },
  "diffEditor.ignoreTrimWhitespace": true,
  "explorer.confirmDelete": false,
  "background.enabled": true,
  "background.useDefault": false,
  "background.customImages": [
    "/Users/dirunru/Documents/images/time1.jpg"
  ],
  "background.style": {
    "content": "''",
    "pointer-events": "none",
    "position": "absolute",
    "z-index": "99999",
    "width": "100%",
    "height": "100%",
    "background-position": "center",
    "background-repeat": "no-repeat",
    "background-size": "100% 100%",
    "opacity": 0.1
  },
  // 保存后自动修复格式
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "git.confirmSync": false,
}
```

```
{
  "editor.tabSize": 2,
  "workbench.editor.showTabs": true,
  "extensions.ignoreRecommendations": false,
  "eslint.run": "onType",
  "eslint.options": {
    "extensions": [".js", ".vue"],
  }, 
  // "eslint.enable": true,
  "editor.formatOnSave": false, 
  "editor.autoFixOnSave": true,
  "eslint.validate": [
    "javascript",
    "javascriptReact",
    "vue",
    "html",
  ],
  "javascript.format.insertSpaceBeforeFunctionParenthesis": true,
  "editor.renderIndentGuides": false,
  "guides.normal.color.dark": "rgba(91, 91, 91, 0.6)",
  "guides.normal.color.light": "rgba(220, 220, 220, 0.7)",
  "guides.active.color.dark": "rgba(210, 110, 210, 0.6)",
  "guides.active.color.light": "rgba(200, 100, 100, 0.7)",
  "guides.active.style": "dashed",
  "guides.normal.style": "dashed",
  "guides.stack.style": "dashed",
  "window.openFilesInNewWindow": "on",
  "html.format.wrapAttributes": "force-expand-multiline",
  "emmet.syntaxProfiles": {
    "vue-html": "html",
    "vue": "html"
  },
  "emmet.showExpandedAbbreviation": "always",
  "emmet.includeLanguages": {
    "vue-html": "html",
    "vue": "html"
  },
  "files.eol": "\n",
  "editor.quickSuggestions": {
    // "other": true,
    // "comments": false,
    "strings": true
  },
  "[jsonc]": {
    "editor.defaultFormatter": "HookyQR.beautify"
  },
  "[json]": {
    "editor.defaultFormatter": "HookyQR.beautify"
  },
  "files.autoSave": "off",  
  "editor.fontSize": 16,
  "editor.minimap.enabled": false,
  "vetur.format.defaultFormatter.js": "vscode-typescript",
  "[javascript]": {
    "editor.defaultFormatter": "vscode.typescript-language-features",
  },
  "window.zoomLevel": 0,
  "workbench.sideBar.location": "left",
  "workbench.activityBar.visible": true,
  // "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",
  "git.autofetch": true,
}
```
