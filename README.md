# Criando-processo-de-rpa-com-n8n-python
Projeto final

🛠 Tecnologias Utilizadas
Automação
n8n
Webhooks
HTTP Request Nodes
Merge Node
Code Node
Inteligência Artificial
OpenAI GPT
Gemini
LangChain (opcional)
Backend
Python 3.11+
Dados Financeiros
Yahoo Finance API
Alpha Vantage (opcional)
Status Invest (opcional)
Comunicação
Gmail API
SMTP
Hospedagem
Docker
VPS Linux
Google Cloud
AWS
Azure
📂 Estrutura do Projeto
Plain Text
investimento-ai-rpa/
│
├── README.md
│
├── n8n/
│ ├── workflow.json
│ └── screenshots/
│
├── python/
│ ├── investment_analyzer.py
│ ├── financial_service.py
│ ├── email_service.py
│ └── requirements.txt
│
├── prompts/
│ ├── investment_prompt.txt
│ ├── email_prompt.txt
│ └── analyst_prompt.txt
│
├── docs/
│ ├── arquitetura.png
│ ├── fluxo-mvp.png
│ └── diagrama-sequencia.png
│
├── examples/
│ ├── request.json
│ └── response.json
│
└── logs/
└── execution.log
🚀 Fluxo Completo da Automação
Etapa 1 - Recebimento dos Dados

O usuário envia uma requisição para o Webhook do n8n.

Exemplo
JSON
{
"nome": "Marinaldo",
"email": "marinaldo@email.com",
"perfil": "moderado",
"capital": 50000,
"objetivo": "aposentadoria"
}
Etapa 2 - Consulta de Mercado

O workflow consulta ativos previamente definidos.

Exemplo:

Plain Text
PETR4
VALE3
ITUB4
BBAS3
BOVA11
TESOURO SELIC

Retorno:

JSON
{
"PETR4": 37.50,
"VALE3": 65.80,
"ITUB4": 35.40
}
Etapa 3 - Análise em Python

O script realiza:

Identificação do perfil;
Classificação de risco;
Distribuição recomendada;
Percentuais sugeridos;
Validação dos dados.

Exemplo:

Python
{
"perfil":"moderado",
"renda_fixa":50,
"acoes":40,
"fundos_imobiliarios":10
}
Etapa 4 - Processamento com IA

A IA recebe:

Perfil do investidor;
Capital disponível;
Objetivo financeiro;
Cotação dos ativos.

Prompt:

Plain Text
Analise os dados do investidor e gere uma recomendação
financeira clara, objetiva e em linguagem acessível.
Etapa 5 - Construção do Relatório

Exemplo:

HTML
<h2>Relatório de Investimentos</h2>
 
<p>Perfil: Moderado</p>
 
<p>Capital: R$ 50.000</p>
 
<h3>Distribuição sugerida</h3>
 
<ul>
<li>50% Renda Fixa</li>
<li>40% Ações</li>
<li>10% Fundos Imobiliários</li>
</ul>
Etapa 6 - Envio por E-mail

O Gmail envia automaticamente o relatório para o cliente.

Assunto:

Plain Text
Relatório Personalizado de Investimentos
🔑 Configuração das Credenciais
OpenAI

Criar variável:

Plain Text
env não tem suporte total. O realce de sintaxe é baseado em Plain Text.
OPENAI_API_KEY=xxxxxxxxxxxxxxxx
Gmail

Configurar OAuth2:

Plain Text
env não tem suporte total. O realce de sintaxe é baseado em Plain Text.
GMAIL_CLIENT_ID=
GMAIL_CLIENT_SECRET=
GMAIL_REFRESH_TOKEN=
Yahoo Finance

Caso a API utilizada exija autenticação:

Plain Text
env não tem suporte total. O realce de sintaxe é baseado em Plain Text.
YAHOO_API_KEY=
🐍 Ambiente Python
Instalação
Shell
git clone https://github.com/seuusuario/investimento-ai-rpa.git
 
cd investimento-ai-rpa
 
python -m venv venv
 
source venv/bin/activate

Linux:

Shell
source venv/bin/activate

Windows:

Shell
venv\Scripts\activate

Instalar dependências:

Shell
pip install -r requirements.txt
📦 requirements.txt
Plain Text
requests
pandas
numpy
openai
python-dotenv
yfinance
▶️ Executando Localmente

Executar análise:

Shell
python investment_analyzer.py

Resultado esperado:

JSON
{
"perfil": "moderado",
"risco": "medio",
"recomendacao": "Carteira balanceada"
}
🔄 Importando o Workflow no n8n
Acessar o n8n.
Selecionar "Import Workflow".
Escolher o arquivo:
Plain Text
n8n/workflow.json

Configurar:

Credencial OpenAI
Credencial Gmail
APIs financeiras
Webhook

Ativar o fluxo.

📊 Exemplo de Entrada
JSON
{
"nome": "Marinaldo",
"perfil": "moderado",
"capital": 50000,
"objetivo": "crescimento patrimonial",
"email": "cliente@email.com"
}
📈 Exemplo de Saída
JSON
{
"perfil":"moderado",
"recomendacao":"Carteira equilibrada",
"renda_fixa":"50%",
"acoes":"40%",
"fiis":"10%"
}
🔐 Segurança

Boas práticas:

Utilizar HTTPS.
Nunca armazenar chaves em código.
Utilizar variáveis de ambiente.
Restringir acesso aos Webhooks.
Configurar autenticação OAuth2.
Implementar logs de auditoria.
Criptografar backups.
📋 Possíveis Evoluções
Versão 2.0
Integração com WhatsApp.
Dashboard em Power BI.
Integração com bancos.
Chatbot financeiro.
Análise técnica automática.
Geração de PDFs.
Agenda automática de reuniões.
📄 Licença

MIT License

👨‍💻 Autor

Projeto desenvolvido para fins de estudo e demonstração de automações inteligentes utilizando:

n8n
Python
IA Generativa
APIs Financeiras
Gmail API
