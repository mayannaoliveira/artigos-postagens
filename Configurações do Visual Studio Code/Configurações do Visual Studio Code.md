# Configurações do Visual Studio Code com comentários

Eu resolvi postar as configurações que eu uso no Visual Studio Code, espero que os comentário possa ajudar vocês com a adequação do editor com o tipo de projeto que vocês desenvolvem.
Vocês podem baixar o [setting.json] clicando no link.

```json
/* 
  * Arquivo de configuração do [Visual Studio Code] com comentários.
  * by Mayanna Oliveira
*/

{
// Controla sugestões do [IntelliSense] 
"editor.suggestSelection": "first",
// Delay (ms) da da sugestão 
"editor.quickSuggestionsDelay": 10,
// Pressionar tab para inserir a sugestão
"editor.tabCompletion": "on",
// Habilitar dicas de parâmetros
"editor.parameterHints.enabled": true,
// Sugestões do [IntelliCode]
"vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
// Controla as sugestões que devem ser aceitas com "Enter" além de "Tab". Evita ambigüidades entre inserir novas linhas e aceitar sugestões
"editor.acceptSuggestionOnEnter": "on",
// Controla se sugestões devem ser aceitas durante a digitação
"editor.acceptSuggestionOnCommitCharacter": true,

// Importação automática do [Tabnine]
"tabnine.experimentalAutoImports": true,
// Telemetria 
"telemetry.enableTelemetry": false,

// [CodeRunner] executar no terminal 
"code-runner.runInTerminal": true,

// Associações do editor
"workbench.editorAssociations": [
{
    "viewType": "jupyter-notebook",
    "filenamePattern": "*.ipynb"
    
},
{
  "viewType": "vscode.markdown.preview.editor",
  "filenamePattern": "*.md"
},
{
  "viewType": "hexEditor.hexedit",
  "filenamePattern": "*.hex"
},
{
  "viewType": "hexEditor.hexedit",
  "filenamePattern": "*.ini"
}],

// Token do Ponicode
"ponicode.token": "TOKEN_DO_USUÁRIO",
// Token do Sourcery
"sourcery.token": "TOKEN_DO_USUÁRIO",

// Tema do editor
"workbench.colorTheme": "Ayu Dark Bordered",
// Tema dos ícones
"workbench.iconTheme": "vscode-great-icons",
// Tema dos ícones na barra de atividades
"workbench.productIconTheme": "icons-carbon",
// Como iniciar o editor
"workbench.startupEditor": "newUntitledFile",
// Abrir arquivos em uma nova janela
"window.openFilesInNewWindow": "default",
  
// Tamanho da guia
"editor.tabSize": 2,
// Webviews using iframes
"webview.experimental.useExternalEndpoint": true,
// Zoom girando a bolinha do mouse
"editor.mouseWheelZoom": true,
// Mini mapa
"editor.minimap.enabled": false,
// Salvar automaticamente
"files.autoSave": "afterDelay",

// Visualização rápida do arquivo leia [User Interface]
"workbench.editor.enablePreview": false,
  
// Quebra de linda
"editor.wordWrap": "on",
// Configurações da [Shortcut Menu Bar] leia a [documentação do Menu Bar]
// Atalho para formatar
"ShortcutMenuBar.formatWith": true,
// Atalho para identar linhas
"ShortcutMenuBar.indentLines": true,
// Atalho para salvar tudo
"ShortcutMenuBar.saveAll": true,
// Atalho para ver comandos
"ShortcutMenuBar.showCommands": true,
// Atalho para ocultar barra de atividades
"ShortcutMenuBar.toggleActivityBar": true,
// Atalho para abrir lista de arquivos
"ShortcutMenuBar.openFilesList": false,
// Atalho para GitLive
"GitLive.Issue tracker integration": "Enable",

// Notificações do Kite
"kite.showWelcomeNotificationOnStartup": false,

// Como font padrão foi definida a [Jetbrains Mono]
// Font do CodeLens
"editor.codeLensFontFamily": "Jetbrains Mono",
// Font do editor
"editor.fontFamily": "Jetbrains Mono",
// Font do Inlay Hints
"editor.inlayHints.fontFamily": "Jetbrains Mono",
// Font do das mensagens de commit
"scm.inputFontFamily": "Jetbrains Mono",
// Font do console
"debug.console.fontFamily": "Jetbrains Mono",
// Font do terminal
"terminal.integrated.fontFamily": "Jetbrains Mono",
// Tamanho da font do terminal
"terminal.integrated.fontSize": 15,
// Espessura da font
"editor.fontWeight": 400,

// Configurações do [Bracket Pair Colorizer 2]
// Mostrar o parênteses ativo na régua
"bracket-pair-colorizer-2.showBracketsInRuler": true,
// Posição do parênteses na régua
"bracket-pair-colorizer-2.rulerPosition": "Center",
// Mostrar posição do parênteses ativo na margem
"bracket-pair-colorizer-2.showBracketsInGutter": true,
// Cores dos parênteses
"bracket-pair-colorizer-2.colors": [
  "Gold",
  "Violet",
  "Orchid",
  "LightSkyBlue",
  "Salmon",
  "LawnGreen",
  "DarkOrange",
  "Purple",
  "Cornsilk"
],
// Configurações para uso no CSS
"bracket-pair-colorizer-2.activeScopeCSS": [
  "borderStyle : solid",
  "borderWidth : 1px",
  "borderColor : {color}",
  "opacity: 0.5"
],
// Linha horizontal para criar um bloco ao redor do parênteses
"bracket-pair-colorizer-2.showVerticalScopeLine": true,
// Fechar parênteses automaticamente 
"editor.autoClosingBrackets": "always",
// Destacar os parênteses
"bracket-pair-colorizer-2.colorMode": "Independent",
// Mostrar uma linha indicando abertura e fechamento do parênteses
"bracket-pair-colorizer-2.showHorizontalScopeLine":true,
// A linha de escopo começará na posição final do parênteses
"bracket-pair-colorizer-2.highlightActiveScope":true,
// Não usar extenção para as seguintes linguagens
// "bracket-pair-colorizer-2.excludedLanguages": [],

// Configurações do [Debugging]
"debug.onTaskErrors": "abort",

// Arquivos confiáveis leia [Restricted Mode]
"security.workspace.trust.untrustedFiles": "open",

"git.autofetch": true,
// Configurações do [Integrated Terminal]
// Evita que combinações de teclas específicas sejam manipuladas pelo terminal
"terminal.integrated.commandsToSkipShell": [
    "workbench.action.toggleSidebarVisibility",
    "language-julia.interrupt"
],
// Na divisão o terminal iniciará no diretório com o qual o terminal pai foi iniciado
"terminal.integrated.splitCwd": "workspaceRoot",

// Definições do [Julia]
"julia.symbolCacheDownload": true,

// Conexões do [SQLTools] leia a documentação do [SQLTools Database management]
"sqltools.connections": [

],

// Comfigurações do [Emmet]
"emmet.includeLanguages": {
    "django-html": "html",
    "django-txt": "html"
},
"explorer.confirmDelete": false,
"window.zoomLevel": -1,

// Configurações para Markdown
"[markdown]": {
  "editor.defaultFormatter": "yzhang.markdown-all-in-one"
},

// Configurações para CSS
"[css]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.autoClosingBrackets": "always"
},

// Configurações para Json
"[json]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},

// Configurações para Jsonc
"[jsonc]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode"
},

// Configurações para Typescript
"[typescript]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.autoClosingBrackets": "always"
},

// Configurações para SCSS
"[scss]": {
  "editor.defaultFormatter": "HookyQR.beautify",
  "editor.autoClosingBrackets": "always"
},

// Configurações para HTML
"[html]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.autoClosingBrackets": "always"
},


// Associações das sintax das linguagens
"files.associations": {
  "**/*.html": "html",
  "**/templates/*/*.html": "django-html",
  "**/templates/*": "django-txt",
  "**/requirements{/**,*}.{txt,in}": "pip-requirements"
},

// Configurações da [Auto Close Tag]
"auto-close-tag.activationOnLanguage": [
  "django-html",
  "Python",
  "xml",
  "php",
  "blade",
  "ejs",
  "jinja",
  "javascript",
  "javascriptreact",
  "typescript",
  "typescriptreact",
  "plaintext",
  "markdown",
  "vue",
  "liquid",
  "erb",
  "lang-cfml",
  "cfml",
  "HTML (Eex)"
],

// Configurações do [TODO Highlight]
// Case sensitive
"todohighlight.isCaseSensitive": false,
// Definição de palavras chaves para o TODO Highlight
"todohighlight.keywords": [
  {
    "text": "TESTANDO",
    "color": "#000",
    "backgroundColor": "#f0b00d",
    "overviewRulerColor": "#f0b00d"
  },
  {
    "text": "GITHUB",
    "color": "#fff",
    "backgroundColor": "#000",
    "overviewRulerColor": "#fff"
  },
  {
    "text": "POSTADO",
    "color": "#000",
    "backgroundColor": "#0c9aa7",
    "overviewRulerColor": "#0c9aa7"
  },
  {
    "text": "APROVADO",
    "color": "#000",
    "backgroundColor": "#1e691b",
    "overviewRulerColor": "#1e691b"
  },
  {
    "text": "REPROVADO",
    "color": "#fff",
    "backgroundColor": "#7f0101",
    "overviewRulerColor": "#7f0101"
  }
],

// Cor do Bookmarks na régua
"bookmarks.overviewRuler": "#2175ca",
// Salvar o Bookmarks do projeto
"bookmarks.saveBookmarksInProject": true,

// Configurações do [Comment Anchors]
// Atrasar o carregamento das âncoras, padrão é true
"commentAnchors.workspace.lazyLoad": false,
// Palavras chaves para serem ancoradas
"commentAnchors.tags.list": [
{
  "tag": "TESTANDO",
  "scope": "file",
  "iconColor": "#f0b00d",
  "highlightColor": "#f0b00d",
  "styleComment": true
},
  {
  "tag": "GITHUB",
  "scope": "file",
  "iconColor": "#969696",
  "highlightColor": "#969696",
  "styleComment": true
},
  {
  "tag": "REPROVADO",
  "scope": "file",
  "iconColor": "#7f0101",
  "highlightColor": "#7f0101",
  "styleComment": true
},
  {
  "tag": "POSTADO",
  "scope": "file",
  "iconColor": "#0c9aa7",
  "highlightColor": "#0c9aa7",
  "styleComment": true
},
  {
  "tag": "APROVADO",
  "scope": "file",
  "iconColor": "#1e691b",
  "highlightColor": "#1e691b",
  "styleComment": true
},
  {
  "tag": "TESTANDO",
  "scope": "file",
  "iconColor": "#1e691b",
  "highlightColor": "#1e691b",
  "styleComment": true
}],
// Configurações da [Todo Tree]
"todo-tree.highlights.customHighlight": {
"[ ]": {
    "background": "#a70c0c"
},
"[x]": {
    "background": "#266902"
},
"[APROVADO]": {
  "icon": "check-circle-fill",
  "type": "line",
  "foreground": "black",
  "iconColour": "yellow",
  "gutterIcon": true
},
"[REPROVADO]": {
  "icon": "alert",
  "type": "line",
  "foreground": "black",
  "iconColour": "yellow",
  "gutterIcon": true
},
"[POSTADO]": {
  "icon": "thumbsup",
  "type": "line",
  "foreground": "black",
  "iconColour": "yellow",
  "gutterIcon": true
},
"[GITHUB]": {
  "icon": "mark-github",
  "type": "line",
  "foreground": "black",
  "iconColour": "yellow",
  "gutterIcon": true
}
},
// Escanear workspace ou current file
"todo-tree.tree.scanMode": "current file",
// Botão para escanear
"todo-tree.tree.showScanModeButton": true,
// Modo de pasta compacta
"todo-tree.tree.disableCompactFolders": true,
// Destaque
"todo-tree.highlights.defaultHighlight": {
        "type": "text-and-comment"
},
// Tags do TODO Tree
"todo-tree.general.tags": [
  "BUG",
  "REPROVADO",
  "APROVADO",
  "GITHUB",
  "TESTANDO",
  "FIXME",
  "TODO",
  "[ ]",
  "[x]"
]
  } // Fim
```
 
