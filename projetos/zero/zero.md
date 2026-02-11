# ZERO

Criar um projeto **do zero com o n8n** é mais simples do que parece 🙂
Um **passo a passo**, desde a instalação até o primeiro workflow funcionando.

---

## 1️⃣ O que é o n8n

O **n8n** é uma ferramenta de **automação de workflows** (tipo Zapier, mas open-source).
Você cria fluxos conectando nós (nodes) para integrar APIs, bancos de dados, IA, e muito mais.

---

## 2️⃣ Escolhendo como instalar o n8n

Você tem 3 opções principais. Para começar, recomendo **Docker** ou **n8n Cloud**.

### Opção A — n8n Cloud (mais fácil)

* Acesse: [https://n8n.io](https://n8n.io)
* Crie uma conta
* Já vem tudo pronto (sem instalação)
  ✔ Ideal para iniciantes

---

### Opção B — Docker (recomendado para projetos reais)

Pré-requisitos:

* Docker instalado

Crie uma pasta para o projeto:

```bash
mkdir n8n && cd n8n
```

Crie um arquivo `docker-compose.yml`:

```yaml
version: "3"

services:
  n8n:
    image: n8nio/n8n
    ports:
      - "5678:5678"
    volumes:
      - ./n8n_data:/home/node/.n8n
    environment:
      - N8N_BASIC_AUTH_ACTIVE=true
      - N8N_BASIC_AUTH_USER=admin
      - N8N_BASIC_AUTH_PASSWORD=senha_forte
```

Suba o n8n:

```bash
docker-compose up -d
```

Acesse no navegador:

```
http://localhost:5678
```

---

### Opção C — NPM (não recomendado para produção)

```bash
nvm install 22
npx n8n
```

Resposta:

```bash
Registered runner "JS Task Runner" (Ly7GeedjFboZx314iUOJT) 
Version: 2.7.4

Editor is now accessible via:
http://localhost:5678

Press "o" to open in Browser.
```

---

## 3️⃣ Criando o primeiro projeto (workflow)

No n8n, **projeto = workflow**.

### Passo 1: Criar workflow

* Clique em **“New Workflow”**
* Dê um nome (ex: `Primeiro Projeto n8n`)

---

### Passo 2: Escolher um gatilho (Trigger)

Todo workflow começa com um **Trigger**.

Exemplos comuns:

* **Manual Trigger** → para testes
* **Webhook** → receber dados externos
* **Cron** → rodar em horários
* **Trigger do WhatsApp, Telegram, Google Sheets, etc**

👉 Para começar:

* Adicione **Manual Trigger**

---

### Passo 3: Adicionar uma ação

Depois do trigger, adicione um nó de ação.

Exemplo simples:

1. Clique em **+**
2. Escolha **Set**
3. Crie um campo:

   * Nome: `mensagem`
   * Valor: `Olá, n8n funcionando!`

---

### Passo 4: Executar o workflow

* Clique em **Execute Workflow**
* Veja os dados passando entre os nós

🎉 Pronto! Seu primeiro projeto está funcionando.

---

## 4️⃣ Estrutura básica de um projeto n8n

Todo projeto segue este padrão:

```
Trigger
  ↓
Processamento (Set, IF, Function, Code)
  ↓
Integrações (API, Banco, WhatsApp, Email, IA)
```

---

## 5️⃣ Exemplo de projeto do zero (real)

### Exemplo: Receber um formulário e enviar email

**Workflow:**

1. Webhook (recebe dados)
2. IF (valida campos)
3. Set (organiza dados)
4. Email (envia mensagem)

---

## 6️⃣ Boas práticas desde o início

✔ Nomeie bem os nós
✔ Use comentários
✔ Teste com Manual Trigger
✔ Versione workflows importantes
✔ Use variáveis de ambiente para senhas

---

## 7️⃣ Próximo nível (quando quiser evoluir)

* Conectar APIs REST
* Usar OpenAI / IA
* Criar automações com WhatsApp
* Trabalhar com banco de dados
* Criar SaaS com n8n

---

Se quiser, posso:

* Criar **um projeto completo passo a passo**
* Montar **um fluxo para seu caso específico**
* Explicar **n8n + IA**
* Ajudar a **hospedar em produção**

👉 **Qual tipo de projeto você quer criar com n8n?**

