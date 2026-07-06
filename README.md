# Produto de Dados para Análise e Previsão de Conversão de Leads em Cursos

Este projeto tem como objetivo desenvolver uma solução de dados para analisar, priorizar e prever a conversão de leads em uma empresa fictícia de cursos e educação profissional.

A proposta é simular um problema comum para times de marketing e comercial: empresas recebem muitos leads por diferentes canais, mas nem todos possuem a mesma chance de conversão. Com isso, o projeto busca transformar dados em informações úteis para apoiar a tomada de decisão, entender padrões de conversão e priorizar melhor os contatos comerciais.

O projeto foi desenvolvido em etapas, começando por análise de dados e BI, avançando para modelos de Machine Learning e interpretação dos resultados.

---

## Objetivo do projeto

Construir um produto de dados capaz de apoiar marketing, comercial e gestão na análise de conversão de leads.

O projeto busca responder perguntas como:

- Qual é a taxa geral de conversão?
- Quais canais geram mais leads?
- Quais fontes possuem melhor taxa de conversão?
- Quais perfis e comportamentos aparecem com mais frequência entre os leads convertidos?
- É possível prever a probabilidade de conversão de um lead?
- Como um modelo de Machine Learning pode apoiar a priorização comercial?

---

## Contexto do problema

Empresas que trabalham com captação de leads recebem contatos por diferentes origens, como landing pages, formulários, campanhas, tráfego direto, busca orgânica, chat e outros canais.

O problema é que nem todos os leads estão no mesmo momento de decisão. Alguns possuem maior intenção de compra, enquanto outros ainda estão pesquisando, comparando opções ou precisam de nutrição.

Sem uma análise estruturada, o time comercial pode perder tempo com leads de baixa probabilidade de conversão ou deixar de priorizar contatos com maior potencial.

Este projeto busca apoiar esse processo com análise de dados, visualização, indicadores e modelos preditivos.

---

## Base de dados

A base utilizada foi o dataset **Lead Scoring X Education**, relacionado a uma empresa de educação online.

A base contém informações sobre leads, incluindo dados de origem, fonte, comportamento, perfil, qualidade e conversão.

Neste projeto, a variável principal é:

| Variável | Descrição |
|---|---|
| `Convertido` | Indica se o lead realizou conversão |
| `0` | Lead não convertido |
| `1` | Lead convertido |

---

## Visão geral da base

Após a etapa inicial de entendimento dos dados, foram identificados:

| Indicador | Valor |
|---|---:|
| Total de leads | 9.240 |
| Leads convertidos | 3.561 |
| Leads não convertidos | 5.679 |
| Taxa geral de conversão | 38,54% |

---

## Etapas do projeto

O projeto foi organizado em uma jornada de análise e modelagem:

1. Entendimento inicial da base
2. Limpeza e preparação dos dados
3. Análise exploratória
4. Construção do dashboard em Power BI
5. Modelagem de Machine Learning
6. Avaliação dos modelos
7. Criação de ranking de leads por probabilidade de conversão
8. Interpretação dos resultados
9. Documentação do projeto

---

## Ferramentas utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Google Colab
- Power BI
- GitHub
- Markdown
- CSV

---

## Estrutura do repositório

```text
previsao-conversao-leads-cursos/
│
├── dashboard/
│   ├── power_bi/
│   └── prints/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_entendimento_dados.ipynb
│   ├── 02_limpeza_preparacao_dados.ipynb
│   ├── 03_analise_exploratoria_mvp1.ipynb
│   └── 04_modelagem_machine_learning.ipynb
│
├── reports/
│   ├── images/
│   └── exports/
│
├── src/
│
└── README.md
