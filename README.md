# Dim

**dim** is a lua plugin for neovim to dim the unused variables and functions using lsp and treesitter.

<video src = "https://user-images.githubusercontent.com/79555780/157270883-da3120c8-b8b2-4036-8063-3b5ce10d4d88.mp4"></video>

## ✨ Features

- **dim** unused variables and functions using lsp and treesitter.

## ⚡️ Requirements

- Neovim >= 0.6.0

## 📦 Installation

Install the plugin with your preferred package manager:

### [lazy](https://github.com/folke/lazy.nvim) 

```lua
-- Lua
{
  "0oAstro/dim.lua",
  dependencies = { "nvim-treesitter/nvim-treesitter", "neovim/nvim-lspconfig" },
},
```

### [packer](https://github.com/wbthomason/packer.nvim)

```lua
-- Lua
use {
  "0oAstro/dim.lua",
  requires = { "nvim-treesitter/nvim-treesitter", "neovim/nvim-lspconfig" },
  config = function()
    require('dim').setup({})
  end
}
```

### [vim-plug](https://github.com/junegunn/vim-plug)

```vim
" Vim Script
Plug 'neovim/nvim-lspconfig'
Plug 'nvim-treesitter/nvim-treesitter'
Plug '0oAstro/dim.lua'

lua require('dim').setup({})
```

## ⚙️ Configuratioon

Dim comes with the following defaults:

```lua
{
  disable_lsp_decorations = false, -- disable virt text and underline by lsp on unused vars and functions
  alpha = 0.4
}
```

## Tested LSPs

| LSPs          | Status |
| ------------- | ------ |
| tsserver      | ✔️     |
| sumneko_lua   | ✔️     |
| rust_analyzer | ✔️     |
| jdtls         | ✔️     |
