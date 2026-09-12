# Padroniza Excel Jet ✈️

> Conversor online inteligente para padronização e limpeza automática de dados em arquivos Excel
> 
> **🌍 Site ao vivo:** https://Mari-Couto.github.io/padroniza-excel-jet
>
> **API:** https://padroniza-excel-jet.vercel.app

## 🎯 Objetivo

O **Padroniza Excel Jet** é uma aplicação web que permite:
- 📊 Carregar arquivo Excel
- 🔍 Identificar automaticamente tipos de dados e padrões
- ✨ Padronizar e limpar dados
- 💾 Baixar arquivo convertido instantaneamente
- ⚡ Conversão rápida e sem registro

## 🚀 Deploy Automático

Cada push em `main` faz deploy automático:
- ✅ **Frontend:** GitHub Pages (gratuito)
- ✅ **Backend:** Vercel (gratuito)

## 🌐 Acessar Online

```
Frontend: https://Mari-Couto.github.io/padroniza-excel-jet
API:      https://padroniza-excel-jet.vercel.app
Docs API: https://padroniza-excel-jet.vercel.app/docs
```

## 🏗️ Arquitetura

```
https://Mari-Couto.github.io/padroniza-excel-jet
                    ↓
            React Frontend
                    ↓
        POST /convert (Vercel API)
                    ↓
    https://padroniza-excel-jet.vercel.app
                    ↓
            Processar Excel
                    ↓
            Download do arquivo
```

## 🎨 Features

- ✅ Upload de arquivo Excel
- ✅ Análise automática de dados
- ✅ Identificação de tipos e padrões
- ✅ Padronização inteligente
- ✅ Download instantâneo
- ✅ Sem armazenamento de dados
- ✅ Conversão rápida
- ✅ Deploy automático

## 📚 Documentação

- [Setup Local](./docs/setup.md)
- [Arquitetura](./docs/architecture.md)
- [Vercel Setup](./docs/VERCEL_SETUP.md)
- [Contribuição](./CONTRIBUTING.md)

## 🛠️ Setup Local

```bash
# Clone
git clone https://github.com/Mari-Couto/padroniza-excel-jet.git
cd padroniza-excel-jet

# Backend
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload

# Frontend (outra aba)
cd frontend
npm install
REACT_APP_API_URL=http://localhost:8000 npm start
```

Acesse: http://localhost:3000

## 🔧 Configurar Vercel (Rápido)

### 1. Instale Vercel CLI
```bash
npm i -g vercel
```

### 2. Conecte seu projeto
```bash
vercel link
```

### 3. Configure GitHub Secrets

**Gere token Vercel:**
```bash
vercel tokens create
```

**Adicione no GitHub (Settings → Secrets and variables → Actions):**
```
VERCEL_TOKEN=<seu-token>
VERCEL_ORG_ID=<seu-org-id>
VERCEL_PROJECT_ID=<seu-project-id>
```

### 4. Configure GitHub Pages
1. **Settings → Pages**
2. **Source:** Deploy from a branch
3. **Branch:** gh-pages

### 5. Faça push
```bash
git push origin main
```

✅ Deploy automático começa!

## 📖 Referência Completa

Veja [VERCEL_SETUP.md](./docs/VERCEL_SETUP.md) para instruções detalhadas.

## 📝 Licença

MIT

## 👤 Autor

**Mari Couto** - [GitHub](https://github.com/Mari-Couto)

---

**⚡ Deploy automático com Vercel + GitHub Pages!**
