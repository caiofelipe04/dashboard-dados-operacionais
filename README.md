# Dashboard-Dados-Operacionais

Dashboard de indicadores operacionais construído no Looker Studio, a partir de dados coletados por um Google Forms e organizados no Google Sheets.

> **Aviso:** os dados deste repositório são **fictícios**, gerados por script, e mantêm a mesma estrutura da base real. O projeto foi inspirado em um caso real de acompanhamento de abordagens operacionais, sem expor nenhuma informação da empresa ou das pessoas envolvidas.

🔗 **Dashboard interativo:** [link público do Looker Studio(Em andamento)]

![Visão geral do dashboard](imagens/dashboard-geral.png)

---

## Contexto e motivação

Ao ingressar na empresa, identifiquei oportunidades de melhoria na forma como os dados operacionais eram organizados, visualizados e interpretados. A existência de diversas planilhas e sistemas dificultava a compreensão de determinadas informações e tornava mais desafiador transformar os dados em informações úteis para a tomada de decisão.

A partir dessa observação, conversei com a gerência sobre a possibilidade de tornar essas informações mais claras, acessíveis e organizadas, tanto para os gestores quanto para a equipe operacional.

## Objetivo

Desenvolver um dashboard de indicadores operacionais no Looker Studio, conectado a uma base no Google Sheets alimentada por respostas de um Google Forms preenchido pela equipe operacional.

A proposta é centralizar a visualização dos dados, facilitar o acompanhamento dos indicadores e permitir análises por período, instrutor e categoria, contribuindo para a identificação de tendências e oportunidades de melhoria nos processos.

## Perguntas que o dashboard responde

- Quantas abordagens cada instrutor realizou por mês?
- Quais são os tipos de abordagem mais frequentes?
- Quantas vezes a mesma pessoa foi abordada (reincidência)?
- Qual a adesão ao aplicativo utilizado pela equipe e quais os motivos de quem não utiliza?

## Principais conclusões

> Preencher depois de montar o painel com os dados fictícios, com 3 a 5 conclusões objetivas. Exemplo de formato:
>
> - O tipo de abordagem **[X]** representa **[N]%** do total.
> - **[N]** pessoas foram abordadas mais de uma vez no período.
> - O instrutor **[X]** concentrou **[N]%** das abordagens no mês de **[Y]**.

## Fluxo dos dados

```
Google Forms  →  Google Sheets  →  Looker Studio
(coleta)         (base de dados)    (dashboard)
```

Neste repositório, o Google Forms é substituído por um script em Python que gera dados fictícios, salvos em CSV e importados no Google Sheets.

## Tecnologias utilizadas

- **Google Forms:** coleta de informações operacionais.
- **Google Sheets:** armazenamento e organização inicial dos dados.
- **Google Looker Studio:** visualização de indicadores e construção do dashboard.
- **Python:** geração dos dados fictícios para este repositório.

## Estrutura do repositório

```
Dashboard-Dados-Operacionais/
├── README.md
├── dados/
│   └── abordagens_ficticias.csv      # base fictícia usada no dashboard
├── scripts/
│   └── gerar_dados_ficticios.py      # script que gera o CSV
├── imagens/
│   ├── dashboard-geral.png           # visão geral do painel
│   └── dashboard-por-instrutor.png   # visão por instrutor
└── docs/
    └── dicionario-de-dados.md        # descrição de cada coluna da base
```

## Como reproduzir

1. Execute o script `scripts/gerar_dados_ficticios.py` para gerar o arquivo CSV (ou use o que já está em `dados/`).
2. Importe o CSV em uma planilha do Google Sheets.
3. No Looker Studio, crie uma nova fonte de dados conectada a essa planilha.
4. Monte os gráficos conforme as perguntas listadas acima.

## Status do projeto

Em desenvolvimento, com foco na organização dos dados, criação de indicadores e melhoria da visualização das informações operacionais.

| Etapa | Situação |
|---|---|
| Coleta via Google Forms e organização no Google Sheets | ✅ Implementado |
| Dashboard no Looker Studio com indicadores por período, instrutor e categoria | 🔄 Em desenvolvimento |
| Versão com dados fictícios para este repositório | 🔄 Em desenvolvimento |
| Envio periódico de informações por e-mail aos instrutores | 📌 Planejado |

> Funcionalidades planejadas são identificadas separadamente das já implementadas.

## Próximos passos

- Automatizar o envio periódico de informações por e-mail aos instrutores, reduzindo tarefas manuais e facilitando o acesso aos dados relevantes.

## Autor

**[Caio Felipe]**
[www.linkedin.com/in/caiofelipez]
