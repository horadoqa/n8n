# 🧪 Gerador de Massa de Teste para QA com n8n

Este projeto automatiza a criação de **massa de dados para testes**, resolvendo uma das tarefas mais repetitivas e chatas do dia a dia de QA.

O workflow foi desenvolvido utilizando **n8n** e gera usuários fictícios seguindo padrões reais de ambientes corporativos.

---

## 🎯 Problema

No dia a dia de QA, é comum precisar criar vários usuários de teste com:
- nomes fictícios
- e-mails padronizados
- CPF válido
- senha padrão definida pelo time

Fazer isso manualmente consome tempo e aumenta a chance de erro humano.

---

## ✅ Solução

Este workflow automatiza todo o processo:

- Geração automática de usuários
- E-mails no padrão corporativo (`nome.sobrenome+01@empresa.dev`)
- CPF **válido e formatado** (`XXX.XXX.XXX-XX`)
- Senha padrão fixa
- Exportação direta para **Google Sheets**, acessível por todo o time

---

## 🔄 Como funciona o fluxo

1. Execução manual do workflow
2. Definição da quantidade de usuários
3. Geração dos dados via JavaScript
4. Inserção automática dos dados no Google Sheets

---

## 🧠 Tecnologias utilizadas

- n8n
- JavaScript (Function/Code Node)
- Google Sheets
- Automação de workflows

---

## ⚙️ Como usar

### CLOUD

1. Acessar o site: [https://n8n.io](https://n8n.io)
2. Criar a conta
3. Salvar o email de cadastro. Padrão: <email>.iam.gserviceaccount.com para permitir a edição na planilha do excel.
4. Crie um Workflow
5. Importe o arquivo `gerador_massa_teste_qa.json`
6. Configure Credenciais
7. Execute o workflow e veja a planilha ser preenchida automaticamente

### LOCAL

1. Instale e execute o n8n

```bash
nvm install 22
npx n8n
```

> OBS.: Não recomendado para produção

2. Crie um Workflow
3. Importe o arquivo `gerador_massa_teste_qa.json`
4. Configure:
   - Credenciais do Google Sheets
5. Substitua no workflow:
   - `GOOGLE_SHEETS_ID_AQUI`
6. Execute o workflow e veja a planilha ser preenchida automaticamente

---

## 🔐 Segurança

- Nenhuma credencial real é versionada
- IDs e dados sensíveis foram substituídos por placeholders
- Os dados gerados são exclusivamente para ambientes de teste

---

## 💼 Contexto

Projeto desenvolvido com foco em **automação para QA**, aplicando n8n em problemas reais do cotidiano e buscando redução de esforço manual e aumento de qualidade nos testes.



