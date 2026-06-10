# Curso Rápido de Git e GitHub — 5 Aulas Práticas

Material fonte para ensinar iniciantes em Git e GitHub com foco em prática, explicações simples e exercícios guiados.

---

## Objetivo do Curso

Capacitar iniciantes a utilizar Git e GitHub para versionar projetos, publicar código e colaborar de forma básica em equipe.

---

## Visão Geral das 5 Aulas

| Aula | Tema | Prática principal |
|---|---|---|
| 1 | Primeiros Passos com Git | `git init`, configuração e README |
| 2 | Commits e Histórico | `git add`, `git commit`, `git log` |
| 3 | GitHub na Prática | repositório remoto e `git push` |
| 4 | Branches | criar branch e trabalhar separado |
| 5 | Merge e Projeto Final | unir alterações e publicar portfólio |

---

# Aula 1 — Primeiros Passos com Git

## Objetivos

- Entender o que é Git
- Instalar Git
- Configurar usuário
- Criar primeiro repositório

## Conteúdo

```bash
git --version

git config --global user.name "Seu Nome"
git config --global user.email "email@gmail.com"

mkdir meu-primeiro-projeto
cd meu-primeiro-projeto
git init

git status
```

## Prática

Criar o arquivo `README.md` com o conteúdo:

```markdown
# Meu Primeiro Projeto
```

## Tarefa

Criar um repositório local chamado `apresentacao-pessoal`.

---

# Aula 2 — Commits e Histórico

## Objetivos

- Salvar alterações
- Entender o ciclo do Git

## Conteúdo

```bash
git add .

git commit -m "feat: cria README"

git log --oneline
```

## Fluxo visual

```text
Arquivo alterado
      ↓
git add .
      ↓
git commit -m "mensagem"
      ↓
Histórico salvo
```

## Prática

Criar `sobre-mim.txt`, adicionar informações pessoais e realizar commit.

## Tarefa

Criar três commits diferentes:

```text
feat: adiciona nome
feat: adiciona curso
feat: adiciona contato
```

---

# Aula 3 — GitHub na Prática

## Objetivos

- Criar conta GitHub
- Criar repositório remoto
- Enviar projeto para a nuvem

## Conteúdo

```bash
git remote add origin URL_DO_REPOSITORIO

git push -u origin master
```

ou:

```bash
git push -u origin main
```

## Fluxo visual

```text
Computador local
      ↓
git remote add origin URL
      ↓
git push
      ↓
GitHub
```

## Prática

Publicar o projeto criado nas aulas anteriores.

## Tarefa

Compartilhar o link do repositório com a turma.

---

# Aula 4 — Branches

## Objetivos

- Trabalhar em funcionalidades separadas
- Entender o conceito de branch
- Criar, visualizar e trocar de branch
- Fazer uma alteração isolada sem mexer imediatamente na versão principal

## Ideia central

Uma **branch** é uma linha paralela de desenvolvimento. Ela permite testar uma ideia, criar uma funcionalidade ou alterar arquivos sem afetar diretamente a branch principal, normalmente chamada `master` ou `main`.

## Diagrama visual

```text
master/main  ── C1 ── C2 ── C3 ── C4
                    \
                     └── feature-foto ── B1 ── B2
```

Interpretação:

- `C1`, `C2`, `C3` e `C4` são commits da linha principal.
- `feature-foto` é uma branch separada.
- `B1` e `B2` são commits feitos dentro da branch.

## Conteúdo

Criar branch:

```bash
git checkout -b feature-foto
```

Visualizar branches:

```bash
git branch
```

Trocar para a branch principal:

```bash
git checkout master
```

ou, se o projeto usa `main`:

```bash
git checkout main
```

## Prática guiada

Criar uma branch para adicionar um arquivo de hobbies:

```bash
git checkout -b feature-hobbies
```

Criar o arquivo:

```text
hobbies.txt
```

Adicionar conteúdo ao arquivo, por exemplo:

```text
Meus hobbies:
- Programar
- Estudar tecnologia
- Jogar
```

Verificar status:

```bash
git status
```

Adicionar e salvar:

```bash
git add .

git commit -m "feat: adiciona arquivo de hobbies"
```

Voltar para a branch principal:

```bash
git checkout master
```

## Fluxo visual da prática

```text
Criar branch
      ↓
Criar hobbies.txt
      ↓
Editar conteúdo
      ↓
git add .
      ↓
git commit -m "feat: adiciona arquivo de hobbies"
      ↓
Voltar para master/main
```

## Roteiro de 1h para ministrar a Aula 4

| Tempo | Atividade | Como conduzir |
|---|---|---|
| 0–10 min | Revisão rápida | Relembrar `git init`, `git add`, `git commit` e `git push` |
| 10–20 min | Conceito de branch | Explicar branch como linha paralela de desenvolvimento |
| 20–40 min | Prática guiada | Criar `feature-hobbies`, adicionar `hobbies.txt` e fazer commit |
| 40–50 min | Prática individual | Cada aluno cria uma branch com funcionalidade própria |
| 50–60 min | Correção | Revisar `git branch`, `git status` e dúvidas |

## Erros comuns

- Criar arquivo na branch errada
- Esquecer de fazer commit antes de trocar de branch
- Confundir `master/main` com `feature`
- Não usar `git status` para se localizar

## Tarefa

Cada aluno deve criar uma branch própria com uma funcionalidade diferente.

Sugestões:

```text
feature-habilidades
feature-contato
feature-bio
feature-hobbies
feature-projetos
```

Checklist da tarefa:

- Criar branch com nome claro
- Criar ou alterar um arquivo
- Executar `git status`
- Executar `git add .`
- Criar commit com mensagem clara
- Voltar para `master` ou `main`

---

# Aula 5 — Merge e Projeto Final

## Objetivos

- Unir alterações
- Simular trabalho em equipe

## Conteúdo

Voltar para a branch principal:

```bash
git checkout master
```

Realizar merge:

```bash
git merge feature-foto
```

Enviar para o GitHub:

```bash
git push
```

## Projeto Final

Criar a seguinte estrutura:

```text
portfolio
│
├── README.md
├── sobre-mim.txt
├── habilidades.txt
├── hobbies.txt
└── contato.txt
```

## Fluxo obrigatório

```bash
git init

git add .

git commit -m "feat: projeto inicial"

git remote add origin URL

git push

git checkout -b feature-habilidades

git add .

git commit -m "feat: adiciona habilidades"

git checkout master

git merge feature-habilidades

git push
```

---

# Resumo dos Comandos

```bash
git init

git status

git add .

git commit -m "mensagem"

git log --oneline

git branch

git checkout -b nova-branch

git checkout master

git merge nome-da-branch

git remote add origin URL

git push

git pull

git clone URL
```

---

# Resultado Esperado

Ao final do curso o aluno será capaz de:

- Criar repositórios Git
- Fazer commits corretamente
- Publicar projetos no GitHub
- Trabalhar com branches
- Realizar merges
- Manter um portfólio simples no GitHub
