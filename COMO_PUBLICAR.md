# 🚀 Como Publicar o Workshop no Google Colab

## Opção 1: GitHub + Google Colab (Recomendado)

### Passo 1: Criar Repositório no GitHub

1. Acesse https://github.com/new
2. Crie um novo repositório:
   - Nome: `redis-workshop-2026` (ou outro nome)
   - Descrição: "Workshop hands-on de Redis com Python e redis-cli"
   - Público ou Privado (público permite link direto no Colab)
   - ✅ Marque "Add a README file" (ou use o README.md existente)

### Passo 2: Fazer Upload dos Arquivos

**Opção A: Via Interface Web do GitHub**
1. No repositório criado, clique em "Add file" → "Upload files"
2. Arraste os arquivos:
   - `redis_workshop_colab.ipynb`
   - `redis_workshop.ipynb`
   - `requirements.txt`
   - `README.md`
   - `QUICKSTART.md`
3. Clique em "Commit changes"

**Opção B: Via Git (linha de comando)**
```bash
cd /Users/gabriel.cerioni/Downloads/redis_workshop_2026

# Inicializar repositório (se ainda não foi)
git init

# Adicionar remote (substitua SEU_USUARIO e NOME_REPO)
git remote add origin https://github.com/SEU_USUARIO/redis-workshop-2026.git

# Adicionar arquivos
git add redis_workshop_colab.ipynb redis_workshop.ipynb requirements.txt README.md QUICKSTART.md

# Commit
git commit -m "Add Redis Workshop notebooks"

# Push
git branch -M main
git push -u origin main
```

### Passo 3: Criar Link do Google Colab

Após publicar no GitHub, o link do Colab segue este padrão:

```
https://colab.research.google.com/github/SEU_USUARIO/NOME_REPO/blob/main/redis_workshop_colab.ipynb
```

**Exemplo:**
Se seu GitHub é `gabrielcerioni` e o repo é `redis-workshop-2026`:
```
https://colab.research.google.com/github/gabrielcerioni/redis-workshop-2026/blob/main/redis_workshop_colab.ipynb
```

### Passo 4: Adicionar Badge no README

Edite o `README.md` e adicione no topo:

```markdown
# Redis Workshop 2026

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SEU_USUARIO/NOME_REPO/blob/main/redis_workshop_colab.ipynb)
```

Isso cria um botão clicável que abre direto no Colab! 🎉

---

## Opção 2: Google Drive + Colab (Sem GitHub)

### Passo 1: Upload para Google Drive

1. Acesse https://drive.google.com
2. Crie uma pasta "Redis Workshop"
3. Faça upload do arquivo `redis_workshop_colab.ipynb`

### Passo 2: Abrir no Colab

1. Clique com botão direito no arquivo `.ipynb`
2. Escolha "Abrir com" → "Google Colaboratory"
3. O notebook abrirá no Colab

### Passo 3: Compartilhar

1. No Colab, clique em "Compartilhar" (canto superior direito)
2. Configure as permissões:
   - "Qualquer pessoa com o link" → "Leitor"
3. Copie o link e compartilhe

**Desvantagem:** O link é longo e feio. GitHub é melhor para compartilhamento profissional.

---

## Opção 3: Publicar Direto no Colab (Temporário)

1. Acesse https://colab.research.google.com
2. Clique em "Arquivo" → "Fazer upload de notebook"
3. Selecione `redis_workshop_colab.ipynb`
4. O notebook abre no Colab
5. Clique em "Compartilhar" para gerar link

**Desvantagem:** Fica no seu Google Drive pessoal, não é versionado.

---

## 🎯 Recomendação Final

**Use GitHub + Colab** porque:
- ✅ Link curto e profissional
- ✅ Versionamento automático
- ✅ Badge bonito no README
- ✅ Fácil de atualizar
- ✅ Outras pessoas podem fazer fork
- ✅ Portfólio público

---

## 📋 Checklist Rápido

- [ ] Criar repositório no GitHub
- [ ] Fazer upload dos arquivos
- [ ] Testar o link do Colab
- [ ] Adicionar badge no README
- [ ] Compartilhar o link!

---

## 🔗 Links Úteis

- [GitHub](https://github.com)
- [Google Colab](https://colab.research.google.com)
- [Como usar Git](https://git-scm.com/book/pt-br/v2)
- [Markdown Guide](https://www.markdownguide.org/)

---

## 💡 Dica Extra

Depois de publicar, você pode compartilhar:
- O link direto do Colab (para quem quer só usar)
- O link do GitHub (para quem quer ver o código/fazer fork)
- Ambos! 🚀