<!-- Links de referência: -->
[IntelliSense]: https://code.visualstudio.com/docs/editor/intellisense
[Emmet]: https://marketplace.visualstudio.com/items?itemName=FallenMax.mithril-emmet
[SQLTools]: https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools
[SQLTools Database management]: https://vscode-sqltools.mteixeira.dev/
[Jetbrains Mono]: https://www.jetbrains.com/lp/mono/
[IntelliCode]: https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode
[Tabnine]: https://www.tabnine.com/
[Shortcut Menu Bar]: https://marketplace.visualstudio.com/items?itemName=jerrygoyal.shortcut-menu-bar
[documentação do Menu Bar]: https://github.com/GorvGoyl/Shortcut-Menu-Bar-VSCode-Extension
[User Interface]: https://code.visualstudio.com/docs/getstarted/userinterface
[Bracket Pair Colorizer 2]: https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2
[Debugging]: https://code.visualstudio.com/docs/editor/debugging
[Visual Studio Code]: https://marketplace.visualstudio.com/
[CodeRunner]: https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner
[TODO Highlight]: https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight
[Restricted Mode]: https://code.visualstudio.com/docs/editor/workspace-trust
[Integrated Terminal]: https://code.visualstudio.com/docs/editor/integrated-terminal
[Julia]: https://marketplace.visualstudio.com/items?itemName=julialang.language-julia
[Auto Close Tag]: https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag
[Bookmarks]: https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks
[Todo Tree]: https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree
[Comment Anchors]: https://marketplace.visualstudio.com/items?itemName=ExodiusStudios.comment-anchors
[Sourcery]: https://marketplace.visualstudio.com/items?itemName=sourcery.sourcery

