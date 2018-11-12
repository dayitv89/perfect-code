<img src="https://raw.githubusercontent.com/dayitv89/perfect-code/master/images/perfect-code.png" alt="drawing" width="200px"/>

# perfect-code [VSCode Extension]

[![v1.0.1](https://img.shields.io/badge/Latest_release-v1.0.2-green.svg?style=flat)](./CHANGELOG.md)

All in one place to good start with VSCode. If you came from Atom/Sublime and moving to VSCode, you'll find a lot of features different from your traditional editor. But you can make compatible by one shot.

#### Advantages to switch VSCode:

- In build debugger for node/ react-native and almost every language.
- More lighter than atom/ sublime

### Initial release with following extension:

Extension Name

```js
Atom Keymap
Auto close Tag
Auto Complete Tag
Auto Rename Tag
Babel JavaScript
C/C++
change-case
Code Runner
Code Spell Checker
Color Highlight
Copy Relative Path
Debugger For Chrome
DotENV
Edge template Support
Git Blame
Material Icon Theme
Node Debug
Path Intellisense
Prettier - Code formatter
Rainbow Brackets
React Native Snippet
React Native Tools
Solarized Espresso Soda
TODO Highlight
Jest
```

Extension detail: `$ code --list-extensions --show-versions`

```
2gua.rainbow-brackets@0.0.6
alexdima.copy-relative-path@0.0.2
brofox86.theme-espresso-soda-solarized@3.0.0
christian-kohler.path-intellisense@1.4.2
dbaeumer.vscode-eslint@1.4.12
esbenp.prettier-vscode@1.5.0
formulahendry.auto-close-tag@0.5.6
formulahendry.auto-complete-tag@0.0.2
formulahendry.auto-rename-tag@0.0.15
formulahendry.code-runner@0.9.3
jundat95.react-native-snippet@0.4.3
luongnd.edge@0.2.0
mgmcdermott.vscode-language-babel@0.0.17
mikestead.dotenv@1.0.1
ms-vscode.atom-keybindings@3.0.4
ms-vscode.cpptools@0.17.5
ms-vscode.node-debug2@1.24.2
msjsdiag.debugger-for-chrome@4.6.0
naumovs.color-highlight@2.3.0
PKief.material-icon-theme@3.5.0
streetsidesoftware.code-spell-checker@1.6.10
vsmobile.vscode-react-native@0.6.11
waderyan.gitblame@2.4.2
wayou.vscode-todo-highlight@0.5.12
wmaurer.change-case@1.0.0
orta.vscode-jest
```

### User Setting (VSCode -> Preferences -> Settings -> User Settings)

```json
{
	"window.zoomLevel": 0,
	"atomKeymap.promptV3Features": true,
	"editor.formatOnPaste": false,
	"editor.formatOnSave": true,
	"prettier.printWidth": 120,
	"prettier.useTabs": true,
	"prettier.singleQuote": true,
	"cSpell.ignoreWords": ["punchh", "reactotron", "proto", "props", "reactnative", "gaurav", "sharma"],
	"editor.renderWhitespace": "boundary",
	"editor.insertSpaces": false,
	"editor.rulers": [120],
	"search.location": "panel",
	"search.useIgnoreFiles": false,
	"search.quickOpen.includeSymbols": false,
	"search.exclude": {
		"**/node_modules": false,
		"**/bower_components": true
	},
	"workbench.editor.enablePreviewFromQuickOpen": false,
	"explorer.confirmDragAndDrop": false,
	"extensions.ignoreRecommendations": false,
	"explorer.confirmDelete": false,
	"emmet.includeLanguages": {
		"vue-html": "html",
		"edge": "javascriptreact"
	},
	"workbench.startupEditor": "welcomePage",
	"launch": {
		"version": "0.2.0",
		"configurations": [
			{
				"name": "Debug react native",
				"program": "${workspaceRoot}/.vscode/launchReactNative.js",
				"type": "reactnative",
				"request": "attach",
				"sourceMaps": true,
				"outDir": "${workspaceRoot}/.vscode/.react"
			},
			{
				"type": "node",
				"request": "launch",
				"name": "debug node",
				"program": "${file}"
			}
		]
	},
	"workbench.iconTheme": "material-icon-theme",
	"workbench.colorTheme": "Solarized Espresso Soda"
}
```

### `Keybindings.json` shortcuts (VSCode -> Preferences -> Keyboard Shortcuts -> [edit] Keybindings.json)

```json
[
	{
		"key": "cmd+k",
		"command": "workbench.debug.panel.action.clearReplAction",
		"when": "inDebugRepl"
	},
	{
		"key": "cmd+j",
		"command": "workbench.action.togglePanel"
	},
	{
		"key": "cmd+j",
		"command": "-workbench.action.togglePanel"
	}
]
```

### Code snippets (VSCode -> Preferences -> User Snippets -> New Global Snippets file)

```json
{
	"Default react-native header": {
		"prefix": "rnh",
		"body": [
			"/**",
			" * Copyright (c) 2017-Present, Punchh, Inc.",
			" * All rights reserved.",
			" *",
			" * @flow",
			" */",
			"'use strict';"
		]
	},
	"Default GDS react-native header": {
		"prefix": "gds",
		"body": [
			"/**",
			" * Copyright (c) 2017-Present, Gaurav D. Sharma",
			" * All rights reserved.",
			" *",
			" * @flow",
			" */",
			"'use strict';"
		]
	},
	"JSON Print": {
		"prefix": "json",
		"scope": "javascript,typescript",
		"body": "JSON.stringify(${1:object}, null, 2)"
	},
	"Import Print": {
		"prefix": "imt",
		"body": "import ${1:module} from '${1:module}';"
	},
	"Export stmt": {
		"prefix": "mex",
		"body": ["module.exports = {", "${1:export}", "};"]
	},
	"Export class stmt": {
		"prefix": "cex",
		"body": [
			"${1:export}.propTypes = {",
			"};",
			"",
			"{1:export}.defaultProps = {",
			"};",
			"",
			"export default {1:export};"
		]
	}
}
```
