# 🔄 Fluxo de Automação – RD Station  
**Captação e Nutrição de Leads | Setor de Planos de Saúde**

---

## 🎯 Objetivo do Fluxo

Este fluxo de automação foi estruturado para simular um cenário real de **captação, nutrição e qualificação de leads** no setor de planos de saúde, priorizando eficiência operacional e organização dos dados.

Os principais objetivos são:

- Captar leads interessados em planos de saúde
- Responder rapidamente ao interesse do usuário
- Nutrir o lead com informações relevantes e educativas
- Identificar leads com maior intenção de compra
- Organizar e preparar os dados para o time comercial

📌 **Foco:** eficiência, organização e rastreabilidade — aspectos altamente valorizados no setor de saúde.

---
![alt text](<../prints/fluxo de automacao RD.png>)
## 🧩 Visão Geral do Fluxo

Formulário preenchido
↓
E-mail automático de confirmação
↓
Lead entra em fluxo de nutrição
↓
Segmentação por interesse
↓
Identificação de engajamento
↓
Lead marcado como qualificado
↓
Envio para controle / time comercial

---

## 🔹 Etapa 1 – Entrada do Fluxo (Gatilho)

### 📥 Gatilho
- Preenchimento de formulário em landing page
 ![alt text](<../prints/formulario rd capta dados .png>)
**Exemplo de landing page:**  
> *“Simule seu plano de saúde”*

### 📝 Campos do Formulário
- Nome
- E-mail
- Telefone
- Tipo de plano de interesse:
  - Individual
  - Familiar
  - Empresarial

![alt text](<../prints/botão de confirmação formulario Rd -- SEGMENTAR PERFIL .png>)
--- 
Esta etapa foi substituida por um formulário próprio, devido a que o tempo de uso gratuito do Rd esgotou, assim criei um botão (para segmentar n N8N) - 
 ### botão final:
 ![alt text](<../prints/captação de e-mail propro .png>)

## 🔹 Etapa 2 – E-mail Automático de Confirmação

### ✉️ Ação
- Envio automático de e-mail imediatamente após o preenchimento do formulário

### 🎯 Objetivos
- Confirmar o recebimento da solicitação
- Criar confiança no processo
- Reduzir a ansiedade do lead

---

## 🔹 Etapa 3 – Inclusão em Fluxo de Nutrição

### 🔄 Ação
- Adicionar o lead a um fluxo curto de nutrição 

### 🎯 Objetivo
- Educar o lead antes do contato comercial

### 📚 Conteúdos Típicos (e-mails que poderiam ser enviados pelo fluxo)

- **E-mail 1 (D+2)**  
  *O que avaliar antes de contratar um plano de saúde*

- **E-mail 2 (D+4)**  
  *Diferença entre planos individuais, familiares e empresariais*

- **E-mail 3 (D+6)**  
  *Como funcionam carência e cobertura*

---

## 🔹 Etapa 4 – Segmentação por Interesse

### 🏷️ Ação
- Aplicação de **tags ou campos personalizados** com base nas respostas do formulário

### 🎯 Exemplos de Segmentação
- Interesse: Plano Individual
- Interesse: Plano Familiar
- Interesse: Plano Empresarial

📌 A segmentação é essencial para personalização de comunicação e análise de métricas.
- a ideia era captar isso pelo Rd- por fim tentei pelo N8N (ainda testando possibilidades)
---

## 🔹 Etapa 5 – Identificação de Engajamento

### 📊 Regra Simples de Qualificação
O lead é considerado engajado se:

- Abriu pelo menos **1 e-mail**
- **OU** clicou em algum link
- **OU** visitou a página *“Planos”*

### 🏷️ Ação
- Aplicar a tag:  
  **Lead Engajado**

📌 Esta etapa simula o início do conceito de **MQL (Marketing Qualified Lead)**.

---

## 🔹 Etapa 6 – Marcação de Lead Qualificado

### ✅ Critérios Simples (comuns em médias empresas)
- Lead engajado
- Interesse claramente definido
- Dados de contato completos

### 🏷️ Ação
- Aplicar a tag:  
  **Lead Qualificado – Marketing**

---

## 🔹 Etapa 7 – Integração / Saída do Fluxo

### 🔄 Ação Final
Após a qualificação, o lead pode ser direcionado para:

- Controle em planilha
- Integração via **n8n**
- Fila de contato do time comercial

---

## 📊 Métricas Acompanhadas no RD Station 

- Número de leads captados
- Taxa de abertura de e-mails
- Taxa de cliques
- Quantidade de leads engajados
- Quantidade de leads qualificados

---
