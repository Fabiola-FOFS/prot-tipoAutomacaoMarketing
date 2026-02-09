# 🚀 Protótipo de Automação de Marketing – Captação e Segmentação de Leads

Este repositório documenta um **protótipo funcional de automação de marketing**, desenvolvido com foco em **captação, segmentação e rastreabilidade de leads**, integrando **WordPress**, **HTML estático (GitHub Pages)**, **n8n** e **Google Sheets**.

O projeto simula um **funil real de marketing digital para planos de saúde**, demonstrando domínio de:
- Jornada do lead
- Automação no-code / low-code
- Integrações via Webhook
- Organização de dados para o time comercial

---

## 🎯 Objetivo do Protótipo

- Captar leads interessados em planos de saúde
- Confirmar e registrar e-mails fora de plataformas pagas
- Aplicar um **simulado de perfil**
- Segmentar leads automaticamente com base no resultado
- Armazenar dados estruturados em Google Sheets
- Garantir **rastreabilidade ponta a ponta**

> ⚠️ Observação: o RD Station foi utilizado apenas como referência conceitual, pois o plano gratuito não permite mais acesso a formulários e automações. A solução foi adaptada para um fluxo **100% funcional sem ferramentas pagas**.

---

## 🧩 Visão Geral da Arquitetura

WordPress (Landing Page)
↓
Página de Confirmação de E-mail (HTML)
↓
Webhook n8n – Captura de E-mail
↓
Página do Simulado
↓
Página de Resultado
↓
Webhook n8n – Resultado do Perfil
↓
Google Sheets (Base de Leads)

---

## 🌐 Páginas do Protótipo (Fluxo do Lead)

### 1️⃣ Landing Page – WordPress

📍 **URL:**  
https://planodesaudeprototipo.rf.gd/

**Função:**
- Apresentar o serviço
- Gerar interesse inicial
- Direcionar o usuário para confirmação de e-mail

> Esta página simula o papel de uma landing page comercial tradicional.

---

### 2️⃣ Confirmação de E-mail + Entrada no Funil

📍 **URL:**  
https://fabiola-fofs.github.io/prot-tipoAutomacaoMarketing/

**Função:**
- Coletar o e-mail do lead
- Enviar os dados para o n8n via **Webhook (POST)**
- Redirecionar o lead para o simulado

📌 **Tecnologia usada:**
- HTML + JavaScript
- Webhook n8n (`/webhook/captura-email`)

📤 Dados enviados:
```json
{
  "email": "lead@email.com"
}
3️⃣ Simulado de Perfil

Função:

Avaliar o comportamento e as prioridades do lead

Classificar em um dos perfis:

Básico

Intermediário

Completo

O resultado é passado como parâmetro de URL para a página final.

4️⃣ Página de Resultado + Segmentação

Função:

Exibir o resultado personalizado ao usuário

Enviar email + perfil para o n8n

Consolidar a segmentação do lead

📤 Webhook de saída:

{
  "email": "lead@email.com",
  "perfil": "intermediario"
}


Webhook utilizado:

/webhook/resultado-simulador

🔄 Automação no n8n

O n8n é responsável por:

Receber dados via Webhook

Validar informações

Unificar o fluxo (email + perfil)

Enviar os dados para o Google Sheets

Webhooks utilizados:
Webhook	Função
captura-email	Registra o e-mail inicial do lead
resultado-simulador	Registra perfil e consolida a segmentação
📊 Armazenamento – Google Sheets

O Google Sheets funciona como:

Base de leads

Histórico de segmentação

Fonte para análises futuras (CRM, BI, remarketing)

Campos armazenados:

Email

Perfil do lead

Data de entrada

Origem (simulado)

📁 Como Ler Este Repositório

Sugestão de leitura:

1️⃣ Entenda o fluxo no README
2️⃣ Analise os arquivos HTML das páginas intermediárias
3️⃣ Observe como os parâmetros de URL são utilizados
4️⃣ Veja como os Webhooks substituem ferramentas pagas
5️⃣ Avalie a rastreabilidade completa do lead

🚧 Próximas Evoluções (Ideias)

Envio automático de e-mails segmentados

Integração com CRM

Dashboard de métricas

Lead scoring

SEO técnico + eventos de conversão

👩‍💻 Autora

Fabiola Oliveira
Estudante de Análise e Desenvolvimento de Sistemas
Foco em Qualidade, Automação, Processos e Marketing Digital