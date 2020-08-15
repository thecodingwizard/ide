# Realtime Collaborative IDE

A proof-of-concept realtime collaborative IDE with code execution and input/output. Designed primarily for Competitive Programming.

IDE and code execution taken from [Judge0 IDE](https://ide.judge0.com/). Realtime collaboration with [Firepad](https://firepad.io/).

---

Note: To fix https://github.com/FirebaseExtended/firepad/issues/315, a very questionable change was done:

Replace

```javascript
var n=this.configurationService.getValue("files.eol",{overrideIdentifier:t,resource:e});return n&&"auto"!==n?n:d.isLinux||d.isMacintosh?"\n":"\r\n"
```

with

```javascript
return '\n';
```

in `third_party/monaco-editor/min/vs/editor/editor.main.js`