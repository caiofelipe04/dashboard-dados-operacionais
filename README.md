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

![Visão filtrada por instrutor](imagens/dashboard-por-instrutor.png)

## Principais conclusões

Leitura do painel com dados fictícios, no período de nov/2025 a out/2026 (700 abordagens, 250 motoristas):

- Os instrutores B e A concentram a maior parte das abordagens (269 e 265), contra 166 do instrutor C.
- "Excesso de velocidade" é o tipo mais frequente (29,3%), seguido de "Frenagem brusca" (25,6%).
- Um motorista foi abordado 27 vezes, mais que o dobro do segundo da lista (13).
- 67,3% das abordagens são de motoristas que usam o aplicativo. Entre os que não usam, o motivo mais comum é "Não conhecia o aplicativo" (64 casos).

## Tecnologias

Google Forms (coleta) → Google Sheets (base de dados) → Looker Studio (dashboard). Python para gerar os dados fictícios.

## Estrutura do repositório

```
├── dados/abordagens_ficticias.csv       # base fictícia do dashboard
├── scripts/gerar_dados_ficticios.py     # script que gera o CSV
├── imagens/                             # prints do dashboard
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
