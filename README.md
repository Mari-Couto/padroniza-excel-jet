# Padroniza Excel Jet ✈️

> Conversor online inteligente para padronização e limpeza automática de dados em arquivos Excel
> 
> **🌍 Site ao vivo:** https://Mari-Couto.github.io/padroniza-excel-jet

## 🎯 Objetivo

O **Padroniza Excel Jet** é uma aplicação web que permite:
- 📊 Carregar arquivo Excel
- 🔍 Identificar automaticamente tipos de dados e padrões
- ✨ Padronizar e limpar dados
- 💾 Baixar arquivo convertido instantaneamente
- ⚡ Conversão rápida e sem registro

## 🚀 Deploy Automático

Cada push em `main` faz deploy automático:
- ✅ Frontend: GitHub Pages (gratuito)
- ✅ Backend: Vercel/Render (gratuito com limitações)

## 🏗️ Arquitetura

```
Acesso: https://Mari-Couto.github.io/padroniza-excel-jet
                    ↓
            React Frontend
                    ↓
            Chamar API Backend
                    ↓
        Vercel/Render/Railway
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
- ✅ Deploy automático no GitHub

## 📚 Documentação

- [Setup Local](./docs/setup.md)
- [Arquitetura](./docs/architecture.md)
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
npm start
```

Acesse: http://localhost:3000

## 🌐 Deploy Online

### Opção 1: GitHub Pages + Vercel (Recomendado)

1. **Frontend automático** no GitHub Pages
2. **Backend** no Vercel (serverless)

```bash
# Apenas push para main
git push origin main
```

### Opção 2: GitHub Pages + Railway

Railway oferece $5/mês grátis

```bash
railway login
railway link
railway up
```

### Opção 3: Google Cloud Run

```bash
gcloud app deploy backend/app.yaml
```

## 📝 Licença

MIT

## 👤 Autor

**Mari Couto** - [GitHub](https://github.com/Mari-Couto)

---

**⚡ Feito com ❤️ - Deploy Automático no GitHub!**
