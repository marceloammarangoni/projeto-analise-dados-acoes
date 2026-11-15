# 📈 Análise de Operações do Mercado de Ações

Projeto de análise de dados desenvolvido como parte do curso **Profissão: Analista de Dados**, utilizando uma base fictícia de 2.000 operações de compra e venda de ações realizadas por 100 clientes ao longo de 2023.

O objetivo foi aplicar, na prática, técnicas de organização, limpeza, análise estatística, projeção e visualização de dados em uma planilha do Google Sheets.

## 🗂️ Estrutura do arquivo

| Aba | Conteúdo |
|---|---|
| `mercado_acoes` | Base de dados original (código e e-mail do cliente, tipo de operação, ticker, preço, data), com colunas derivadas de dia/mês/ano e preço normalizado |
| `estatística` | Estatísticas descritivas do preço das operações (soma, mínimo, máximo, média, mediana, moda, variância e desvio padrão), além de busca de cliente por código |
| `cliente` | Painel de consulta por e-mail ou código do cliente: contagem, soma e média de operações, com classificação automática de perfil (Conservador / Moderado / Agressivo) |
| `tendência_temporal` | Quantidade de operações por mês, previsão do volume do mês 12 com base nos 11 meses anteriores e cálculo do erro da previsão |
| `compra_venda` | Tabela dinâmica com quantidade e valor total de operações de compra vs. venda |
| `cliente_compra_venda` | Tabela dinâmica com quantidade e valor total de compra/venda por cliente |
| `cliente_lucro_prejuízo` | Tabela dinâmica de lucro (venda − compra) por ticker, com filtros por cliente e por ativo |
| `gráficos` | Painel único reunindo os 6 gráficos do projeto, um de cada aba de análise |

## 🛠️ Técnicas e ferramentas aplicadas

- **Tratamento de dados**: ajuste de tipos de coluna, normalização Min-Max do preço, extração de dia/mês/ano a partir da data
- **Estatística descritiva**: soma, mínimo, máximo, média, mediana, moda, variância e desvio padrão
- **Fórmulas**: `PROCV` com tratamento de erro (`SEERRO`), `CONT.SE`, `SOMASE` e `MÉDIASE`
- **Séries temporais**: contagem de operações por mês e previsão linear (`PREVISÃO`) com cálculo do erro em relação ao valor real
- **Tabelas dinâmicas**: cruzamento de operação × cliente × ticker, com filtros
- **Boas práticas de planilha**: formatação condicional, proteção de células com fórmulas, visualizações de filtro
- **Visualização de dados**: 6 gráficos (colunas, linhas, pizza, barras, colunas empilhadas e dispersão), cada um com tipo e propósito diferente

## 📊 Principais insights

- Total de 2.000 operações, divididas entre 1.018 compras e 982 vendas, somando R$ 50.905,24 em valor negociado
- A previsão do volume de operações do mês 12 (172) ficou 15 operações abaixo do valor real (187)
- Análise de lucro por cliente e ticker permite identificar rapidamente operações lucrativas ou deficitárias

## 📁 Arquivos neste repositório

- `operacoes_mercado_acoes.xlsx` — planilha completa, com fórmulas, tabelas dinâmicas e gráficos
- `operacoes_mercado_acoes - mercado_acoes.csv` — dados brutos da base de operações

## 🎓 Contexto

Projeto desenvolvido durante minha transição de carreira para a área de Análise de Dados, aplicando os conceitos do módulo de planilhas do curso **Profissão: Analista de Dados**.

