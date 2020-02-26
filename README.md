<img src="https://raw.githubusercontent.com/dayitv89/perfect-code/master/images/perfect-code.png" alt="drawing" width="200px"/>

# perfect-code [VSCode Extension]

[![v1.1.2](https://img.shields.io/badge/Latest_release-v1.1.2-green.svg?style=flat)](./CHANGELOG.md)

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
ProtoMaker
```

Extension detail: `$ code --list-extensions --show-versions`

```
2gua.rainbow-brackets
alexdima.copy-relative-path
brofox86.theme-espresso-soda-solarized
christian-kohler.path-intellisense
dbaeumer.vscode-eslint
esbenp.prettier-vscode
formulahendry.auto-close-tag
formulahendry.auto-complete-tag
formulahendry.auto-rename-tag
formulahendry.code-runner
jundat95.react-native-snippet
luongnd.edge
mgmcdermott.vscode-language-babel
mikestead.dotenv
ms-vscode.atom-keybindings
ms-vscode.cpptools
ms-vscode.node-debug2
msjsdiag.debugger-for-chrome
naumovs.color-highlight
PKief.material-icon-theme
streetsidesoftware.code-spell-checker
vsmobile.vscode-react-native
waderyan.gitblame
wayou.vscode-todo-highlight
wmaurer.change-case
orta.vscode-jest
vikramvk.protomaker
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
	"cSpell.ignoreWords": [
		"punchh",
		"reactotron",
		"proto",
		"props",
		"reactnative",
		"gaurav",
		"sharma",
		"redeemable",
		"Signup",
		"redeemables",
		"gorm",
		"repo",
		"repos"
	],
	"editor.renderWhitespace": "all",
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
				"type": "node",
				"request": "launch",
				"name": "adonis",
				"program": "${workspaceFolder}/server.js"
			},
			{
				"name": "Debug react native",
				"program": "${workspaceRoot}/.vscode/launchReactNative.js",
				"type": "reactnative",
				"request": "attach",
				"sourceMaps": true,
				"outDir": "${workspaceRoot}/.vscode/.react",
				"runtimeArgs": ["--preserve-symlinks"]
			},
			{
				"type": "node",
				"request": "launch",
				"name": "debug node",
				"program": "${file}"
			},
			{
				"type": "node",
				"request": "launch",
				"name": "Launch nodejs server.js",
				"program": "${workspaceFolder}/server.js"
			},
			{
				"type": "node",
				"request": "attach",
				"name": "node attach to process",
				"processId": "${command:PickProcess}"
			},
			{
				"type": "node",
				"request": "attach",
				"name": "Node: Nodemon",
				"processId": "${command:PickProcess}",
				"restart": true,
				"protocol": "inspector"
			},
			{
				"name": "golang app.go",
				"type": "go",
				"request": "launch",
				"mode": "auto",
				"program": "${workspaceRoot}/app.go",
				"env": {},
				"args": []
			},
			{
				"name": "golang",
				"type": "go",
				"request": "launch",
				"mode": "debug",
				"program": "${file}"
			}
		]
	},
	"workbench.iconTheme": "material-icon-theme",
	"workbench.colorTheme": "Solarized Espresso Soda",
	"editor.minimap.enabled": false,
	"breadcrumbs.enabled": true,
	"prettier.disableLanguages": ["vue", "html"],
	"liveServer.settings.donotShowInfoMsg": true,
	"liveServer.settings.donotVerifyTags": true,
	"editor.suggestSelection": "first",
	"vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
	"java.errors.incompleteClasspath.severity": "ignore",
	"java.configuration.checkProjectSettingsExclusions": false,
	"javascript.suggest.autoImports": false,
	"terminal.integrated.shell.osx": "/bin/bash"
}
```

### `Keybindings.json` shortcuts (VSCode -> Preferences -> Keyboard Shortcuts -> [edit] Keybindings.json)

```json
[
	{
		"mac": "cmd+k",
		"win": "ctrl+k",
		"linux": "ctrl+k",
		"key": "cmd+k",
		"command": "workbench.debug.panel.action.clearReplAction",
		"when": "inDebugRepl"
	},
	{
		"mac": "cmd+j",
		"win": "ctrl+j",
		"linux": "ctrl+j",
		"key": "cmd+j",
		"command": "workbench.action.togglePanel"
	}
]
```

### Code snippets (VSCode -> Preferences -> User Snippets -> New Global Snippets file)

```json
{
	"Default react-native header": {
		"prefix": "rnp",
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
	"Default tron log": {
		"prefix": "tron",
		"body": "console.tron.log(${1:log});"
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
			"${1:export}.defaultProps = {",
			"};",
			"",
			"export default ${1:export};"
		]
	}
}
```
