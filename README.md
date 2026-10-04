# Chat com IA em Streamlit

Este projeto é uma aplicação de chatbot em Python usando Streamlit e a API do Google Gemini. Ele foi criado para permitir conversas em tempo real com memória da sessão, em que o histórico da conversa é mantido enquanto a interface estiver aberta.

A ideia principal é oferecer uma experiência simples de chat, com um assistente que responde perguntas de forma conversacional, especialmente para assuntos de programação e tecnologia.

## Sobre o projeto

A aplicação inclui:

- interface web com Streamlit
- entrada de mensagens do usuário
- histórico de conversa em memória
- prompt orientado para responder como tutor de programação
- controle de temperatura do modelo para ajustar a criatividade da resposta
- botão para resetar o chat
- carregamento da API key via variável de ambiente ou secrets do Streamlit

## Estrutura do projeto

```bash
chat-streamlit-poc/
├── app.py
├── functions.py
├── requirements.txt
├── .env.example
├── README.md
```

## Requisitos

Antes de começar, você precisa ter instalado:

- Python 3.9+
- pip
- Git (opcional, para clonar o projeto)

## Como rodar o projeto

### 1. Clone o repositório

```bash
git clone <url-do-repositorio>
cd chat-streamlit-poc
```

### 2. Crie um ambiente virtual

No Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

No macOS/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Configure sua API key

Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

```env
API_KEY=sua_chave_aqui
```

Se estiver usando Streamlit Cloud, também é possível guardar a chave em `st.secrets["API_KEY"]`.

### 5. Execute a aplicação

```bash
streamlit run app.py
```

Depois disso, o Streamlit abrirá a aplicação no navegador, normalmente em:

```text
http://localhost:8501
```

## Como usar

1. Digite sua mensagem no campo de chat.
2. O assistente responderá com base no modelo do Gemini.
3. O histórico da conversa permanece visível durante a sessão.
4. Você pode clicar em "Reset chat" para limpar a conversa.

## Arquivos principais

- `app.py`: interface do chat e lógica da conversa
- `functions.py`: funções utilitárias, incluindo leitura da chave da API e reset do chat
- `requirements.txt`: dependências do projeto

## Créditos

Este projeto foi inspirado no tutorial:

Step-by-Step Guide to Build and Deploy an LLM-Powered Chat with Memory in Streamlit
https://towardsdatascience.com/step-by-step-guide-to-build-and-deploy-an-llm-powered-chat-with-memory-in-streamlit/

Crédito à criadora/Autora: Alessandra.

## Observação

Este projeto foi desenvolvido como exemplo educacional e pode ser adaptado para outros modelos de IA, integrações e cenários de uso.

## Licença

Este projeto é destinado apenas para fins educacionais e de demonstração.
