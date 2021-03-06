vim-header
==========
Easily adds brief author info and license headers

Install
-------
Preferred installation method is [Pathogen](https://github.com/tpope/vim-pathogen)
```sh
cd ~/.vim/bundle
git clone https://github.com/alpertuna/vim-header
```
Or you can use your own way

Usage
-----
This is a general usage example.
You can add these lines into your `.vimrc`
```vim
let g:header_field_author = 'Your Name'
let g:header_field_author_email = 'your@mail'
map <F4> :AddHeader<CR>
```
Pressing `F4` in normal mode will add a brief author information at the top of your buffer.

Examples
--------
For example, when you open a file named `start.sh` and press `F4` after above settings, plugin will add these lines at the top of your buffer
```sh
#!/bin/bash
# File: start.sh
# Author: Your Name <your@mail>
# Date: 13.03.2016
# Last Modified Date: 13.03.2016
# Last Modified By: Your Name <your@mail>
```
or for a file named `index.php`
```php
<?php
/*
 * File: index.php
 * @author: Your Name <your@mail>
 * Date: 13.03.2016
 * Last Modified Date: 13.03.2016
 * Last Modified By: Your Name <your@mail>
 */
```
Commands
--------
Adding Brief Headers

- `:AddHeader` Adds brief author information or updates if exists
- `:AddMinHeader` Adds minified version of author information

Adding Lincenses

- `:AddMITLicense` Adds MIT License with author info
- `:AddApacheLicense` Adds Apache License with author info
- `:AddGNULicense` Adds GNU License with author info

Settings
--------
These settings are for your `.vimrc`
```vim
let g:header_field_filename = 0
```
It disables to add filename line in header. Default is 1.
```vim
let g:header_field_author = 'Your Name'
```
It adds your name as author. Default is ''. Empty string means to disable adding it.
```vim
let g:header_field_author_email = 'your@mail'
```
It adds your email after author name with surrounding `<` `>` chars. If you don't define your author name, defined email also won't be shown. Default is ''. Empty string means to disable adding it.
```vim
let g:header_field_timestamp = 0
```
It disables to add creating date line. Default is 1.
```vim
let g:header_field_modified_timestamp = 0
```
It disables to add modified date line. Default is 1.
```vim
let g:header_field_modified_by = 0
```
It disables to add modified author line. Default is 1. Likewise the author name line, if you don't define your author name, this line won't be shown. If your email is defined together with your name, your email will be appended after your author name.
```vim
let g:header_field_timestamp_format = '%d.%m.%Y'
```
It sets timestamp format for your locale. Default is '%d.%m.%Y'.
```vim
let g:header_auto_add_header = 0
```
It disables to add header automatically. Default is 1.

It sets cfg's filetype comment character as this filetype supports multiple set of comment characters (`;`, `//`, `#`, ...). Default is `#`.
```vim
let g:header_cfg_comment_char = ';'
```

This option sets the range from which vim-header will search for required
headers (ones sets in global options) to determinate if it should update
existing headers or add new ones.
```vim
let g:header_max_size = 20
```
This options is used to prevent text replacement if your file contains text
matching headers (for instance `File:`). Default is 7. See [#20](https://github.com/alpertuna/vim-header/issues/20#issuecomment-319127330) for more explanations.

Support
-------
Supported filetypes are;

- asm
- c
- cfg
- clojure
- cpp
- cs
- css
- elixir
- erlang
- go
- groovy
- haskel
- java
- javascript
- jsx
- lisp
- lua
- matlab/octave
- ocaml
- php
- perl
- plaintex
- pug
- python
- ruby
- rust
- sass
- scala
- scheme
- sh
- tmux
- vim
- xdefaults

And licenses are;

- MIT
- Apache
- GNU

If you want more filetypes or licenses, you can open issues or provide any improvements by pull requests on [alpertuna/vim-header](https://github.com/alpertuna/vim-header). Also you can correct my English on README file or at comments in source code.

### Thanks to Contributors
[Contributors List](https://github.com/alpertuna/vim-header/graphs/contributors)
