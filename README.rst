Overview
--------

Vim script to help moving around in larger Python source files. It displays
current class, method or function the cursor is placed in in the status line
for every python file.  It's more clever than Yegappan Lakshmanan's taglist.vim
because it takes into account indentation and comments to determine what tag the
cursor is placed on and from version 0.80 doesn't need exuberant ctags utility.

This is a fork of http://www.vim.org/scripts/script.php?script_id=435

Needs Vim built with Python support.


Installation
------------

I recommend `Vundle <https://github.com/gmarik/vundle>`_, `pathogen
<https://github.com/tpope/vim-pathogen>`_ or `Vim Addon Manager
<https://github.com/MarcWeber/vim-addon-manager>`_.  E.g. with Vundle do ::

  :PluginInstall mgedmin/pythonhelper.vim

Manual installation:

- copy ``plugin/pythonhelper.vim`` to ``~/.vim/plugin/``.
- copy ``pythonx/pythonhelper.py`` to ``~/.vim/pythonx/``.


Configuration
-------------

Add ``%{TagInStatusLine()}`` to your 'statusline', e.g. ::

  set statusline=%<%f\ %h%m%r\ %1*%{TagInStatusLine()}%*%=%-14.(%l,%c%V%)\ %P


Alternatives
------------

`Tagbar <https://github.com/majutsushi/tagbar>`_ looks like a better-maintained
alternative that supports not just Python, but other languages as well.


Copyright
---------

``pythonhelper.vim`` was written by Michal Vitecek.
Licence: ???
