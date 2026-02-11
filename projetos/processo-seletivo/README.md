# 📋 Automação de Processo Seletivo com n8n

Este projeto demonstra a automação de um processo seletivo utilizando o **n8n**, desde a leitura dos candidatos até a comunicação automática dos resultados.

## 🚀 Objetivo
Automatizar tarefas repetitivas de um processo seletivo, reduzindo esforço manual e garantindo padronização na comunicação com candidatos.

## 🔄 Fluxo do Processo
1. Disparo automático em data e horário definidos
2. Leitura dos candidatos em uma planilha do Google Sheets
3. Avaliação automática dos critérios:
   - Mais de 5 anos de experiência
   - Ensino superior completo
4. Envio de e-mail de aprovação para candidatos elegíveis
5. Consolidação dos candidatos reprovados
6. Envio de lista de reprovados ao recrutador

## 🧠 Tecnologias Utilizadas
- n8n
- Google Sheets
- SMTP (e-mail)
- Automação de workflows

## ⚙️ Como utilizar
1. Instale o n8n
2. Importe o arquivo `processo_seletivo_n8n.json`
3. Configure:
   - Credenciais do Google Sheets
   - Credenciais SMTP
4. Substitua os placeholders:
   - `GOOGLE_SHEETS_ID_AQUI`
   - E-mails de exemplo
5. Ative o workflow

## 🔐 Segurança
- Nenhuma credencial real é versionada
- Todos os dados sensíveis foram substituídos por placeholders
- Os e-mails e valores utilizados são apenas ilustrativos

## 💼 Diferencial QA
O fluxo foi pensado com foco em:
- Controle de volume (Split in Batches)
- Evitar spam/rate limit (Wait)
- Clareza de regras de negócio
- Facilidade de manutenção e testes

---

📌 Projeto desenvolvido como parte de estudos em automação com n8n.

<img width="2048" height="950" alt="image" src="https://github.com/user-attachments/assets/98b355ee-2304-4e2a-ad90-f38bdf17e972" />


