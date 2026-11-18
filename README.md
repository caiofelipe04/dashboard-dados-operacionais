# Dashboard-Dados-Operacionais

Dashboard de abordagens operacionais no Looker Studio, com dados coletados por Google Forms e organizados no Google Sheets.

> **Dados fictícios:** a base deste repositório foi gerada por script e mantém a estrutura da base real. O projeto é inspirado em um caso real, sem expor informações da empresa ou das pessoas envolvidas.

🔗 **[Abrir o dashboard interativo](https://datastudio.google.com/reporting/ddc1de6f-2510-4faa-98a6-2b43a5152661)**

[![Visão geral do dashboard](imagens/dashboard-geral.png)](https://datastudio.google.com/reporting/ddc1de6f-2510-4faa-98a6-2b43a5152661)

## Sobre o projeto

Ao ingressar na empresa, percebi que os dados operacionais estavam espalhados em várias planilhas e sistemas, o que dificultava transformá-los em informação para decisão. Conversei com a gerência e propus centralizá-los em um painel claro, para gestores e equipe operacional.

O painel permite acompanhar os indicadores por período, instrutor e tipo de abordagem, e responde:

- Quantas abordagens cada instrutor realizou por mês?
- Quais tipos de abordagem são mais frequentes?
- Quais motoristas são abordados mais de uma vez (reincidência)?
- Qual a adesão ao aplicativo e por que parte da equipe não o utiliza?

![Visão filtrada por instrutor](imagens/dashboard-por-instrutor.pdf)

## O que a análise mostra e o que fazer com isso

Interpretação dos dados fictícios (nov/2025 a out/2026). Os padrões são ilustrativos, o objetivo é mostrar como o painel vira decisão:

- **A reincidência está concentrada em poucos motoristas.** Um deles foi abordado 27 vezes, mais que o dobro do segundo (13). *Ação:* acompanhamento individual desses casos, em vez de repetir a mesma abordagem.
- **Dois tipos de abordagem somam cerca de 55% do total:** "Excesso de velocidade" (29,3%) e "Frenagem brusca" (25,6%). *Ação:* priorizar esses temas nos treinamentos.
- **O maior motivo isolado para não usar o aplicativo é desconhecimento** (64 dos 229 casos sem uso). *Ação:* divulgação e orientação inicial tendem a ter mais efeito do que suporte técnico, que fica para senha (54) e cadastro (22).
- **O instrutor C fez menos abordagens (166) que A e B (265 e 269).** Pode refletir menos dias dedicados a abordagem. *Ação:* antes de comparar desempenho, normalizar as abordagens pelos dias trabalhados.

## Tecnologias

Google Forms (coleta) → Google Sheets (base de dados) → Looker Studio (dashboard). Python para gerar os dados fictícios.

## Estrutura do repositório

```
├── dados/abordagens_ficticias.csv       # base fictícia do dashboard
├── scripts/gerar_dados_ficticios.py     # script que gera o CSV
├── imagens/                             # prints do dashboard
├── docs/dicionario-de-dados.md          # descrição das colunas e indicadores
└── README.md
```

## Como reproduzir

1. Rode `scripts/gerar_dados_ficticios.py` (ou use o CSV que já está em `dados/`).
2. Importe o CSV em uma planilha do Google Sheets.
3. Conecte a planilha ao Looker Studio e monte os gráficos.

## Status

Versão com dados fictícios concluída.

---

**Caio Felipe** · [LinkedIn](https://www.linkedin.com/in/caiofelipez)
