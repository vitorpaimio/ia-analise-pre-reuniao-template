# Relatório Técnico - Template de Análise Pré-Reunião com IA

**Projeto:** Automação de Análise Pré-Reunião com IA  
**Plataforma:** n8n + OpenAI/Anthropic + Pipedrive API  
**Versão:** 1.0  
**Autor:** Vitor Paim

---

## 1. Visão Geral

O objetivo desta automação é gerar **análises consultivas automáticas** antes de reuniões de vendas no CRM, fornecendo ao closer um resumo estratégico do lead com base em dados disponíveis no Pipedrive e informações públicas.

A solução combina automação via **n8n** e geração de texto com **IA generativa (OpenAI ou Anthropic)**, possibilitando a entrega de insights personalizados em poucos segundos.

---

## 2. Arquitetura da Solução

**Fluxo principal:**

1. **Entrada (Input)**
   - Trigger de deal no Pipedrive (novo negócio ou mudança de stage)
   - Captura de informações da organização e do contato

2. **Processamento**
   - Estruturação dos dados em JSON padronizado
   - Consulta a fontes externas (via API ou busca web)
   - Envio das informações para o modelo de IA

3. **Saída (Output)**
   - Geração de análise em HTML
   - Criação automática de nota dentro do deal no Pipedrive

**Componentes principais:**
- n8n (orquestração)
- Pipedrive API
- OpenAI GPT-4o ou Anthropic Claude
- Serper API (busca web opcional)

---

## 3. Funcionalidades

- Extração automática de dados de deals, organizações e contatos.  
- Geração de análises consultivas com base em IA.  
- Criação automática de notas formatadas no CRM.  
- Classificação de oportunidades com sistema de pontuação (score).  
- Redução de tempo de preparação pré-reunião em até 80%.

---

## 4. Tecnologias Utilizadas

| Componente | Descrição |
|-------------|------------|
| **n8n** | Plataforma de automação no-code usada para orquestrar o fluxo |
| **Pipedrive API** | Fonte de dados principal dos leads e negócios |
| **OpenAI / Anthropic** | Modelos de linguagem usados para análise e geração de texto |
| **Serper API (opcional)** | Realiza busca web para obter contexto atualizado |
| **HTML Notes** | Formato de saída otimizado para exibição no Pipedrive |

---

## 5. Benefícios da Automação

- **Preparação imediata:** Closers recebem contexto completo antes das reuniões.  
- **Padronização:** Todas as análises seguem estrutura e linguagem consistentes.  
- **Redução de custo operacional:** Menos tempo gasto com pesquisa manual.  
- **Integração nativa:** Executa dentro do ecossistema Pipedrive.  
- **Escalabilidade:** Pode ser replicado para múltiplas equipes e setores.

---

## 6. Requisitos Técnicos

- Conta no **n8n Cloud** ou servidor self-hosted  
- Acesso à **API do Pipedrive**  
- Chave de API da **OpenAI** ou **Anthropic**  
- (Opcional) Chave da **Serper API** para web search  

---

## 7. Estrutura do Repositório

ia-analise-pre-reuniao-template/
│
├── workflow/
│ └── ia-analise-pre-reuniao.json
│
├── docs/
│ └── relatorio_tecnico.md
│
├── assets/
│ └── fluxo.png
│
├── README.md
└── .gitignore
---

## 8. Métricas de Sucesso (exemplo de referência)

| Indicador | Antes | Depois |
|------------|--------|--------|
| Tempo médio de preparação | 15–20 min | < 2 min |
| Taxa de conversão | 35% | 50%+ |
| Casos com análise prévia | 0% | 100% |

---

## 9. Possíveis Extensões Futuras

- Envio de alertas via Slack ou e-mail quando a análise for criada.  
- Painel de métricas em tempo real com dados do Pipedrive.  
- Integração com Google Calendar para contexto de reuniões.  
- Geração automática de follow-up pós-reunião com IA.

---

## 10. Considerações Finais

O template demonstra o potencial de combinar automação (n8n) e inteligência artificial (LLM) para otimizar processos de vendas e CRM.  
Ele serve como **modelo base** para qualquer operação que deseje implementar análises automatizadas e contextuais em seus pipelines de vendas.

---

© 2025 | Desenvolvido por **Vitor Paim**
