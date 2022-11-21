# My Vim Configuration

This configuration has been tested on Ubuntu 20.04.5 LTS with vim 9.0.749

## Plugin list

This is the list of the plugins I use:

- [coc.nvim](https://github.com/neoclide/coc.nvim)
- [fzf](https://github.com/junegunn/fzf)
- [fzf.Vim](https://github.com/junegunn/fzf.vim)
- [indentLine](https://github.com/Yggdroot/indentLine)
- [nerdcommenter](https://github.com/preservim/nerdcommenter)
- [nerdtree](https://github.com/preservim/nerdtree)
- [snipmate](https://github.com/garbas/vim-snipmate)
- [vim-addon-mw-utils](https://github.com/MarcWeber/vim-addon-mw-utils)
- [vim-anyfold](https://github.com/pseewald/vim-anyfold)
- [vim-buftabline](https://github.com/ap/vim-buftabline)
- [vim-powerline](https://github.com/Lokaltog/vim-powerline)
- [vim-repeat](https://github.com/tpope/vim-repeat)
- [vim-surround](https://github.com/tpope/vim-surround)
- [vim-polyglot](https://github.com/sheerun/vim-polyglot)
- [spakup](https://github.com/rstacruz/sparkup)
- [vimspector](https://github.com/puremourning/vimspector)

## Environment variables

Add this line to your .bashrc file will make fzf search for hidden files.

```console
export FZF_DEFAULT_COMMAND="find -L"
```

## Installation

- Clone this repo with all submodules using `git clone --recurse-submodules https://github.com/OGR-67/vim-as-ide.git`
- Copy .vimrc file and .vim folder into your home/ directory
- Check every plugins dependencies

Note: On MacOs, conceal is disable in vim.  
Use macvim instead and open files with mvim command.

## Plugins dependencies

### coc.nvim

#### nodeJS

coc.nvim needs a recent version of nodeJS and npm

```console
curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
npm install -g npm@latest
```

#### yarn

I ran into issue that for installation of some language server I needed to
install yarn.

```console
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update
sudo apt install yarn
```

#### language servers

You'll have to install coc-extension or configure language server for each
language you use

```console
:CocInstall coc-json coc-tsserver coc-sh coc-css coc-html coc-java /
coc-markdownlint coc-psalm coc-pyright
```

Check any error maybe you'll have to install some more dependencies. Feel free
to customize as you like in .vimrc file.

### vimspector

vimspector comes nude. You'll have to install related languages debugger called
gadgets.  

To install a gadget:

- execute this command in vim `:VimspectorInstall`
- followed by `space` and `tab` to see all adapters available.

For node adapter installation, you'll have to downgrade node version to 16.

## My cheat sheet

To get my personal vim cheat sheet taking in count my configuration
Follow [this
link](https://www.canva.com/design/DAFREPtgktk/o03Y-HRZqEwxBryaNzfqNQ/view?utm_content=DAFREPtgktk&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink)
