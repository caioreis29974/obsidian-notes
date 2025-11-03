# ⚔️ Vim: Os Fundamentos do Editor Modal

## 🎯 Objetivo
Dominar a navegação e edição de arquivos de texto diretamente no terminal utilizando o editor Vim, compreendendo seus modos de operação e comandos essenciais para produtividade.

---

## 🧠 Módulo 1: Os Modos de Operação (O Coração do Vim)

O Vim é um editor **modal**, ou seja, seu comportamento muda drasticamente dependendo do modo em que você está:
h

| Modo | Atalho para Acessar | Função Principal |
| :--- | :--- | :--- |
| **Normal** | `Esc` (a partir de qualquer outro modo) | Navegação, comandos de manipulação (copiar, colar, deletar, repetir). |
| **Inserção** | `i`, `a`, `o` | Permite a digitação normal de texto, como em qualquer outro editor. |
| **Visual** | `v` (caractere), `V` (linha), `Ctrl + v` (bloco) | Seleção de texto para comandos em massa (copiar, deletar). |
| **Comando** | `:` | Acesso a funções do editor (salvar, sair, configurações, buscar). |

### 🧭 Navegação Rápida (Modo Normal)
A chave é manter as mãos nas teclas base (`h, j, k, l`):

| Ação | Comando | Ação | Comando |
| :--- | :--- | :--- | :--- |
| **Esquerda** | `h` | **Direita** | `l` |
| **Baixo** | `j` | **Cima** | `k` |
| **Início da Linha** | `0` (zero) | **Fim da Linha** | `$` |
| **Início do Arquivo** | `gg` | **Fim do Arquivo** | `G` |

---

## 🛠️ Módulo 2: Comandos de Edição e Manipulação

### ✏️ Inserção
| Comando | Efeito |
| :--- | :--- |
| `i` | Insere (Insert) antes do cursor. |
| `a` | Adiciona (Append) após o cursor. |
| `o` | Abre uma nova linha abaixo (Open). |
| `O` | Abre uma nova linha acima. |

### ✂️ Exclusão e Cópia (Yank)
- **`d` (Delete):** Comandos de exclusão.
    - `dw`: Deleta a palavra (word).
    - `d$`: Deleta até o fim da linha.
    - `dd`: Deleta a linha inteira.
    - **`D`**: Deleta o resto da linha (equivalente a `d$`).
- **`y` (Yank):** Comandos de cópia.
    - `yw`: Copia a palavra.
    - `yy`: Copia a linha inteira.
- **`p` (Paste):** Cola após o cursor.

### 🔄 Modificação
- **`c` (Change):** Deleta e entra no modo de inserção.
    - `cw`: Altera a palavra.
    - `cc`: Altera a linha inteira.
- **`u`**: Desfaz (Undo) a última alteração.
- **`.` (Ponto):** Repete o último comando de edição.

---

## 💾 Módulo 3: Salvar e Sair (Modo Comando)

Todos os comandos de gerenciamento começam com dois pontos (`:`) no **Modo Comando**.

| Comando | Efeito |
| :--- | :--- |
| `:w` | Salva (Write) o arquivo. |
| `:q` | Sai (Quit) do arquivo. |
| `:wq` ou `:x` | Salva e sai. |
| `:q!` | Sai sem salvar (Ignora alterações). |
| `:w !sudo tee %` | Salva arquivo somente leitura com privilégios de root. |
| `/<texto>` | Busca por uma palavra. Pressione `n` para próxima ocorrência. |

---

## ➡️ A evolução (Neovim)

O Vim é a base da produtividade, mas com o tempo, surgiram limitações em termos de modernização e extensibilidade, especialmente no gerenciamento de plugins e na integração com ferramentas de desenvolvimento (como servidores de linguagem).

Nesse contexto, surgiu o **Neovim**, que é um projeto que **reconstrói o Vim do zero**, mantendo todos os comandos e a filosofia modal, mas otimizado para a era moderna:

* **A Base é a Mesma:** 99% dos comandos e modos que você aprendeu no Vim (Normal, Inserção, Visual, comandos `dd`, `yy`, `:wq`) funcionam perfeitamente no Neovim.
* **A Diferença é a Extensibilidade:** O Neovim permite configurações mais fáceis e poderosas via Lua, além de melhor suporte a features de IDE (como LSP e plugins assíncronos).

Para saber como essa base é transformada em um ambiente de desenvolvimento moderno, confira a próxima nota:

[[Neovim]]