Alguns comando só irão funcionar se tiver determinadas extensões instaladas. Imagem para melhor visualização do código:

![setting.json](https://i.imgur.com/byfRlI1.png)

#### Lista das referências 

[IntelliSense](https://code.visualstudio.com/docs/editor/intellisense), [Emmet](https://marketplace.visualstudio.com/items?itemName=FallenMax.mithril-emmet), [SQLTools](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools), [SQLTools Database management](https://vscode-sqltools.mteixeira.dev/), [Jetbrains Mono](https://www.jetbrains.com/lp/mono/), [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode), [Tabnine](https://www.tabnine.com/), [Shortcut Menu Bar](https://marketplace.visualstudio.com/items?itemName=jerrygoyal.shortcut-menu-bar), [documentação do Menu Bar](https://github.com/GorvGoyl/Shortcut-Menu-Bar-VSCode-Extension), [User Interface](https://code.visualstudio.com/docs/getstarted/userinterface), [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2), [Debugging](https://code.visualstudio.com/docs/editor/debugging), [Visual Studio Code](https://marketplace.visualstudio.com/),
[CodeRunner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner), [TODO Highlight](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight), [Restricted Mode](https://code.visualstudio.com/docs/editor/workspace-trust), [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal), [Julia](https://marketplace.visualstudio.com/items?itemName=julialang.language-julia), [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag), [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks), [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree), [Comment Anchors](https://marketplace.visualstudio.com/items?itemName=ExodiusStudios.comment-anchors) e [Sourcery](https://marketplace.visualstudio.com/items?itemName=sourcery.sourcery).

[Linktree]: https://linktr.ee/mayannaoliveira
[Github]: https://github.com/mayannaoliveira
[setting.json]: https://carbon.now.sh/

##### Postagem disponível
[![Hashnode](https://img.shields.io/badge/Publicado_no-Hashnode-blue?style=for-the-badge&logoColor=00C11C&logo=data:image/png;base64,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)](https://maosnocodigo.hashnode.dev/) 

##### Siga-me nas redes sociais
[![github](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mayannaoliveira) [![gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white&link=mailto:mayannait@gmail.com)](mailto:mayannait@gmail.com) [![whatsapp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://api.whatsapp.com/message/5XLG4UPSFCNWP1) [![linktree](https://img.shields.io/badge/linktree-39E09B?style=for-the-badge&logo=linktree&logoColor=white)](https://linktr.ee/mayannaoliveira) [![instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/oliveiramayanna/) [![twitter](https://img.shields.io/badge/twitter-blue?style=for-the-badge&logo=twitter&logoColor=white)](ttps://twitter.com/oliveiramayanna/)