# CRIADOR DE PROJETOS para Claude Code no VS Code

---

## O que é isso?

Imagine que você quer contratar um assistente para organizar seus projetos de programação. Toda vez que você dissesse "quero criar um projeto de controle financeiro", ele imediatamente criaria uma pasta organizada, separaria os arquivos nos lugares certos, conectaria tudo ao GitHub (o lugar onde programadores guardam os projetos na nuvem) e deixaria tudo pronto para começar a trabalhar.

**É exatamente isso que este sistema faz.**

Depois de instalar, você abre o Claude Code no VS Code, diz algo como *"criar um projeto de lista de tarefas"*, e o Claude organiza tudo automaticamente. Você não precisa criar pasta, não precisa configurar nada, não precisa lembrar de fazer backup. Ele faz por você.

---

## Antes de começar — o que você precisa ter no computador

Antes de instalar este sistema, você precisa ter 3 coisas no seu computador. Vamos verificar uma por uma.

---

### Coisa 1 — VS Code com a extensão Claude Code

O **VS Code** é um programa para escrever código — é como um bloco de notas, mas muito mais esperto. Dentro do VS Code, existe uma extensão (um complemento, como um plugin) chamada **Claude Code**, feita pela Anthropic, que é a empresa do Claude.

Quando o VS Code está aberto com essa extensão, você tem uma janelinha onde pode conversar com o Claude e pedir para ele criar arquivos, escrever código, organizar pastas — tudo ali dentro.

Se você já usa o Claude Code no VS Code, pode ir para a próxima coisa. Se não tiver ainda, instale o VS Code em https://code.visualstudio.com e depois instale a extensão Claude Code dentro do VS Code, na aba de extensões (o ícone de 4 quadradinhos na barra lateral esquerda).

---

### Coisa 2 — Node.js

O **Node.js** é um programa que o Claude Code precisa para funcionar nos bastidores. Você não vai usar ele diretamente, mas sem ele, o Claude Code não roda.

**Para verificar se você já tem:**

Abra o Terminal (veja abaixo como abrir) e digite exatamente isso, depois pressione Enter:

```
node --version
```

Se aparecer algo como `v20.11.0` ou qualquer número, você já tem. Pode pular para a Coisa 3.

Se aparecer uma mensagem de erro dizendo que o comando não foi encontrado, você precisa instalar. Acesse https://nodejs.org, clique no botão grande que diz **LTS**, baixe e instale normalmente como qualquer programa no Mac.

---

### Como abrir o Terminal

O Terminal é um programa que vem instalado em todos os Macs. É uma janela preta (ou branca, dependendo das suas configurações) onde você digita comandos de texto.

Para abrir: pressione **Command + Espaço**, digite **Terminal** e pressione Enter. Vai abrir uma janela onde você digita.

Não se assuste com a aparência. Você só vai precisar copiar e colar os comandos que estão neste guia. É mais simples do que parece.

---

### Coisa 3 — GitHub CLI (a ferramenta para criar repositórios automaticamente)

O **GitHub** é como um Google Drive para projetos de programação. É onde os projetos ficam guardados na nuvem, com todo o histórico de mudanças. Quando o Claude cria um projeto pra você, ele automaticamente cria um repositório privado no GitHub para guardar aquele projeto.

Para fazer isso automaticamente, você precisa de uma ferramenta chamada **GitHub CLI** — é um programa de linha de comando que se comunica com o GitHub.

**Para verificar se você já tem:**

No Terminal, digite:

```
gh --version
```

Se aparecer algo como `gh version 2.40.0`, você já tem. Pode ir para a próxima etapa.

**Se não aparecer, instale assim:**

Primeiro, você precisa do Homebrew — um instalador de programas para Mac. Para verificar se você tem:

```
brew --version
```

Se não tiver o Homebrew, instale com este comando (copie tudo, cole no Terminal, pressione Enter):

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Aguarde terminar. Depois, instale o GitHub CLI:

```
brew install gh
```

**Depois de instalar, conecte ao GitHub (só precisa fazer isso uma vez):**

```
gh auth login
```

Vai aparecer um menu de opções no terminal. Use as setas do teclado para escolher e Enter para confirmar. Escolha:
- **GitHub.com** (não GitHub Enterprise)
- **HTTPS**
- **Login with a web browser** (autenticar com o navegador)

O terminal vai mostrar um código de 8 letras e abrir o GitHub no seu navegador. Cole o código lá, faça login na sua conta do GitHub, e pronto. Você vai ver uma mensagem de confirmação no terminal.

Se ainda não tem conta no GitHub, crie uma grátis em https://github.com antes de fazer esse passo.

---

## Instalando o sistema

Agora sim. Com as 3 coisas acima verificadas, vamos instalar.

### Passo 1 — Baixar os arquivos do sistema

Abra o Terminal e cole este comando inteiro, depois pressione Enter:

```
cd ~/Downloads && git clone https://github.com/Hackerdomarketing/criador-de-projetos-claude-code-no-vscode.git
```

O que acontece: o terminal vai baixar uma pasta chamada `criador-de-projetos-claude-code-no-vscode` dentro dos seus Downloads. Você vai ver algumas linhas de texto passando — é normal, é o download acontecendo.

### Passo 2 — Entrar na pasta baixada

```
cd ~/Downloads/criador-de-projetos-claude-code-no-vscode
```

### Passo 3 — Rodar o instalador

```
bash instalar.sh
```

