# Dicionário de dados

Descrição das colunas de `dados/abordagens_ficticias.csv` e dos indicadores calculados no painel. Todos os dados são fictícios.

## Colunas da base

| Coluna | Tipo | Descrição | Valores / exemplo |
|---|---|---|---|
| Carimbo de data/hora | Data e hora | Momento em que o registro foi preenchido (equivalente ao carimbo automático do Google Forms) | 12/03/2026 14:35:10 |
| Data da abordagem | Data | Dia em que a abordagem aconteceu | 12/03/2026 |
| Instrutor | Texto | Instrutor responsável pela abordagem | Instrutor A, B ou C |
| Chapa do motorista | Número | Código de identificação do motorista (fictício) | 1012 |
| Nome do motorista | Texto | Nome do motorista (fictício) | Carlos Silva |
| Tipo de abordagem | Texto | Categoria do motivo da abordagem | Excesso de velocidade, Frenagem brusca, Uso de celular, Cinto de segurança, Fadiga |
| Utiliza o aplicativo | Texto | Se o motorista utiliza o aplicativo da operação | Sim ou Não |
| Motivo se não utiliza | Texto | Motivo informado por quem não usa o aplicativo. Fica vazio quando a resposta anterior é "Sim" | Esqueceu a senha, Celular sem memória, Sem internet no celular, Não conhecia o aplicativo, Problema no cadastro |
| E-mail | Texto | E-mail de quem registrou a abordagem (fictício) | instrutor.a@exemplo.com |

## Indicadores do painel

| Indicador | Como é calculado |
|---|---|
| Total de abordagens | Contagem de registros (`Record Count`) no período filtrado |
| Motoristas únicos | Contagem distinta de `Chapa do motorista` |
| % usa o aplicativo | Proporção de abordagens com `Utiliza o aplicativo` = "Sim" |
| Média por instrutor | `Record Count / COUNT_DISTINCT(Instrutor)` |
| Quantas vezes foi abordado | Número de registros por motorista |

## Observações

- Um mesmo motorista pode aparecer em várias linhas, uma por abordagem. É isso que permite medir a reincidência.
- O gráfico mensal mostra os últimos 12 meses e não responde ao filtro de data da página.
- A base é gerada por `scripts/gerar_dados_ficticios.py`, com semente fixa, então o resultado é sempre o mesmo.
