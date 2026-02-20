# CRIADOR DE PROJETOS para Claude Code no VS Code

---

## O que é isso?

Imagine que você quer contratar um assistente para organizar seus projetos de programação. Toda vez que você dissesse *"quero criar um projeto de controle financeiro"*, ele imediatamente criaria uma pasta organizada, separaria os arquivos nos lugares certos, conectaria tudo ao GitHub (o lugar onde programadores guardam os projetos na nuvem) e deixaria tudo pronto para começar a trabalhar.

**É exatamente isso que este sistema faz.**

Depois de instalar, você abre o Claude Code no VS Code, diz algo como *"criar um projeto de lista de tarefas"*, e o Claude organiza tudo automaticamente. Você não precisa criar pasta, não precisa configurar nada, não precisa lembrar de fazer backup. Ele faz por você.

> Este repositório é para quem usa o **Claude Code como extensão do VS Code**.
> Se você usa o Claude Code no terminal ou no Claude Desktop App, use este outro:
> https://github.com/Hackerdomarketing/criador-de-projetos-no-claude-code

---

## Instalação

A instalação é feita pelo próprio Claude Code. Você só precisa colar um prompt — ele faz todo o resto.

---

### Se você usa Mac

Abra o VS Code, clique no ícone do Claude Code na barra lateral e cole o prompt abaixo:

```
Por favor, instala o sistema Criador de Projetos no meu computador.

Passos:
1. Clona este repositório em ~/Downloads:
   https://github.com/Hackerdomarketing/criador-de-projetos-claude-code-no-vscode.git
2. Entra na pasta clonada
3. Roda: bash instalar.sh
   O script verifica e instala automaticamente Node.js, GitHub CLI
   e faz a autenticação no GitHub. Confirme as permissões que ele pedir.
4. Ao terminar, me mostra o que foi instalado e como começar a usar.
```

O Claude vai pedir permissão antes de cada ação. Clique em **Sim** para tudo — ele está instalando as ferramentas necessárias. Se pedir a senha do seu computador, é normal — é para instalar programas.

---

### Se você usa Windows

No Windows, você precisa de um programa chamado **Git for Windows** antes de instalar. Ele é necessário para o Claude conseguir baixar os arquivos do repositório.

**Para instalar o Git for Windows:**
1. Acesse: https://git-scm.com/download/win
2. O download começa automaticamente — abra o arquivo que baixar
3. Clique **Next** em todas as telas (as opções padrão estão corretas) e **Install**

Depois de instalar o Git, abra o VS Code, clique no ícone do Claude Code e cole o prompt abaixo:

```
Por favor, instala o sistema Criador de Projetos no meu computador.
Estou no Windows com Git Bash disponível.

Passos:
1. Clona este repositório em ~/Downloads:
   https://github.com/Hackerdomarketing/criador-de-projetos-claude-code-no-vscode.git
2. Entra na pasta clonada
3. Roda: bash instalar.sh
   O script verifica se Node.js e GitHub CLI estão instalados.
   Se não estiverem, vai mostrar como instalar cada um.
   Confirme as permissões que ele pedir.
4. Ao terminar, me mostra o que foi instalado e como começar a usar.
```

---

## Usando depois de instalar

### Onde abrir o VS Code

Abra o VS Code na pasta `~/Documents/VSCODE/` — é lá que o Claude vai criar os projetos.

No VS Code: **File → Open Folder → Documents → VSCODE → Select Folder**

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
| `CLAUDE.md` | As instruções do projeto: memória, nomenclatura, como se comunicar com você. |
| `.memoria-ultimas-tarefas.md` | As 3 últimas tarefas feitas. O Claude lê isso primeiro ao abrir o projeto. |
| `.memoria-do-dia.md` | Registro cronológico de tudo que foi feito hoje neste projeto. |
| `.memoria-projeto.md` | Memória completa do projeto: decisões, arquitetura, histórico. |
| `README.md` | Documento explicando o que o projeto faz e como usar. |
| `.gitignore` | Lista de arquivos que não vão para o GitHub (senhas, arquivos temporários). |

---

## Perguntas frequentes

**Eu preciso abrir o VS Code em uma pasta específica para o sistema funcionar?**

Sim. Abra o VS Code sempre em `~/Documents/VSCODE/`. É nessa pasta que ficam as instruções que o Claude precisa ler. Se você abrir em outra pasta, o Claude não vai encontrar essas instruções e não vai saber criar projetos automaticamente.

**E se eu já tiver um arquivo CLAUDE.md na minha pasta do VS Code?**

O instalador não apaga nem modifica o que você já tem. Ele só cria um CLAUDE.md novo se não existir nenhum. Se você já tem um, ele vai avisar e não vai mexer. Para adicionar as instruções deste sistema ao seu CLAUDE.md existente, copie o conteúdo de `CRIADOR-DE-PROJETOS/templates/CLAUDE.md` e cole no seu.

**O repositório que o Claude cria no GitHub é privado ou público?**

Sempre privado. Só você tem acesso.

**O que é o `~` que aparece nos caminhos de pasta?**

É uma abreviação para a pasta do seu usuário. Se seu nome de usuário é `joao`, então `~/Documents/VSCODE/` significa `/Users/joao/Documents/VSCODE/` no Mac, ou `C:\Users\joao\Documents\VSCODE\` no Windows.

**Posso desinstalar se não gostar?**

Sim. Delete a pasta `~/Documents/VSCODE/CRIADOR-DE-PROJETOS/` e o arquivo `~/Documents/VSCODE/CLAUDE.md`. Nada mais foi modificado no seu computador.

**O que é o Git que o Claude configura em cada projeto?**

O Git é um sistema que registra cada mudança feita nos arquivos do projeto — como um histórico completo. Se você apagar algo por acidente ou quiser voltar para uma versão anterior, o Git permite isso. Quando o Claude cria um projeto, ele configura o Git automaticamente para você não precisar fazer isso na mão.
