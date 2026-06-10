# Curso Rápido de Git e GitHub — 5 Aulas Práticas

> Material fonte para apresentação em sala, ministração em 5 encontros de 1h e estudo prático com diagramas de fluxo.

---

## Objetivo do Curso

Capacitar iniciantes a utilizar Git e GitHub para versionar projetos, publicar código e colaborar de forma básica em equipe.

---

## Visão Geral dos 5 Encontros

| Aula | Tema | Entrega prática |
|---|---|---|
| 1 | Primeiros passos com Git | Repositório local criado |
| 2 | Commits e histórico | Três commits no projeto |
| 3 | GitHub na prática | Projeto publicado no GitHub |
| 4 | Branches | Funcionalidade em branch separada |
| 5 | Merge e projeto final | Mini portfólio versionado |

---

# Diagrama Geral do Fluxo Git/GitHub

```text
[Projeto local]
      |
      v
  git init
      |
      v
[Arquivos modificados]
      |
      v
  git add .
      |
      v
[Stage / Preparado]
      |
      v
  git commit -m "mensagem"
      |
      v
[Histórico local]
      |
      v
  git push
      |
      v
[GitHub / Repositório remoto]
```

---

# Aula 1 — Primeiros Passos com Git

## Objetivos

- Entender o que é Git
- Instalar Git
- Configurar usuário
- Criar primeiro repositório

## Conteúdo

Verificar instalação:

```bash
git --version
```

Configuração inicial:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "email@gmail.com"
```

Criando projeto:

```bash
mkdir meu-primeiro-projeto
cd meu-primeiro-projeto
git init
```

Verificando status:

```bash
git status
```

## Prática

Criar um arquivo:

```text
README.md
```

Conteúdo:

```markdown
# Meu Primeiro Projeto
```

## Tarefa

Criar um repositório local chamado:

```text
apresentacao-pessoal
```

---

# Aula 2 — Commits e Histórico

## Objetivos

- Salvar alterações
- Entender o ciclo do Git

## Conteúdo

Adicionar arquivos:

```bash
git add .
```

Criar commit:

```bash
git commit -m "feat: cria README"
```

Ver histórico:

```bash
git log --oneline
```

## Diagrama do Ciclo do Commit

```text
[Arquivo alterado]
       |
       v
   git status
       |
       v
   git add .
       |
       v
[Arquivo preparado]
       |
       v
   git commit
       |
       v
[Versão salva no histórico]
```

## Prática

Criar:

```text
sobre-mim.txt
```

Adicionar informações pessoais e realizar commit.

## Tarefa

Criar três commits diferentes.

Exemplo:

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

Criar um repositório no GitHub.

Conectar repositório local ao remoto:

```bash
git remote add origin URL_DO_REPOSITORIO
```

Enviar projeto:

```bash
git push -u origin master
```

ou

```bash
git push -u origin main
```

## Diagrama Local x Remoto

```text
[Seu computador]  -- git push -->  [GitHub]
[Seu computador]  <-- git pull --  [GitHub]
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

## Conteúdo

Criar branch:

```bash
git checkout -b feature-foto
```

Visualizar branches:

```bash
git branch
```

Trocar de branch:

```bash
git checkout master
```

## Diagrama de Branch

```text
master:        A ---- B ---- C
                    \
feature-foto:       D ---- E
```

## Prática

Criar o arquivo:

```text
hobbies.txt
```

Adicionar conteúdo e realizar commit.

## Tarefa

Cada aluno deve criar uma branch própria com uma funcionalidade diferente.

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

## Diagrama de Merge

```text
master:        A ---- B -------- M
                    \          /
feature-foto:       C ---- D --

M = commit de merge ou integração das alterações
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

Fluxo obrigatório:

```bash
git init

git add .

git commit -m "feat: projeto inicial"

git remote add origin URL

git push

git checkout -b feature-habilidades

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
