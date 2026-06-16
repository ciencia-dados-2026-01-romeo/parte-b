# Projeto I - EDA: Análise de Séries Temporais da Inadimplência no Brasil

Parte B da disciplina de Ciência de Dados.

Este repositório reúne os artefatos da análise exploratória sobre a evolução da inadimplência no Brasil e sua relação com indicadores macroeconômicos, usando séries públicas do Banco Central do Brasil.

## Sumário das entregas

| Item | Entrega | Arquivo / link | Status |
| --- | --- | --- | --- |
| 2.1 | Notebook executável no Colab com as análises desenvolvidas | [`parte_b.ipynb`](parte_b.ipynb) | Entregue |
| 2.2 | Dados empregados no projeto | [`inadimplencia.json`](inadimplencia.json), [`selic.json`](selic.json), [`ipca.json`](ipca.json) | Entregue |
| 2.3 | Texto do trabalho com Introdução, Métodos e Resultados/Conclusão | [`ParteB.docx`](ParteB.docx) | Entregue |
| 2.4 | Vídeo de apresentação, com até 5 minutos | [YouTube](https://www.youtube.com/watch?v=oGvUtoClMmE) | Entregue |
| 2.4 | Slides empregados na apresentação | [`Analise-de-Series-Temporais-da-Inadimplencia-noBrasil.pptx`](Analise-de-Series-Temporais-da-Inadimplencia-noBrasil.pptx) | Entregue |
| 2.5 | README com sumário das entregas | [`README.md`](README.md) | Entregue |

## Autores

- João Paulo Bonagurio Ramirez - RA: 22.01247-8
- Lucas Olivares Borges da Silva - RA: 22.00889-6
- Luis Gustavo Machado - RA: 21.00322-0
- Tiago Tadeu de Azevedo - RA: 22.00856-0
- Victor Augusto de Gasperi - RA: 22.00765-2

## Tema

O trabalho investiga a evolução histórica da inadimplência no Brasil e sua relação com variáveis macroeconômicas relevantes. A análise considera a taxa de inadimplência, a taxa SELIC e o IPCA para observar tendências, correlações e possíveis defasagens entre o cenário econômico e a capacidade de pagamento.

As bases foram extraídas do Sistema Gerenciador de Séries Temporais (SGS) do Banco Central do Brasil e estão armazenadas no repositório em formato JSON:

| Variável | Código SGS | Arquivo | Período disponível no arquivo |
| --- | --- | --- | --- |
| Inadimplência | 21082 | [`inadimplencia.json`](inadimplencia.json) | mar/2011 a abr/2026 |
| SELIC | 4390 | [`selic.json`](selic.json) | ago/1986 a jun/2026 |
| IPCA | 433 | [`ipca.json`](ipca.json) | jan/1980 a mai/2026 |

No notebook, as séries são unificadas por data e filtradas para o período a partir de janeiro de 2011, mantendo apenas os meses com observações disponíveis nas três variáveis.

## Como executar o notebook

1. Abra o arquivo [`parte_b.ipynb`](parte_b.ipynb) no Google Colab.
2. Execute as células em ordem.
3. O notebook utiliza os pacotes:
   - `pandas`
   - `matplotlib`
   - `seaborn`
   - `requests`
4. As séries são consultadas pela API pública do Banco Central do Brasil e as bases utilizadas também estão disponíveis no repositório em formato JSON.

## Estrutura do repositório

```text
.
├── Analise-de-Series-Temporais-da-Inadimplencia-noBrasil.pptx # Slides da apresentação
├── ParteB.docx                                                # Texto do trabalho
├── README.md                                                  # Sumário e organização das entregas
├── inadimplencia.json                                         # Base de inadimplência do SGS/BCB
├── ipca.json                                                  # Base de IPCA do SGS/BCB
├── parte_b.ipynb                                              # Notebook com EDA e visualizações
└── selic.json                                                 # Base de SELIC do SGS/BCB
```

## Métodos empregados

A análise foi desenvolvida em Python, com foco em:

- consulta de séries temporais via API do SGS/BCB;
- tratamento e conversão de datas e valores numéricos;
- unificação das séries de inadimplência, SELIC e IPCA;
- recorte temporal a partir de janeiro de 2011;
- análise exploratória da evolução temporal das variáveis;
- visualização com gráfico de linhas e eixos duplos;
- matriz de correlação de Pearson para avaliar a associação linear entre as variáveis;
- visualizações com Matplotlib e Seaborn.

## Principais resultados

- A análise considera a inadimplência como indicador da saúde financeira de famílias e empresas.
- A série temporal permite observar períodos de pressão sobre a inadimplência em cenários de juros elevados.
- A SELIC aparece como uma variável relevante para interpretar o custo do crédito e possíveis aumentos no risco de atraso nos pagamentos.
- O IPCA ajuda a contextualizar a perda de poder de compra e seus efeitos sobre a capacidade de honrar dívidas.
- A matriz de correlação mostra a associação linear entre inadimplência, SELIC e IPCA no período analisado.
- O trabalho conclui que a inadimplência deve ser analisada como consequência das condições macroeconômicas, e não como fenômeno isolado.

## Referências

- Banco Central do Brasil. Sistema Gerenciador de Séries Temporais (SGS).
- Banco Central do Brasil. API de dados abertos do SGS/BCB.
- Documentação das bibliotecas Python utilizadas:
  - Pandas
  - Matplotlib
  - Seaborn
  - Requests