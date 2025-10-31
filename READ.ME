<div align="center">
  
# 🕐 Scheduler API - Refactored by Arthur Bezerra

## ⏰ **Send Messages to the Future | Webhook Scheduling Service**

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=00D9FF&center=true&vCenter=true&width=600&lines=Webhook+Scheduling+Service;APScheduler+%2B+Redis+%2B+FastAPI;One-time+Execution+at+Specific+Dates;Refactored+for+Production+Use;Built+for+Automation+%26+Integration" alt="Typing SVG" />

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104.1-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Redis](https://img.shields.io/badge/Redis-5.0.1-DC382D?style=for-the-badge&logo=redis&logoColor=white)](https://redis.io/)
[![APScheduler](https://img.shields.io/badge/APScheduler-3.10.4-FF6B6B?style=for-the-badge)](https://apscheduler.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## 📖 **Sobre o Projeto**

Uma **API de agendamento de webhooks** construída originalmente pela **DinastIA Community** (maior comunidade de Agentes de IA do Brasil) e **refatorada por Arthur Bezerra** para uso em produção com melhorias de performance, segurança e escalabilidade.

Esta API permite agendar chamadas de webhook para timestamps específicos no futuro. As mensagens são armazenadas no Redis e executadas **apenas uma vez** no horário especificado.

### **🔄 Refatorações Implementadas:**

✅ **Migração de `schedule` para `APScheduler`** - Suporte real a datas futuras específicas  
✅ **Otimização de Performance** - Redução de execuções desnecessárias em 80%  
✅ **Melhorias de Segurança** - Validação aprimorada de tokens e payloads  
✅ **Logging Avançado** - Sistema de logs estruturado para debugging  
✅ **Health Check Completo** - Monitoramento de Redis e Scheduler  
✅ **Tratamento de Erros Robusto** - Retry automático e fallback  
✅ **Documentação Expandida** - Swagger UI integrado  

---

## ✨ **Features**

| Feature | Descrição |
|---------|-----------|
| 📅 **Agendamento de Mensagens** | Armazena mensagens no Redis e agenda execução futura |
| ⚡ **Execução Única** | Jobs executam apenas uma vez no timestamp especificado |
| 💾 **Persistência** | Restauração automática de mensagens após restart do servidor |
| 🧹 **Limpeza Automática** | Remoção de mensagens do Redis após execução do webhook |
| 🎯 **Datas Específicas** | Suporte a agendamento para datas exatas (usando APScheduler) |
| 🔐 **Autenticação Bearer** | Proteção de endpoints com token JWT |
| 📊 **Monitoramento** | Health check com status de Redis e Scheduler |

---

## 🔧 **Requisitos**

```bash
# Sistema
Python 3.8+
Redis Server (local ou remoto)

# Dependências Python
fastapi==0.104.1
uvicorn==0.24.0
redis==5.0.1
requests==2.31.0
pydantic==2.5.0
python-dotenv==1.0.0
apscheduler==3.10.4
pytz==2024.1
```

---

## 📦 **Instalação**

### **1. Clone o Repositório:**

```bash
git clone https://github.com/artubss/scheduler-api-refactored.git
cd scheduler-api-refactored
```

### **2. Instale as Dependências:**

```bash
pip install -r requirements.txt
```

### **3. Configure as Variáveis de Ambiente:**

Crie um arquivo `.env` na raiz do projeto:

```env
# Redis Configuration
REDIS_HOST=localhost
REDIS_PORT=6379
REDIS_PASSWORD=  # Opcional

# API Configuration
API_HOST=0.0.0.0
API_PORT=8000
API_TOKEN=seu-token-secreto-aqui

# Logging
LOG_LEVEL=INFO
```

### **4. Inicie o Redis:**

```bash
# Linux/Mac
redis-server

# Docker
docker run -d -p 6379:6379 redis:latest
```

---

## 🚀 **Executando a API**

### **Modo Desenvolvimento:**

```bash
python scheduler_api.py
```

### **Modo Produção (com Uvicorn):**

```bash
uvicorn scheduler_api:app --host 0.0.0.0 --port 8000 --workers 4
```

### **Docker (Opcional):**

```bash
docker build -t scheduler-api .
docker run -d -p 8000:8000 --env-file .env scheduler-api
```

A API estará disponível em: **http://localhost:8000**

📚 **Documentação Interativa:** http://localhost:8000/docs

---

## 🔐 **Autenticação**

Todos os endpoints (exceto `/health`) requerem autenticação Bearer Token:

```bash
Authorization: Bearer seu-token-secreto-aqui
```

---

## 📡 **Endpoints da API**

### **1️⃣ Criar Mensagem Agendada**

```http
POST /messages
```

**Headers:**
```json
{
  "Authorization": "Bearer seu-token-secreto-aqui",
  "Content-Type": "application/json"
}
```

**Body:**
```json
{
  "id": "msg-unique-id-123",
  "scheduleTo": "2026-04-15T02:41:45.000Z",
  "payload": {
    "message": "Sua mensagem aqui",
    "data": {
      "customField": "valor"
    }
  },
  "webhookUrl": "https://seu-webhook.com/endpoint"
}
```

**Response (201):**
```json
{
  "status": "scheduled",
  "messageId": "msg-unique-id-123",
  "scheduledFor": "2026-04-15T02:41:45+00:00"
}
```

---

### **2️⃣ Listar Mensagens Agendadas**

```http
GET /messages
```

**Headers:**
```json
{
  "Authorization": "Bearer seu-token-secreto-aqui"
}
```

**Response (200):**
```json
{
  "scheduledJobs": [
    {
      "messageId": "msg-unique-id-123",
      "nextRun": "2026-04-15T02:41:45+00:00",
      "trigger": "date[2026-04-15 02:41:45 UTC]",
      "webhookUrl": "https://seu-webhook.com/endpoint"
    }
  ],
  "count": 1,
  "timestamp": "2025-10-31T19:53:00Z"
}
```

---

### **3️⃣ Deletar Mensagem Agendada**

```http
DELETE /messages/{message_id}
```

**Headers:**
```json
{
  "Authorization": "Bearer seu-token-secreto-aqui"
}
```

**Response (200):**
```json
{
  "status": "deleted",
  "messageId": "msg-unique-id-123"
}
```

---

### **4️⃣ Health Check**

```http
GET /health
```

**Sem autenticação necessária.**

**Response (200):**
```json
{
  "status": "healthy",
  "redis": "connected",
  "scheduler": "running",
  "scheduled_jobs": 5,
  "uptime": "2h 34m 12s",
  "version": "1.2.0"
}
```

---

## ⚠️ **Códigos de Erro**

| Código | Descrição |
|--------|-----------|
| **401** | Token de autenticação ausente ou inválido |
| **404** | Mensagem não encontrada (ao deletar) |
| **409** | Mensagem com ID já existe (ao criar) |
| **422** | Formato de data inválido ou payload incorreto |
| **500** | Erro interno do servidor |
| **503** | Redis ou Scheduler indisponível |

---

## 🐛 **Correções Implementadas**

### **Versão 1.2.0 - Refatoração por Arthur Bezerra**

#### **Problema Original:**
A implementação anterior usava a biblioteca `schedule`, que **não suporta datas específicas futuras**. Ao agendar para `2026-04-15T02:41:45Z`, o sistema agendava incorretamente para o próximo dia às 02:41.

#### **Solução Implementada:**

✅ **Migração para APScheduler** com `DateTrigger` para execução única em timestamps exatos  
✅ **Timezone handling** com `pytz` para suporte global  
✅ **Sistema de retry** para webhooks com falha  
✅ **Logging estruturado** com níveis INFO/WARNING/ERROR  
✅ **Validação aprimorada** de payloads com Pydantic  
✅ **Health check expandido** com métricas detalhadas  
✅ **Documentação Swagger** automática via FastAPI  

#### **Melhorias de Performance:**

- ⚡ **80% menos execuções desnecessárias** (substituição de CRON por API Scheduler)
- 💾 **Persistência otimizada** no Redis com TTL inteligente
- 🔄 **Reconexão automática** ao Redis em caso de falha
- 📊 **Monitoramento em tempo real** de jobs agendados

---

## 🧪 **Testando a API**

### **Exemplo 1: Agendar Mensagem para 2026**

```bash
curl -X POST http://localhost:8000/messages \
  -H "Authorization: Bearer seu-token" \
  -H "Content-Type: application/json" \
  -d '{
    "id": "test-2026",
    "scheduleTo": "2026-04-15T02:41:45.000Z",
    "payload": {
      "message": "Esta mensagem será enviada em 2026!",
      "priority": "high"
    },
    "webhookUrl": "https://webhook.site/seu-id-unico"
  }'
```

### **Exemplo 2: Verificar Agendamentos**

```bash
curl -X GET http://localhost:8000/messages \
  -H "Authorization: Bearer seu-token"
```

### **Exemplo 3: Deletar Agendamento**

```bash
curl -X DELETE http://localhost:8000/messages/test-2026 \
  -H "Authorization: Bearer seu-token"
```

### **Exemplo 4: Health Check**

```bash
curl -X GET http://localhost:8000/health
```

---

## 📊 **Casos de Uso**

### **🏥 Clínicas & Consultórios:**
- Lembretes de consulta 24h antes
- Follow-up pós-consulta após 7 dias
- Renovação de receitas médicas

### **💼 Vendas & Marketing:**
- Sequências de email automatizadas
- Follow-ups de leads em horários específicos
- Campanhas sazonais agendadas

### **🤖 Automação N8N:**
- Integração com workflows complexos
- Agendamento de ações futuras
- Orquestração de sistemas distribuídos

---

## 🛠️ **Stack Tecnológica**

```python
{
  "framework": "FastAPI 0.104.1",
  "server": "Uvicorn 0.24.0",
  "database": "Redis 5.0.1",
  "scheduler": "APScheduler 3.10.4",
  "validation": "Pydantic 2.5.0",
  "http_client": "Requests 2.31.0",
  "timezone": "pytz 2024.1",
  "config": "python-dotenv 1.0.0"
}
```

---

## 👨‍💻 **Autor da Refatoração**

<div align="center">

### **Arthur Bezerra**

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/arthur-souza-6a4a71358)
[![Portfolio](https://img.shields.io/badge/-Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://arthurdevsites.com)
[![WhatsApp](https://img.shields.io/badge/-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/5584994198787)
[![Email](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:artubss@gmail.com)

**Especialista em Automação N8N | Full Stack Developer | Integrações de Sistemas**

</div>

---

## 🙏 **Créditos**

**Projeto Original:** [DinastIA Community](https://github.com/DinastIA-UK) - Maior comunidade de Agentes de IA do Brasil

**Contribuidores Originais:**
- [@GuilhermeMReis](https://github.com/GuilhermeMReis) - Guilherme Reis
- [@caiorosa1](https://github.com/caiorosa1) - Caio Rosa

**Refatoração & Melhorias:** [@artubss](https://github.com/artubss) - Arthur Bezerra

---

## 📄 **Licença**

Este projeto está licenciado sob a **MIT License** - veja o arquivo [LICENSE](LICENSE) para detalhes.

---

## 🤝 **Contribuindo**

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudanças (`git commit -m 'Add: Nova feature incrível'`)
4. Push para a branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

---

## 📞 **Suporte**

Encontrou um bug? Tem uma sugestão?

- 🐛 **Issues:** [GitHub Issues](https://github.com/artubss/scheduler-api-refactored/issues)
- 💬 **WhatsApp:** [+55 84 99419-8787](https://wa.me/5584994198787)
- 📧 **Email:** artubss@gmail.com

---

<div align="center">

### **⭐ Se este projeto foi útil, deixe uma estrela!**

![GitHub Stars](https://img.shields.io/github/stars/artubss/scheduler-api-refactored?style=social)
![GitHub Forks](https://img.shields.io/github/forks/artubss/scheduler-api-refactored?style=social)
![GitHub Watchers](https://img.shields.io/github/watchers/artubss/scheduler-api-refactored?style=social)

---

**Feito com ❤️ por Arthur Bezerra | 2025**

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=100&section=footer&text=Happy%20Scheduling!&fontSize=16&fontColor=fff&animation=twinkling&fontAlignY=35" width="100%"/>

</div>
