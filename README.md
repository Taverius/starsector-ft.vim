# starsector-ft.vim

Just a simple little `ftdetect` file so vim knows what to do with all the various files used in [Starsector](https://fractalsoftworks.com) mods which are really just JSON.

I think I got them all!

## Installation

### Simple

As normal with your favourite plugin manager

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
Plug 'Taverius/starsector-ft.vim'
```

or using [paq](https://github.com/savq/paq-nvim):

```lua
require("paq") {
    "Taverius/starsector-ft.vim";
}
```

### Lazy

While it is unlikely, there's a number of filetypes this covers, and it might conflict with something else using those extensions.

In that case, you'll want to only load it when needed, like in your project settings, session file, etc.

For example, with a  user command `:Starsector`:

Using [vim-plug](https://github.com/junegunn/vim-plug):

```vim
Plug 'Taverius/starsector-ft.vim', { 'on': [] }
```

and then somewhere after `call plug#end()` 

```vim
command! Starsector call plug#load('starsector-ft.vim)
```

or using [paq](https://github.com/savq/paq-nvim):

```lua
require("paq") {
    { "Taverius/starsector-ft.vim", opt = true };
}
vim.api.nvim_create_user_command(
	'Starsector',
	vim.cmd.packadd('starsector-ft.vim'),
	{ bang = true }
)
```

