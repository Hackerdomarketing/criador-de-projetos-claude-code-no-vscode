# CRIADOR DE PROJETOS para Claude Code no VS Code

---

## O que é isso?

Imagine que você quer contratar um assistente para organizar seus projetos de programação. Toda vez que você dissesse "quero criar um projeto de controle financeiro", ele imediatamente criaria uma pasta organizada, separaria os arquivos nos lugares certos, conectaria tudo ao GitHub (o lugar onde programadores guardam os projetos na nuvem) e deixaria tudo pronto para começar a trabalhar.

**É exatamente isso que este sistema faz.**

Depois de instalar, você abre o Claude Code no VS Code, diz algo como *"criar um projeto de lista de tarefas"*, e o Claude organiza tudo automaticamente. Você não precisa criar pasta, não precisa configurar nada, não precisa lembrar de fazer backup. Ele faz por você.

---

## O que você precisa ter antes de instalar

Apenas uma coisa: o **VS Code com a extensão Claude Code** instalada e funcionando.

Tudo o mais que o sistema precisa — Node.js, GitHub CLI, autenticação no GitHub — o instalador verifica e instala automaticamente. Você não precisa fazer nada disso na mão.

Se você ainda não tem o VS Code: baixe em https://code.visualstudio.com. Depois, dentro do VS Code, instale a extensão **Claude Code** pela aba de extensões (o ícone de 4 quadradinhos na barra lateral esquerda do VS Code).

---

## Instalando o sistema

### No Mac

Abra o **Terminal** — pressione **Command + Espaço**, escreva **Terminal** e pressione Enter. Uma janela escura vai abrir. É aqui onde você vai digitar os comandos.

Cole estes três comandos, um por vez, pressionando Enter após cada um:

**Passo 1 — Baixar os arquivos:**
```
cd ~/Downloads && git clone https://github.com/Hackerdomarketing/criador-de-projetos-claude-code-no-vscode.git
```

**Passo 2 — Entrar na pasta baixada:**
```
cd ~/Downloads/criador-de-projetos-claude-code-no-vscode
```

**Passo 3 — Rodar o instalador:**
```
bash instalar.sh
```

O instalador vai verificar automaticamente tudo que está instalado no seu computador e vai instalar o que estiver faltando. Se precisar de alguma autorização — senha do computador, confirmação de instalação — ele vai pedir na hora e explicar o que está fazendo. Você só precisa acompanhar e confirmar quando pedido.

### No Windows

No Windows, você precisa de um programa chamado **Git for Windows** antes de rodar o instalador. Ele instala o Git (necessário para criar repositórios) e um terminal chamado **Git Bash**, que é onde você vai digitar os comandos.

**Para instalar o Git for Windows:**
1. Acesse: https://git-scm.com/download/win
2. O download começa automaticamente — abra o arquivo que baixar
3. Clique **Next** em todas as telas (as opções padrão estão corretas) e depois **Install**
4. Após instalar, pesquise **Git Bash** no menu Iniciar e abra

Com o Git Bash aberto, cole os mesmos três passos acima — eles funcionam igual ao Mac. O instalador vai verificar automaticamente se Node.js e GitHub CLI estão instalados no seu computador. Se não estiverem, ele vai mostrar exatamente o que você precisa fazer antes de continuar.

---

## Usando depois de instalar

### Onde abrir o VS Code

Abra o VS Code na pasta `~/Documents/VSCODE/`. É lá que o Claude vai criar os projetos.

No VS Code: **File → Open Folder → Documents → VSCODE → Select Folder**

### Como abrir o Claude Code no VS Code

Na barra lateral esquerda do VS Code, clique no ícone do Claude Code (um "A" estilizado ou o logo da Anthropic). Uma janela de conversa vai abrir do lado.

### O que dizer para criar um projeto

Simplesmente descreva o que você quer criar:

*"Criar um projeto de lista de tarefas em Python"*

*"Novo projeto: um site de portfólio com Next.js"*

*"Quero criar um sistema de controle de estoque"*

*"Faz um app de calculadora de gastos"*

O Claude vai perguntar algumas coisas para entender melhor — tecnologia, funcionalidades, integrações. Responda normalmente, como se fosse uma conversa. Depois, ele cria tudo automaticamente: pasta, arquivos, código inicial, repositório no GitHub.

---

## O que é criado em cada projeto

Toda vez que você pede um projeto novo, o Claude cria estes arquivos dentro de uma pasta com o nome do projeto:

| Arquivo | Para que serve |
|---------|----------------|
| `ARQUITETURA-MENTAL.md` | Define como o Claude vai pensar e se comportar neste projeto. Ele lê isso sempre. |
| `CLAUDE.md` | As instruções do projeto: memória, nomenclatura, como se comunicar com você. |
| `.memoria-ultimas-tarefas.md` | As 3 últimas tarefas feitas. O Claude lê isso primeiro ao abrir o projeto. |
| `.memoria-do-dia.md` | Registro cronológico de tudo que foi feito hoje neste projeto. |
| `.memoria-projeto.md` | Memória completa do projeto: decisões, arquitetura, histórico. |
| `README.md` | Documento explicando o que o projeto faz e como usar. |
| `.gitignore` | Lista de arquivos que não vão para o GitHub (senhas, arquivos temporários). |

---

## Perguntas frequentes

**Eu preciso abrir o VS Code em uma pasta específica para o sistema funcionar?**

Sim. Abra o VS Code sempre em `~/Documents/VSCODE/`. É nessa pasta que o Claude vai criar os seus projetos e onde estão as instruções que ele precisa ler. Se você abrir em outra pasta, o projeto vai ser criado lá, o que pode causar confusão.

**E se eu já tiver um arquivo CLAUDE.md na minha pasta do VS Code?**

O instalador não apaga nem modifica o que você já tem. Ele só cria um CLAUDE.md novo se não existir nenhum. Se você já tem um, o instalador vai avisar e não vai mexer nele. Se quiser adicionar as instruções do sistema ao seu CLAUDE.md existente, copie o conteúdo do arquivo `CRIADOR-DE-PROJETOS/templates/CLAUDE.md` e cole no seu.

**O repositório que o Claude cria no GitHub é privado ou público?**

Sempre privado. Só você tem acesso. Ninguém mais consegue ver.

**O que é o `~` que aparece nos caminhos de pasta?**

O `~` é uma abreviação para a pasta do seu usuário. Por exemplo, se seu nome de usuário é `joao`, então `~/Documents/VSCODE/` significa `/Users/joao/Documents/VSCODE/` no Mac, ou `C:\Users\joao\Documents\VSCODE\` no Windows.

**Posso desinstalar se não gostar?**

Sim. Basta deletar a pasta `~/Documents/VSCODE/CRIADOR-DE-PROJETOS/` e o arquivo `~/Documents/VSCODE/CLAUDE.md`. Nada mais foi modificado no seu computador.

**O que é o Git que o Claude configura em cada projeto?**

O Git é um sistema que registra cada mudança feita nos arquivos do projeto — como um histórico completo. Se você apagar algo por acidente, ou quiser voltar para uma versão anterior, o Git permite isso. O GitHub é o lugar online onde esse histórico fica guardado. Quando o Claude cria um projeto, ele configura o Git automaticamente.