O que acontece: o instalador vai criar uma pasta chamada `CRIADOR-DE-PROJETOS` dentro de `~/Documents/VSCODE/` — que é onde o VS Code guarda seus projetos. Ele também vai criar um arquivo chamado `CLAUDE.md` que contém as instruções que o Claude precisa ler para saber como criar projetos para você.

Você vai ver mensagens como:

```
═══════════════════════════════════════
  Instalando o Criador de Projetos...
═══════════════════════════════════════

Copiando arquivos...
✓ CRIADOR-DE-PROJETOS instalado em /Users/[seu nome]/Documents/VSCODE/
✓ CLAUDE.md criado com as regras de memória, nomenclatura e comunicação

═══════════════════════════════════════
  Instalação concluída!
═══════════════════════════════════════
```

Se aparecer isso, deu certo. Você pode fechar o terminal.

---

## Usando depois de instalar

### Onde abrir o VS Code

Abra o VS Code na pasta `~/Documents/VSCODE/`. Essa é a pasta onde todos os seus projetos ficam — e é lá que o Claude vai criar as pastas quando você pedir.

Para abrir nela: no VS Code, vá em **File → Open Folder** e navegue até Documents → VSCODE.

### Como abrir o Claude Code no VS Code

Na barra lateral do VS Code, procure o ícone do Claude (parece um "A" estilizado ou um logo da Anthropic). Clique nele. Uma janela de conversa vai abrir do lado.

### O que dizer para criar um projeto

Simplesmente descreva o que você quer criar. Você pode usar frases como:

---

*"Criar um projeto de lista de tarefas em Python"*

*"Novo projeto: um site de portfólio com Next.js"*

*"Quero criar um sistema de controle de estoque"*

*"Faz um app de calculadora de gastos"*

*"Preciso de um bot de WhatsApp que responde mensagens automáticas"*

*"Monta um sistema de envio de emails automáticos"*

---

O Claude vai perguntar algumas coisas para entender melhor o que você quer — o que o projeto precisa fazer, qual tecnologia usar, se precisa de alguma integração com outros serviços. Responda normalmente, como se fosse uma conversa.

Depois das perguntas, ele vai criar tudo automaticamente:
- A pasta do projeto
- Os arquivos de memória (para ele lembrar o que foi feito)
- O código inicial
- A conexão com o Git (o sistema de controle de versões)
- O repositório privado no GitHub

E vai te mostrar o link do repositório no GitHub quando terminar.

---

## O que é criado em cada projeto

Toda vez que você pede um projeto novo, o Claude cria estes arquivos dentro de uma pasta com o nome do projeto:

| Arquivo | Para que serve |
|---------|----------------|
| `ARQUITETURA-MENTAL.md` | Define como o Claude vai pensar e se comportar neste projeto específico. Ele lê isso sempre. |
| `CLAUDE.md` | As instruções do projeto: como usar a memória, como nomear arquivos, como se comunicar com você. |
| `.memoria-ultimas-tarefas.md` | As 3 últimas tarefas que foram feitas. O Claude lê isso primeiro ao abrir o projeto — para lembrar onde parou. |
| `.memoria-do-dia.md` | Um registro cronológico de tudo que foi feito hoje neste projeto. |
| `.memoria-projeto.md` | A memória completa do projeto: decisões tomadas, arquitetura, histórico. O Claude lê isso quando precisa de contexto mais profundo. |
| `README.md` | Um documento explicando o que o projeto faz e como usar. |
| `.gitignore` | Uma lista de arquivos que não devem ir para o GitHub (senhas, arquivos temporários, etc.). |

---

## Perguntas frequentes

**Eu preciso abrir o VS Code em uma pasta específica para o sistema funcionar?**

Sim. Abra o VS Code sempre em `~/Documents/VSCODE/`. É nessa pasta que o Claude vai criar os seus projetos. Se você abrir o VS Code em outra pasta, o projeto vai ser criado lá, o que pode causar confusão.

**E se eu já tiver um arquivo CLAUDE.md na minha pasta do VS Code?**

O instalador não apaga nem modifica o que você já tem. Ele só cria um CLAUDE.md novo se não existir nenhum. Se você já tem um, o instalador vai avisar e não vai mexer nele. Se quiser adicionar as instruções do sistema ao seu CLAUDE.md existente, você pode copiar o conteúdo do arquivo `CRIADOR-DE-PROJETOS/templates/CLAUDE.md` e colar no seu.

**O repositório que o Claude cria no GitHub é privado ou público?**

Sempre privado. Só você tem acesso. Ninguém mais consegue ver.

**Posso usar isso em Windows ou Linux?**

Por enquanto, o sistema foi feito para macOS. Os caminhos de pasta usados (`~/Documents/VSCODE/`) são específicos do Mac. No Windows ou Linux, os caminhos são diferentes e você precisaria adaptá-los manualmente.

**O que é o `~` que aparece nos caminhos de pasta?**

O `~` é uma abreviação para a pasta do seu usuário no Mac. Por exemplo, se seu nome de usuário é `joao`, então `~/Documents/VSCODE/` significa `/Users/joao/Documents/VSCODE/`. É só um atalho para não ter que escrever o nome completo.

**Posso desinstalar se não gostar?**

Sim. Basta deletar a pasta `~/Documents/VSCODE/CRIADOR-DE-PROJETOS/` e o arquivo `~/Documents/VSCODE/CLAUDE.md`. Nada mais foi modificado no seu computador.
