# CRIADOR DE PROJETOS — Claude Code no VS Code

Ensina o Claude Code a criar projetos completos automaticamente quando você pede.

Você diz "quero criar um app de controle financeiro" — e ele cria a pasta, os arquivos, conecta ao GitHub e organiza tudo. Sem você precisar fazer nada manualmente.

---

## O que você precisa ter instalado antes

Antes de instalar, confirme que você já tem estes 3 programas:

**1. VS Code com a extensão Claude Code**
A extensão da Anthropic dentro do VS Code. É com ela que você conversa com o Claude.

**2. Node.js**
Necessário para o Claude Code funcionar. Baixe em: https://nodejs.org (versão LTS)

**3. GitHub CLI (`gh`)**
Ferramenta de terminal que permite criar repositórios no GitHub automaticamente.

Para verificar se já está instalado, abra o Terminal e digite:
```
gh --version
```
Se aparecer um número de versão, está instalado. Se não aparecer, instale com:
```
brew install gh
```
Depois, conecte ao GitHub (só precisa fazer uma vez):
```
gh auth login
```
Siga as instruções na tela. Escolha GitHub.com → HTTPS → autentique com o navegador.

---

## Como baixar e instalar

### Passo 1 — Baixar este repositório

No Terminal, cole este comando e pressione Enter:

```
cd ~/Downloads && git clone https://github.com/Hackerdomarketing/criador-de-projetos-claude-code-no-vscode.git
```

Isso vai criar uma pasta chamada `criador-de-projetos-claude-code-no-vscode` nos seus Downloads.

### Passo 2 — Abrir a pasta no Terminal

```
cd ~/Downloads/criador-de-projetos-claude-code-no-vscode
```

### Passo 3 — Rodar o instalador

```
bash instalar.sh
```

Pronto. O instalador vai:
- Criar a pasta `~/Documents/VSCODE/CRIADOR-DE-PROJETOS/` com todos os arquivos
- Criar o arquivo `~/Documents/VSCODE/CLAUDE.md` com as instruções do sistema (se você ainda não tiver)

---

## Como usar depois de instalar

**Abra o VS Code** na pasta `~/Documents/VSCODE/` — esta é a pasta onde todos os seus projetos ficam.

**Abra o Claude Code** (a extensão da Anthropic no VS Code).

**Diga qualquer uma dessas frases:**

> "criar um projeto..."
> "novo projeto..."
> "quero criar..."
> "faz um app..."
> "preciso de um sistema..."
> "monta um..."

O Claude vai perguntar algumas coisas (o que o projeto faz, qual tecnologia, etc.) e depois criar tudo automaticamente — pasta, arquivos de memória, código inicial, Git e repositório privado no GitHub.

---

## O que é criado em cada projeto

Toda vez que você pede um projeto novo, o Claude cria estes arquivos automaticamente:

| Arquivo | Para que serve |
|---------|---------------|
| `ARQUITETURA-MENTAL.md` | Como o Claude pensa e processa informação neste projeto |
| `CLAUDE.md` | Instruções do projeto — memória, comunicação, nomenclatura |
| `.memoria-ultimas-tarefas.md` | As 3 últimas tarefas feitas (o Claude lê isso primeiro a cada sessão) |
| `.memoria-do-dia.md` | Registro cronológico do que foi feito hoje |
| `.memoria-projeto.md` | Memória completa do projeto |
| `README.md` | Documentação básica do projeto |
| `.gitignore` | Lista de arquivos que não vão para o GitHub |

---

## Dúvidas frequentes

**Preciso abrir o VS Code em alguma pasta específica?**
Sim. Abra o VS Code em `~/Documents/VSCODE/` — é onde os projetos são criados. Se abrir em outra pasta, o sistema ainda funciona, mas os projetos serão criados lá.

**O que acontece se eu já tiver um CLAUDE.md?**
O instalador não apaga o que você já tem. Você pode copiar manualmente o conteúdo de `templates/CLAUDE.md` para o seu CLAUDE.md existente.

**Funciona só no Mac?**
Por enquanto sim. O caminho `~/Documents/VSCODE/` é padrão no macOS. No Windows ou Linux, os caminhos são diferentes.

**O repositório criado no GitHub é privado ou público?**
Sempre privado. Só você vê.
