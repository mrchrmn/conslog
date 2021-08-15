# Conslog - for a better console.log() experience

_Conslog_ is a collection of VSCode snippets that add or remove `console.log`s to and from selected code.

## Features

### Log selection

> Prefix: cl
>
> Keyboard shortcut: Alt-Shift-C

The idea behind this snippet was to make it easier to log the test cases that are sometimes provided with coding problems.

It wraps the selection in `console.log`s. But only the part of the selection until the first semicolon is getting wrapped, the rest remains as is.

If multiple lines are selected, each line is treated like an individual selection, adding multiple `console.log`s.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogLogSelection.gif?raw=true)

### Undo _log selection_

> Prefix: ucl
>
> Keyboard shortcut: Alt-Shift-U

Removes `console.log` from selected lines, unwrapping the argument. Reverts the effect of _log selection_.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogUndoLogSelection.gif?raw=true)

### Log variable

> Prefix: clv
>
> Keyboard shortcut: Alt-Shift-L

If you are a fan of `console.log` debugging, this feature is for you. Enter the variable name, and then TAB to the end of the line. The variable name and value will be logged in a nicely formatted way.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogLogVariable.gif?raw=true)

### Delete console logs

> Prefix: dcl <- changed!
>
> Keyboard shortcut: Alt-Shift-D

So, if you _really_ are indeed a fan of `console.log` debugging, chances are that your code now has plenty of lines temporarily logging variables. Get rid of them in one go with this snippet.

It deletes every line that starts with `console.log` from the selection, so be careful. Note: This is not the reverse of _Log selection_.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogDeleteConsoleLogs.gif?raw=true)

## Known issues

- _Log selection_ does not work properly if the test cases include the characters `/` or `;`, or line breaks.
- Spaces at the beginning of selected lines are included in the `console.log` parentheses.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslogIssues.gif?raw=true)

I'm working on it.