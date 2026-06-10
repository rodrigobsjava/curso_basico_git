# Curso Rápido de Git e GitHub — 5 Aulas Práticas

## Objetivo do Curso

Capacitar iniciantes a utilizar Git e GitHub para versionar projetos, publicar código e colaborar de forma básica em equipe.

---

## Fluxo visual principal

```text
Editar arquivo
     ↓
git add .
     ↓
git commit -m "mensagem"
     ↓
git push
     ↓
GitHub
```

---

# Aula 1 — Primeiros Passos com Git

## Objetivos

- Entender o que é Git
- Instalar Git
- Configurar usuário
- Criar primeiro repositório

## Comandos

```bash
git --version

git config --global user.name "Seu Nome"
git config --global user.email "email@gmail.com"

mkdir meu-primeiro-projeto
cd meu-primeiro-projeto
git init
git status
```

## Tarefa

Criar um repositório local chamado `apresentacao-pessoal`.

---

# Aula 2 — Commits e Histórico

## Objetivos

- Salvar alterações
- Entender o ciclo do Git
- Ver histórico de commits

## Diagrama

```text
Arquivo modificado → Stage → Commit → Histórico
```

## Comandos

```bash
git add .

git commit -m "feat: cria README"

git log --oneline
```

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

## Diagrama

```text
Seu computador
     ↓
Git registra versões
     ↓
GitHub publica o projeto
```

## Conteúdo

Criar um repositório no GitHub. Depois, conectar o repositório local ao remoto:

```bash
git remote add origin URL_DO_REPOSITORIO
```

Enviar projeto:

```bash
git push -u origin master
```

ou:

```bash
git push -u origin main
```

## Prática

Publicar o projeto criado nas aulas anteriores.

## Tarefa

Compartilhar o link do repositório com a turma.

---

# Aula 4 — Branches

## Objetivos

- Trabalhar em funcionalidades separadas
- Criar branches
- Trocar de branch

## Diagrama

```text
master ────────●────────●
                 \      \ merge
                  ●──────● feature-hobbies
```

## Comandos

```bash
git checkout -b feature-foto

git branch

git checkout master
```

## Tarefa

Criar uma branch própria e adicionar um arquivo novo.

---

# Aula 5 — Merge e Projeto Final

## Objetivos

- Juntar alterações
- Simular trabalho em equipe
- Publicar a versão final

## Comandos

```bash
git checkout master

git merge feature-foto

git push
```

## Projeto Final

```text
portfolio
│
├── README.md
├── sobre-mim.txt
├── habilidades.txt
├── hobbies.txt
└── contato.txt
```

---

# Roteiro dos 5 encontros de 1h

| Encontro | Tema | Divisão sugerida |
|---|---|---|
| 1 | Git básico | 10min teoria + 40min prática + 10min tarefa |
| 2 | Commits | 15min explicação + 35min commits + 10min revisão |
| 3 | GitHub | 15min demo + 35min publicação + 10min dúvidas |
| 4 | Branches | 15min conceito + 35min prática + 10min revisão |
| 5 | Merge | 15min merge + 35min projeto final + 10min fechamento |
