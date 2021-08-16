# Conslog - for a better console.log() experience

_Conslog_ is a collection of VSCode snippets that add or remove `console.log`s to and from selected code.

The idea behind it was to make it easier to log the test cases that are sometimes provided with coding problems, eg. on Codewars or Leetcode, for example like this:
```js
mySolution(testCase); // => true
mySolution("testCase"); // => "Casetest"
```

## Features

### Log selection

> Prefix: cl
>
> Keyboard shortcut: Alt-Shift-C

It wraps the selection in `console.log`s. But only the part of the selection **until the first semicolon** is getting wrapped, the rest remains as is.

If multiple lines are selected, each line is treated like an individual selection, adding multiple `console.log`s. 

Skips empty lines and comment lines.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogLogSelection.gif?raw=true)

#### Limitations

```js
mySolution("My favourite symbol is the ;");
```
If the selection includes semicolons, use _log lines to last semicolon_ instead.

```js
mySolution(testCase) // What? No semicolon?
```
If the code doesn't end in a semicolon but in a closing bracket _AND_ is followed by a comment on the same line, use use _log lines to last closed bracket_. 

### Log lines to last semicolon

> Prefix: lls
>
> Keyboard shortcut: Alt-Shift-,

Like _log selection_ but wraps until the last semicolon instead. 

#### Limitations

Does not work if the code is followed by a comment on the same line that includes a semicolon:
```js
mySolution("My favourite symbol is the ;"); // Comment with ; semicolon
```

### Log lines to last closing bracket

> Prefix: llb
>
> Keyboard shortcut: Alt-Shift-B

#### Limitations

Does not work if the code is followed by a comment on the same line that includes a closing bracket:
```js
mySolution(testCase) // Comment with ) closing bracket
```

### Undo logs

> Prefix: ucl
>
> Keyboard shortcut: Alt-Shift-U

Removes `console.log` from selected lines, unwrapping the argument. Reverts the effect of _log lines ..._.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogUndoLogSelection.gif?raw=true)

### Log variable

> Prefix: clv
>
> Keyboard shortcut: Alt-Shift-L

If you are a fan of `console.log` debugging, this feature is for you. Enter the variable name, and then TAB to the end of the line. The variable name and value will be logged in a nicely formatted way.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogLogVariable.gif?raw=true)

### Delete console logs

> Prefix: dcl
>
> Keyboard shortcut: Alt-Shift-D

So, if you _really_ are indeed a fan of `console.log` debugging, chances are that your code now has plenty of lines temporarily logging variables. Get rid of them in one go with this snippet.

It deletes every line that starts with `console.log` from the selection, so be careful. Note: This is not the reverse of _Log selection_.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogDeleteConsoleLogs.gif?raw=true)

## Known Issues

See _Limitations_ for individual features.