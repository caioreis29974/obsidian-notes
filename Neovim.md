# ✨ Neovim: O Editor Moderno e Extensível

## 🎯 Objetivo
Entender o que diferencia o Neovim do Vim tradicional e como configurá-lo para se tornar um ambiente de desenvolvimento completo (IDE-like) usando a linguagem Lua.

---

## ⚙️ Módulo 1: O Que é Neovim (nvim)?

O Neovim é uma reescrita do Vim, focada em modernidade, extensibilidade e usabilidade:

- **Filosofia:** Melhorar a experiência do usuário, facilitar a manutenção do código e, principalmente, permitir que plugins funcionem de forma assíncrona.
- **Configuração em Lua:** Enquanto o Vim usa o Vimscript, o Neovim incentiva a configuração utilizando **Lua**, uma linguagem leve e rápida, facilitando a criação de plugins mais complexos e eficientes.
- **Base de Comandos:** Mantém 100% dos comandos do [[Vim]]. Se você sabe usar o Vim, sabe usar o Neovim.

---

## 🧩 Módulo 2: Extensibilidade e Plugins

A principal força do Neovim é a comunidade e o ecossistema de plugins.

### 📦 Gerenciamento de Plugins
- **Package Managers:** O Neovim requer um gerenciador para organizar, instalar e atualizar plugins. (Ex: `packer.nvim`, `lazy.nvim`).
- **Configuração:** O arquivo principal de configuração é `init.lua`, que substitui o antigo `.vimrc`.

### ⚡ Plugins Essenciais para Desenvolvimento
- **LSP (Language Server Protocol):** O Neovim tem suporte nativo a Servidores de Linguagem, que fornecem funcionalidades avançadas de IDE:
    - Autocompletar inteligente (ex: com `nvim-cmp`).
    - Pular para definição.
    - Refatoração de código.
    - Detecção de erros em tempo real.
- **Treesitter:** Uma engine de parseamento de código que melhora o *syntax highlighting* e a manipulação de blocos de código (ex: alterar um bloco inteiro de um `if`).
- **Fuzzy Finder:** Plugins como `Telescope` ou `fzf` melhoram drasticamente a navegação e busca de arquivos no projeto.
- **Barra de Status:** Plugins como `lualine` ou `airline` criam barras de status ricas em informação.

---

## 💡 Módulo 3: Neovim como IDE (Ambiente de Desenvolvimento)

O objetivo da comunidade Neovim é transformar o editor em uma IDE completa e minimalista:

- **Terminal Integrado:** Permite rodar comandos e testes sem sair do editor.
- **Mapeamentos Personalizados (Keymaps):** Configurar atalhos específicos para tarefas de desenvolvimento (ex: rodar testes com `<leader>t`).
- **Navegação de Projeto:** Uso de painéis (buffers, janelas e tabs) para gerenciar vários arquivos abertos, assim como em um IDE moderno.

---