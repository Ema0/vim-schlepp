VIM-Schlepp
===========
Vim plugin to allow the movement of lines (or blocks) of text around easily.
Inspired by Damian Conway's DragVisuals from his
[More Instantly Better Vim](http://programming.oreilly.com/2013/10/more-instantly-better-vim.html)

What it Does
============
Schlepp lets you move a highlighted (visual mode) section of text around,
respecting other text around it.

Block and Line Selections work now.

Setup
=====
Add the following mappings to your vimrc, feel free to change from using the
arrows to something more to your vim usage.

```vimscript
vmap <unique> <up>    <Plug>SchleppUp
vmap <unique> <down>  <Plug>SchleppDown
vmap <unique> <left>  <Plug>SchleppLeft
vmap <unique> <right> <Plug>SchleppRight
```

When moving text left, Schlepp by default does not allow you to move left if any
text is all the way left. eg
```text
All the way left text cannot be moved left
    Even though this text can be
```
To allow the 'Squishing' of text add this line to your vimrc
```vimscript
let g:Schlepp#AllowSquishing = 1
```
