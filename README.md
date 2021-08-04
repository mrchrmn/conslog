# Conslog - for a better console.log() experience.

_Conslog_ is a collection of VSCode snippets that either add or remove `console.logs()` to selected code. 

## Features

### Log selection

> Prefix: cl
>
> Keyboard shortcut: Alt-Shift-C

The idea behind this snippet was to make it easier to log the test cases that are sometimes provided with coding problems.

It wraps the selection in `console.logs()`. But only the part of the selection until the first semicolon is getting wrapped, the rest remains as is. 

If multiple lines are selected, each line is treated like an individual selection, adding multiple `console.log()`s.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslog11.gif?raw=true)

### Clear console logs

> Prefix: ccl
>
> Keyboard shortcut: Alt-Shift-D

If you are a fan of `console.log()` debugging, chances are that your code has plenty of lines temporarily logging variables. Get rid of them in one go with this snippet. 

It deletes every line that starts with `console.log` from the selection. Note: It is not the reverse of _Log selection_.

![GIF animation showing Conslog at work](https://github.com/mrchrmn/conslog/blob/main/images/conslog12.gif?raw=true)