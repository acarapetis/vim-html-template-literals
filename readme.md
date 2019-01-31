Syntax highlighting and indentation for
[**lit-html**](https://github.com/Polymer/lit-html). Largely inspired by
[**vim-jsx**](https://github.com/mxw/vim-jsx).

This fork adds support for lit-html templates in typescript files. **NOTE**: looks like typescript is now supported by the original version, so don't install my hacky nonsense!

## Supported Syntaxes inside ``html`...` ``
- HTML (including CSS embedded in `<style>` tags)
- JavaScript string interpolation (`${...}`)
- nested templates (``` html`${html`${}`}` ```)

## Installation

This plugin requires
[**vim-javascript**](https://github.com/pangloss/vim-javascript) 
for javascript or 
[**typescript-vim**](https://github.com/leafgarland/typescript-vim)
for typescript. If you use
[**vim-plug**](https://github.com/junegunn/vim-plug) for package management,
installation looks like this:

```vim
Plug 'acarapetis/experimental-lit-html-vim'
Plug 'pangloss/vim-javascript'
```

Note: it's generally a good idea to have `let g:html_indent_style1 = "inc"` in
your vimrc for reasonable indentation of `<style>` tags. See `:help
html-indenting`.

## Known Issues

- The indentation logic still has some kinks.
  <!-- The boundaries between js and html (``html`...` `` and `${...}`) are
  rather tricky. -->
- This plugin conflicts a bit with vim-jsx. Having both installed
  simultaneously may result in undesired indentation behaviors.
