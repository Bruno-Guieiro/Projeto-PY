# 📦 Guia de Git para Trabalho em Equipe

Este guia explica **como e quando usar os principais comandos do Git** no dia a dia de um projeto em equipe.

---

## 🚀 Configuração inicial (uma vez só)

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@email.com"
```

**Quando usar:**
- Apenas na primeira vez que instalar o Git

**Por quê:**
- Define quem você é nos commits

---

## 📥 Clonar o repositório

```bash
git clone <url-do-repositorio>
cd <nome-do-repositorio>
```

**Quando usar:**
- Quando for baixar o projeto pela primeira vez

---

## 🌿 Trabalhando com branches

### Criar uma nova branch
```bash
git checkout -b minha-feature
```

### Trocar de branch
```bash
git checkout main
```

### Ver branches
```bash
git branch
```

**Quando usar:**
- Sempre que for começar uma nova funcionalidade ou correção

**Por quê:**
- Evita mexer direto na `main`
- Permite trabalho em equipe sem conflitos

---

## 🔍 Ver estado do projeto

```bash
git status
```

**Quando usar:**
- Antes de qualquer ação

**Por quê:**
- Mostra arquivos modificados e preparados

---

## ➕ Adicionar arquivos

```bash
git add .
```

**Quando usar:**
- Antes de fazer commit

**Por quê:**
- Define quais arquivos vão ser salvos

---

## 💾 Criar um commit

```bash
git commit -m "mensagem clara do que foi feito"
```

**Quando usar:**
- Depois do `git add`

**Por quê:**
- Salva uma versão do seu trabalho

---

## 🔄 Atualizar o projeto

```bash
git checkout main
git pull origin main
```

**Quando usar:**
- Antes de começar a trabalhar
- Antes de enviar alterações

**Por quê:**
- Evita conflitos e mantém seu código atualizado

---

## 📤 Enviar alterações

```bash
git push origin minha-feature
```

**Quando usar:**
- Depois de commits

**Por quê:**
- Envia seu código para o repositório remoto

---

## 🔀 Atualizar sua branch com a main

```bash
git checkout minha-feature
git merge main
```

**Quando usar:**
- Quando a `main` foi atualizada e você precisa dessas mudanças

---

## ⚠️ Resolver conflitos

**Quando acontece:**
- Duas pessoas alteram a mesma parte do código

**Como resolver:**
1. Editar os arquivos manualmente
2. Depois executar:

```bash
git add .
git commit -m "resolve conflito"
```

---

## 📜 Ver histórico

```bash
git log --oneline
```

**Quando usar:**
- Para ver o histórico de commits

---

## ❌ Desfazer alterações

### Antes do commit
```bash
git checkout -- arquivo
```

### Remover do stage
```bash
git reset arquivo
```

**Quando usar:**
- Quando quiser corrigir algo antes de salvar

---

## 🔁 Fluxo de trabalho padrão

```bash
git checkout main
git pull origin main

git checkout -b minha-feature

# fazer alterações

git status
git add .
git commit -m "feat: descrição da alteração"

git push origin minha-feature
```

Depois:
- Abrir Pull Request no GitHub

---

## 🧹 Boas práticas

- Criar uma branch para cada tarefa
- Nunca trabalhar direto na `main`
- Fazer commits pequenos e claros
- Sempre atualizar antes de começar
- Revisar código antes de enviar

---

## 🧩 Resumo rápido

- `git clone` → baixar projeto  
- `git checkout -b` → criar branch  
- `git status` → ver mudanças  
- `git add` → preparar arquivos  
- `git commit` → salvar alterações  
- `git pull` → atualizar projeto  
- `git push` → enviar alterações  
- `git merge` → juntar mudanças  