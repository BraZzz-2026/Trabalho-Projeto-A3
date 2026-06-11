# Projeto A3 – Agente Autônomo de IA para Clínica Odontológica

## Squad
[GRUPO 4]

Integrantes:
- Braz Moura 
- Nome 2
- Nome 3
- Nome 4
- Nome 5

---

# Problema Âncora

A Clínica Odontológica Sorriso Feliz possui dificuldades no gerenciamento de consultas, resultando em atrasos no atendimento, cancelamentos não registrados e grande volume de solicitações repetitivas feitas pelos pacientes.

O agente autônomo foi desenvolvido para automatizar o processo de atendimento, consulta de horários, agendamento e cancelamento de consultas, reduzindo o trabalho manual da recepção e melhorando a experiência do paciente.

---

# Solução Proposta

Foi desenvolvido um Agente Autônomo de IA utilizando n8n integrado ao Telegram e Google Sheets.

O agente é capaz de:

- Receber mensagens de texto pelo Telegram.
- Receber mensagens de áudio e realizar transcrição automática.
- Consultar horários disponíveis.
- Consultar consultas já agendadas.
- Realizar novos agendamentos.
- Cancelar consultas.
- Atualizar automaticamente a agenda da clínica.
- Encaminhar atendimentos complexos para um humano.
- Notificar o atendente quando necessário.

---

# Tecnologias Utilizadas

- n8n
- Google Gemini
- Telegram Bot API
- Google Sheets
- Google OAuth 2.0

---

# Arquitetura da Solução

Fluxo principal:

Telegram

↓

Recepção da Mensagem

↓

Transcrição de Áudio (quando necessário)

↓

Agente de IA (Gemini)

↓

Consulta Google Sheets

↓

Ação:
- Consultar
- Agendar
- Cancelar
- Encaminhar Humano

↓

Resposta ao Cliente

↓

Encaminha para Atendente
---

# Funcionalidades Demonstradas

## Consultar horários

Paciente:
"Quais horários estão disponíveis?"

O agente consulta a agenda e informa os horários livres.

---

## Agendar consulta

Paciente:
"Meu nome é Denis Moura, quero agendar dia 23/06 às 15h"

O agente verifica disponibilidade e registra o agendamento.

---

## Cancelar consulta

Paciente:
"Meu nome é João Silva e quero cancelar minha consulta"

O agente localiza o agendamento e altera o status para Livre.

---

## Encaminhamento Humano

Paciente:
"Quero remarcar minha consulta"

O agente informa que um atendente entrará em contato e envia uma notificação para a equipe.

---

# Como Importar o Workflow

1. Acesse o n8n.
2. Clique em Import Workflow.
3. Selecione o arquivo:

workflow_clinica_odontologica.json

4. Configure as credenciais necessárias.
5. Salve o workflow.
6. Execute o fluxo.

---

# Como Executar

1. Inicie o workflow no n8n.
2. Certifique-se de que o bot do Telegram está ativo.
3. Envie uma mensagem para o bot.
4. O agente processará automaticamente a solicitação.

---

# Variáveis de Ambiente

Utilize placeholders:

```env
GEMINI_API_KEY=SUA_CHAVE_API_AQUI

TELEGRAM_BOT_TOKEN=SEU_TOKEN_AQUI

GOOGLE_CLIENT_ID=SEU_CLIENT_ID_AQUI

GOOGLE_CLIENT_SECRET=SEU_CLIENT_SECRET_AQUI

GOOGLE_SHEET_ID=SEU_SHEET_ID_AQUI
```
