# 🤖 Assistente de Investimentos com IA

Sistema de automação (RPA) desenvolvido com **n8n**, **Python** e **Inteligência Artificial** para analisar o perfil de investidores, consultar dados de mercado, gerar recomendações financeiras personalizadas e enviar relatórios automaticamente por e-mail.

O projeto foi criado como um MVP (Minimum Viable Product) e demonstra a integração entre automações no n8n, processamento em Python, APIs externas e modelos de IA para construção de um assistente financeiro inteligente.

---

# 📋 Visão Geral

Este projeto automatiza todo o processo de atendimento de um investidor:

1. Recebe os dados do cliente através de um Webhook.
2. Consulta ativos financeiros em APIs do mercado.
3. Processa informações utilizando Python.
4. Utiliza IA para gerar recomendações.
5. Produz um relatório em linguagem natural.
6. Monta um e-mail profissional.
7. Envia automaticamente para o investidor.
8. Registra a execução para auditoria e rastreabilidade.

---

# 🎯 Objetivo

Criar um assistente capaz de:

- Coletar informações dos investidores;
- Interpretar o perfil de risco;
- Consultar informações de mercado;
- Gerar recomendações automatizadas utilizando IA;
- Produzir relatórios personalizados;
- Automatizar o envio por e-mail;
- Reduzir o trabalho manual de análise e comunicação.

---
# 📚 Conteúdo do Projeto

O MVP será construído seguindo as seguintes etapas:

## 1. Introdução à Criação de Assistentes de Investimento com IA

- Conceitos de IA aplicada ao mercado financeiro.
- Estrutura de agentes inteligentes.
- Perfil de investidor.
- Tomada de decisão baseada em dados.

## 2. Estruturando o MVP com Colab, Webhook e n8n

- Criação do ambiente Python no Google Colab.
- Configuração dos Webhooks no n8n.
- Recebimento de informações dos investidores.
- Integração inicial entre serviços.

## 3. HTTP + Code + Merge: Integrando o Fluxo do MVP

- Consumo de APIs financeiras.
- Processamento dos dados.
- Combinação de múltiplas fontes utilizando Merge.
- Preparação dos dados para análise.

## 4. Code + Recapitulação: Integração dos Agentes de IA

- Tratamento de dados em Python.
- Criação de prompts.
- Integração com OpenAI ou Gemini.
- Geração das recomendações personalizadas.

## 5. Briefing Email + LLM: Automação de Emails com IA

- Criação automática de resumos.
- Geração de conteúdo de e-mail.
- Personalização baseada no perfil do investidor.

## 6. Gmail + Final: Validação e Automação de Emails

- Integração com Gmail.
- Envio automático dos relatórios.
- Controle de erros.
- Validação completa do fluxo.
- Controle de erros.
- Validação completa do fluxo.

# 🏗 Arquitetura da Solução

```text
┌──────────────┐
│   Usuário    │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│   Webhook    │
│     n8n      │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ HTTP Request │
│ APIs Mercado │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Python Agent │
│   Análises   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│     LLM      │
│ OpenAI/Gemini│
└──────┬───────┘
       │
       ▼
┌──────────────┐
│    Merge     │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│ Email HTML   │
└──────┬───────┘
       │
       ▼
┌──────────────┐
│    Gmail     │
└──────────────┘
```
# 🛠 Tecnologias Utilizadas

## Automação

- n8n
- Webhooks
- HTTP Request
- Code Node
- Merge Node

## Linguagem

- Python 3.11+

## Inteligência Artificial

- OpenAI GPT
- Google Gemini
- LangChain (opcional)

## APIs Financeiras

- Yahoo Finance
- Alpha Vantage
- Status Invest

## Comunicação

- Gmail API
- SMTP

## Ambiente

- Linux
- Docker
- Google Colab

---
{
  "perfil": "moderado",
  "recomendacao": "Carteira equilibrada",
  "renda_fixa": "50%",
  "acoes": "40%",
  "fiis": "10%"
}
```

---

# 🔐 Segurança

Boas práticas utilizadas:

- HTTPS obrigatório
- Variáveis de ambiente
- Credenciais protegidas
- OAuth2 para Gmail
- Logs de execução
- Auditoria de processamento
- Validação de dados de entrada

---

# 📈 Roadmap

## Versão 2.0

- Integração com WhatsApp
- Dashboard Power BI
- Agente financeiro via Telegram
- Geração automática de PDFs
- Histórico de recomendações
- Banco de dados PostgreSQL
- Integração com corretoras

---

# 🧪 Testes

Para validar o Webhook:

```bash
curl -X POST https://n8n.seudominio.com/webhook/investimentos \
-H "Content-Type: application/json" \
-d '{
     "nome":"Marinaldo",
     "perfil":"moderado",
     "capital":50000,
     "email":"cliente@email.com"
}'
```

---

# 📄 Licença

MIT License

Este projeto pode ser utilizado para fins acadêmicos, estudos, demonstrações e evolução futura.

---

# 👨‍💻 Autor

**Marinaldo da Silva Souza**

Assistente II | Automação | Linux | OpenShift | JBoss | n8n | IA Generativa

---

# 📈 Roadmap

## Versão 2.0

- Integração com WhatsApp
- Dashboard Power BI
- Agente financeiro via Telegram
- Geração automática de PDFs
- Histórico de recomendações
- Banco de dados PostgreSQL
- Integração com corretoras

---

# 🧪 Testes

Para validar o Webhook:

```bash
curl -X POST https://n8n.seudominio.com/webhook/investimentos \
-H "Content-Type: application/json" \
-d '{
     "nome":"Marinaldo",
     "perfil":"moderado",
     "capital":50000,
     "email":"cliente@email.com"
}'
```

---

# 📄 Licença

MIT License

Este projeto pode ser utilizado para fins acadêmicos, estudos, demonstrações e evolução futura.

---

# 👨‍💻 Autor

**Marinaldo da Silva Souza**

Assistente II | Automação | Linux | OpenShift | JBoss | n8n | IA Generativa

---
