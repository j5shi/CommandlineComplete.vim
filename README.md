# Introduction

This plugin completes keywords in Vim `Cmdline mode` (a.k.a. `Command-line mode`).

# Install

If you are using a Vim plugin management tool, for instance, Pathogen, then just clone this
repository to './bundle'

    cd bundle
    git clone https://github.com/j5shi/CommandlineComplete.vim

# Usage

When editing the command-line, press `<C-j>` or `<C-k>` to complete the word before the cursor with the
matched keywords found in the current buffer and $MYVIMRC (not supported if Vim compiled without
`+python` support), if any.

If you want to use other keys instead of default `<C-j>` `<C-k>` to trigger the completion, please
define them in `$MYVIMRC` as follows:

    cmap <c-p> <Plug>CmdlineCompleteBackward
    cmap <c-n> <Plug>CmdlineCompleteForward

This will use `<C-p>` `<C-n>` to search backward and forward.

Without python, the complete speed will be a bit slow with large file (e.g. > 100K). Compile your
vim with python is recommended.

