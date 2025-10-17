## 🎯 Objetivo Entender o que é um Sistema de Controle de Versão Distribuído (VCS), como usar o Git localmente para gerenciar o histórico do código e como colaborar em projetos utilizando a plataforma GitHub. 
--- 
## 💾 Módulo 1: Fundamentos do Git e o Fluxo de Trabalho Local 

### 💡 O que é Git? - **Git**: Sistema de Controle de Versão Distribuído (DVCS). 
- **Função**: Rastrear e gerenciar mudanças no código ao longo do tempo. Permite "voltar no tempo" e colaborar sem sobrescrever o trabalho alheio. 
- **Vantagem**: Histórico completo do projeto fica na máquina local (Distribuído). 

### ⚙️ Os Três Estados do Git (Working Tree, Staging Area, Repositório)
1. **Working Tree (Área de Trabalho):** Onde você edita e salva os arquivos.
2. **Staging Area (Área de Preparação):** Onde você seleciona as mudanças que farão parte do próximo *commit*.
3. **Repositório (.git Directory):** Onde o Git armazena permanentemente o histórico do projeto como commits.

| Comando | Ação | Movimento |
| :--- | :--- | :--- |
| `git add <arquivo>` | Adiciona a mudança na Staging Area. | Working Tree -> Staging Area |
| `git commit -m "Mensagem"` | Salva permanentemente as mudanças. | Staging Area -> Repositório |
### 🛠️ Comandos Essenciais Iniciais 
- `git init`: Inicializa um repositório Git na pasta atual. 
- `git config`: Configurações globais (nome de usuário e e-mail). 
- `git config --global user.name "Seu Nome"` 
- `git config --global user.email "seu@email.com"` 
- `git status`: Vê o estado atual da Working Tree e Staging Area. 
- `git log`: Visualiza o histórico de commits. 
---

## ☁️ Módulo 2: O GitHub e a Colaboração Remota 
### 🌐 O que é GitHub? 

- **GitHub**: Plataforma de hospedagem de repositórios Git (Repositorio Remoto) e ambiente social/colaborativo para desenvolvimento de software. 
- **Função**: Backup remoto, trabalho em equipe e exposição de portfólio. ### 🔗 Sincronizando Local e Remoto 
- **Repositório Remoto**: O repositório hospedado no GitHub. 
- **`git remote add origin <URL>`**: Conecta o repositório local ao remoto. 
- **`git push`**: Envia seus commits locais para o repositório remoto (GitHub). 
- **`git pull`**: Baixa novos commits do repositório remoto e tenta integrá-los no seu repositório local. 
- **`git clone <URL>`**: Cria uma cópia local de um repositório remoto existente. 

* **Conexão com HTTP:** **Protocolo de Comunicação Remota:** O Git precisa de um protocolo para transferir dados entre o seu computador (local) e o GitHub (remoto). O protocolo mais comum para isso é o **HTTPS** (o [[HTTP]] criptografado).

### 📝 Recursos Adicionais 

- **README.md**: Arquivo crucial para documentar o projeto. - **.gitignore**: Arquivo que define quais arquivos e pastas o Git deve ignorar (ex: arquivos temporários, senhas, dependências). 
- **Gist**: Ferramenta do GitHub para compartilhar pequenos trechos de código ou arquivos. 

--- 

## 🌳 Módulo 3: Branches, Colaboração e Conflitos 

### 🌿 Branches (Ramificações) 

- **Branch**: Um ponteiro móvel e isolado para um commit. Permite trabalhar em novas funcionalidades sem afetar a linha de código principal (`main` ou `master`). 
- **`git branch <nome>`**: Cria uma nova branch. 
- **`git checkout <nome>` / `git switch <nome>`**: Navega/Muda para a branch especificada. 
- **`git merge <branch>`**: Une o histórico da branch especificada na branch atual. ### 🤝 Fluxo de Colaboração 
- **Fork**: Criar uma cópia de um repositório alheio para sua conta. 
- **Pull Request (PR)**: Solicitação para que as mudanças de sua branch sejam revisadas e integradas (merge) à branch principal de outro repositório. 

### 💥 Conflitos (Merge Conflicts) 

- **Ocorrência**: Acontecem quando duas branches modificam a **mesma linha** de um arquivo, e o Git não consegue decidir qual versão manter. 
- **Resolução**: Abrir o arquivo, editar manualmente para escolher a versão final do código e fazer um novo `git add` e `git commit`. 
- **Simulando Conflitos na IDE (VS Code)**: Prática comum para aprender a resolver conflitos de forma eficiente. 

---

## 🕰️ Módulo 4: Voltando no Tempo (Desfazer Alterações) 

### ⏪ Comandos para Desfazer 

- **`git restore <arquivo>`**: Desfaz alterações na Working Tree (arquivos modificados, mas não adicionados). - **`git reset`**: Comando poderoso usado para: 
- **`git reset HEAD <arquivo>`**: Remove um arquivo da Staging Area (volta para a Working Tree). 
- **`git reset --hard <hash>`**: Move o ponteiro da branch para um commit anterior, **descartando** todas as mudanças posteriores. **(Cuidado!)** 
- **`git reset --soft <hash>`**: Move o ponteiro, mas mantém as mudanças posteriores na Staging Area. 
- **`git revert <hash>`**: Cria um **novo commit** que desfaz as alterações de um commit anterior (mantém o histórico). 

### 🏷️ Tags e Releases 

- **Tags**: Marcadores fixos no histórico do Git, geralmente usados para marcar versões importantes (`v1.0.0`, `v2.0.0`). 
- **Releases (GitHub)**: Ferramenta do GitHub que formaliza uma tag, permitindo anexar binários e notas de lançamento. 

---