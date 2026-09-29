<img width="1341" height="742" alt="Image" src="https://github.com/user-attachments/assets/ac6894d2-c073-4110-a3c1-7f7ce9553df7" />

# 📊 Sales Dashboard — Power BI

Dashboard desenvolvido no Power BI para análise de vendas, faturamento e lucratividade a partir do dataset **Financial Sample**, disponibilizado pela Microsoft.

O projeto foi desenvolvido com foco em demonstrar conhecimentos práticos de **Power BI, Power Query, DAX, análise de dados e visualização de indicadores**.

## 🎯 Objetivo

Construir um dashboard simples e interativo capaz de responder perguntas como:

- Como o faturamento evolui ao longo do tempo?
- Quais segmentos apresentam maior faturamento?
- Quais países concentram maior faturamento?
- Quais produtos geram maior faturamento?
- Como analisar faturamento em conjunto com lucro e margem?
- Quais pontos podem ser investigados para apoiar futuras decisões comerciais e de estoque?

## 🛠️ Tecnologias utilizadas

- **Power BI Desktop**
- **Power Query**
- **DAX**
- Excel / Financial Sample
- Análise e visualização de dados

## 📌 Indicadores

O dashboard apresenta os seguintes KPIs:

- **Faturamento Total:** R$ 118,73 milhões
- **Lucro Total:** R$ 16,89 milhões
- **Unidades Vendidas:** 1,13 milhão
- **Margem de Lucro:** 14,23%

> Os valores acima correspondem ao conjunto de dados utilizado no projeto.

## 📈 Visualizações

O dashboard contém:

1. **Faturamento ao longo do tempo**
2. **Faturamento por segmento**
3. **Faturamento por país**
4. **Faturamento por produto**
5. **Filtros por ano, país e segmento**

Os filtros permitem analisar os indicadores sob diferentes contextos.

## 🔎 Principais análises

### Faturamento ao longo do tempo

A análise permite observar a evolução do faturamento entre os períodos disponíveis e investigar quais segmentos, países e produtos contribuíram para as variações observadas.

### Faturamento por segmento

O dashboard permite identificar os segmentos responsáveis pela maior parcela do faturamento.

Uma análise mais aprofundada deve comparar esses resultados com **lucro e margem de lucro**, pois maior faturamento não significa necessariamente maior rentabilidade.

### Faturamento por país

É possível identificar os países que concentram maior faturamento e comparar seu desempenho com outros mercados.

Países com menor faturamento não devem ser considerados automaticamente como problemáticos. É necessário investigar volume, lucro, margem e contexto comercial antes de concluir que existe uma oportunidade de melhoria.

### Faturamento por produto

O gráfico identifica os produtos que geram maior faturamento.

Importante: este projeto diferencia **faturamento** de **quantidade vendida**. Um produto com maior faturamento não necessariamente é o produto mais vendido em unidades.

Os resultados podem servir como ponto de partida para futuras análises de estoque e compras.

## 🧹 Tratamento dos dados

A preparação foi realizada no Power Query, incluindo:

- Verificação dos tipos de dados;
- Ajuste dos campos numéricos e de data;
- Remoção de colunas que não eram necessárias para o escopo inicial;
- Preparação dos dados para utilização no modelo do Power BI.

## 🧮 Medidas DAX

Principais medidas utilizadas:

```DAX
Faturamento Total = SUM(Financials[Sales])

Lucro Total = SUM(Financials[Profit])

Unidades Vendidas = SUM(Financials[Units Sold])

Margem de Lucro = DIVIDE([Lucro Total], [Faturamento Total])
```

Também foi utilizada uma medida de venda média por registro durante o desenvolvimento, mas ela não foi tratada como **Ticket Médio**, pois o dataset não possui um identificador de pedido que permita calcular o ticket médio real.

## 💡 Aprendizados

Durante o desenvolvimento foram praticados:

- Importação e preparação de dados;
- Power Query;
- Tipagem de dados;
- Criação de medidas DAX;
- `SUM`, `DIVIDE` e `COUNTROWS`;
- Formatação de indicadores;
- Contexto de filtro;
- Segmentadores;
- Construção de gráficos;
- Interpretação de indicadores;
- Diferenciação entre faturamento, lucro e margem.

## 📂 Estrutura do projeto

```text
powerbi-sales-dashboard/
│
├── README.md
│
├── images/
│   └── dashboard.png
│
└── docs/
    └── insights.md
```

O arquivo `.pbix` pode ser incluído na raiz do repositório:

```text
powerbi-sales-dashboard/
│
├── Sales_Dashboard.pbix
├── README.md
├── images/
│   └── dashboard.png
└── docs/
    └── insights.md
```

## 📊 Dataset

O projeto utiliza o **Financial Sample**, disponibilizado pela Microsoft.

O arquivo original não é incluído neste repositório. O objetivo é manter o projeto leve e direcionar o usuário para a fonte oficial do dataset.

## 🚀 Próximos passos

Possíveis evoluções deste projeto:

- Criar uma tabela calendário;
- Analisar faturamento e lucro por mês;
- Comparar lucro e margem por produto, país e segmento;
- Criar análise de crescimento percentual;
- Criar indicadores de participação no faturamento;
- Incluir análise de quantidade vendida por produto;
- Evoluir para um modelo dimensional mais completo.

---

**Projeto desenvolvido como parte da minha evolução prática em Análise de Dados e Power BI.**
