# Arquitetura

## Visão Geral

```
┌─────────────┐
│   Frontend  │
│   (React)   │
└──────┬──────┘
       │
       │ POST /convert
       ▼
┌─────────────────────┐
│   FastAPI Backend   │
│  (Padronização)     │
└──────┬──────────────┘
       │
       ▼
    Download
   (sem cache)
```

## Backend

### Endpoints

```
POST /convert
- Upload de arquivo Excel/CSV
- Processamento in-memory
- Retorna arquivo convertido
```

### Processamento

1. **Receber**: Upload do arquivo
2. **Validar**: Extensão e formato
3. **Ler**: Com Pandas
4. **Padronizar**: 
   - Remover linhas vazias
   - Normalizar cabeçalhos
   - Remover espaços
   - Converter tipos
5. **Retornar**: Arquivo pronto para download

### Stack

```
backend/
├── main.py          # Aplicação principal
├── requirements.txt # Dependências
└── Dockerfile      # Imagem Docker
```

## Frontend

### Componentes

```
frontend/
├── src/
│   ├── App.tsx      # Interface de upload/conversão
│   ├── App.css      # Estilos
│   └── index.tsx    # Entry point
├── package.json
├── tsconfig.json
└── Dockerfile
```

### Fluxo

1. Usuário seleciona arquivo
2. Validação local (extensão)
3. Upload para API
4. Processamento
5. Download automático

## Tecnologias

- **Frontend**: React, TypeScript, CSS3
- **Backend**: FastAPI, Python 3.11
- **Processamento**: Pandas, Openpyxl
- **DevOps**: Docker, Docker Compose

## Segurança

- ✅ Sem persistência
- ✅ Processamento in-memory
- ✅ CORS configurado
- ✅ Validação de arquivo
- ✅ Timeout automático
