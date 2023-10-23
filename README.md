# synthwave-black-neon
Black based remix on [theme for MS Visual Studio Code synthwave84](https://marketplace.visualstudio.com/items?itemName=RobbOwen.synthwave-vscode) by [robbOwens](https://github.com/robb0wen)

Here is what I've got with this:
![preview](https://github.com/vadym4che/synthwave-black-neon/blob/main/screenshot.png)

# FIX SUBTLE BACKGROUND PROBLEM:

1. Find the file called "neondreams.js" located at this path (or something similar):

<b><i>
'~\AppData\Local\Programs\Microsoft VS Code\resources\app\out\vs\code\electron-sandbox\workbench\neondreams.js
</i><b>

2. Replace it with the file attached in the folder ".vscode--extensions--robbowen.synthwave--vscode-0.1.15" OR fix it manually:
- Locate the 98th line of code that affects your GUTTER color
- Add the following code snippet:
```css
/* Add the subtle gradient to the editor background */
.monaco-editor {
  background-color: transparent !important;
  background-image: linear-gradient(to bottom, #000000 75%, #000000);
  background-size: auto 100vh;
  background-position: top;
  background-repeat: no-repeat;
}
```

Here my sreen view is:
![preview](https://github.com/vadym4che/synthwave-black-neon/blob/main/fixed.png)

ALSO, YOU CAN USE MY TOTAL BLACK NEON GLOWED THEME .json file for this purpose. Replace the file(s) at the following path:

```shell
~\.vscode\extensions\robbowen.synthwave-vscode-0.1.15\
```

***

I want to express my gratitude for the post that brought us closer to a real working solution for this problem. You can refer to it [here](https://github.com/robb0wen/synthwave-vscode/issues/199)