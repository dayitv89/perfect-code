<img src="https://raw.githubusercontent.com/dayitv89/perfect-code/master/images/perfect-code.png" alt="drawing" width="200px"/>

# perfect-code [VSCode Extension]

[![v1.1.3](https://img.shields.io/badge/Latest_release-v1.1.3-green.svg?style=flat)](./CHANGELOG.md)

All in one place to good start with VSCode. If you came from Atom/Sublime and moving to VSCode, you'll find a lot of features different from your traditional editor. But you can make compatible by one shot.

#### Advantages to switch VSCode:

-   In build debugger for node/ react-native and almost every language.
-   More lighter than atom/ sublime

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
Formatter Toggle
VSCode Intellicode
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
tombonnike.vscode-status-bar-format-toggle
VisualStudioExptTeam.vscodeintellicode
```

### User Setting (VSCode -> Preferences -> Settings -> User Settings)

```json
{
	"window.zoomLevel": 0,
	"atomKeymap.promptV3Features": true,
	"editor.formatOnPaste": true,
	"cSpell.ignoreWords": [
		"punchh",
		"reactotron",
		"proto",
		"props",
		"reactnative",
		"gaurav",
		"gauravds",
		"sharma",
		"redeemable",
		"Signup",
		"redeemables",
		"gorm",
		"repo",
		"repos",
		"bson",
		"rcvr",
		"algo"
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
				"name": "react-native",
				"program": "${workspaceRoot}/.vscode/launchReactNative.js",
				"type": "reactnative",
				"request": "attach",
				"sourceMaps": true,
				"cwd": "${workspaceFolder}"
			},
			{
				"name": "node current file",
				"type": "node",
				"request": "launch",
				"program": "${file}"
			},
			{
				"name": "node server.js",
				"type": "node",
				"request": "launch",
				"program": "${workspaceFolder}/server.js"
			},
			{
				"name": "node attach to process",
				"type": "node",
				"request": "attach",
				"processId": "${command:PickProcess}"
			},
			{
				"name": "Node: Nodemon",
				"type": "node",
				"request": "attach",
				"processId": "${command:PickProcess}",
				"restart": true,
				"protocol": "inspector"
			},
			{
				"name": "golang current file",
				"type": "go",
				"request": "launch",
				"mode": "debug",
				"program": "${file}"
			},
			{
				"name": "golang main.go",
				"type": "go",
				"request": "launch",
				"mode": "debug",
				"program": "${workspaceRoot}/main.go",
				"env": {},
				"args": [],
				"trace": "error"
			},
			{
				"name": "golang main.go cli",
				"type": "go",
				"request": "launch",
				"mode": "debug",
				"program": "${workspaceRoot}/main.go",
				"env": {},
				"args": ["cli"],
				"trace": "error"
			},
			{
				"name": "server: golang main.go",
				"type": "go",
				"request": "launch",
				"mode": "debug",
				"program": "${workspaceRoot}/main.go",
				"env": {
					"INSTANCE_TYPE": "server"
				},
				"args": [],
				"trace": "error"
			},
			{
				"name": "worker@3001: golang main.go",
				"type": "go",
				"request": "launch",
				"mode": "debug",
				"program": "${workspaceRoot}/main.go",
				"env": {
					"INSTANCE_TYPE": "worker",
					"PORT": "3001"
				},
				"args": [],
				"trace": "error"
			}
		]
	},
	"workbench.iconTheme": "material-icon-theme",
	"workbench.colorTheme": "Solarized Espresso Soda",
	"editor.minimap.enabled": false,
	"breadcrumbs.enabled": true,
	"liveServer.settings.donotShowInfoMsg": true,
	"liveServer.settings.donotVerifyTags": true,
	"editor.suggestSelection": "first",
	"vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
	"java.errors.incompleteClasspath.severity": "ignore",
	"java.configuration.checkProjectSettingsExclusions": false,
	"javascript.suggest.autoImports": false,
	"terminal.integrated.shell.osx": "/bin/bash",
	"telemetry.enableTelemetry": false,
	"telemetry.enableCrashReporter": false,
	"update.showReleaseNotes": false,
	"update.mode": "manual",
	"editor.formatOnSave": true,
	"go.formatTool": "gofmt",
	"go.docsTool": "guru",
	"go.useLanguageServer": true,
	"go.inferGopath": false,
	"go.buildOnSave": "off",
	"go.delveConfig": {
		"dlvLoadConfig": {
			"followPointers": true,
			"maxVariableRecurse": 1,
			"maxStringLen": 1024,
			"maxArrayValues": 64,
			"maxStructFields": -1
		},
		"debug.openDebug": "openOnDebugBreak",
		"apiVersion": 2,
		"showGlobalVariables": true
	},
	"go.useCodeSnippetsOnFunctionSuggestWithoutType": true,
	"go.useCodeSnippetsOnFunctionSuggest": true,
	"go.autocompleteUnimportedPackages": true,
	"editor.gotoLocation.multiple": "goto",
	"prettier.disableLanguages": ["htm", "html", "yml", "yaml"],
	"prettier.printWidth": 120,
	"prettier.singleQuote": true,
	"prettier.useTabs": true,
	"go.lintOnSave": "workspace",
	"go.testFlags": ["-count=1", "-v"],
	"editor.formatOnType": true
}
```

### `Keybindings.json` shortcuts (VSCode -> Preferences -> Keyboard Shortcuts -> [edit] Keybindings.json)

```json
[
	{
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
	},
	"Default react-native header": {
		"prefix": "gds",
		"body": [
			"/**",
			" * Copyright (c) 2017-Present, Gaurav D. Sharma",
			" * All rights reserved.",
			" *",
			" */",
			"'use strict';"
		]
	},
	"main Go body": {
		"prefix": "f_main",
		"body": ["package main", "", "func main() {", "	$1", "}"]
	}
}
```
