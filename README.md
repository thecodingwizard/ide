Note: To fix https://github.com/FirebaseExtended/firepad/issues/315, a very questionable change was done:

Replace

var n=this.configurationService.getValue("files.eol",{overrideIdentifier:t,resource:e});return n&&"auto"!==n?n:d.isLinux||d.isMacintosh?"\n":"\r\n"

with

return '\n';

in `js/monaco-editor/min/vs/editor/editor.main.js`