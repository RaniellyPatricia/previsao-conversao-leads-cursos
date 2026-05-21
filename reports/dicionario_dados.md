# Dicionário de Dados — Base de Leads

## 1. Objetivo

Este documento descreve as colunas da base utilizada no projeto **Produto de Dados para Análise e Previsão de Conversão de Leads em Cursos**.

O objetivo do dicionário de dados é registrar o significado das variáveis, seus tipos esperados, possíveis usos analíticos e relação com a conversão dos leads.

Este documento será usado como apoio para:

- limpeza e padronização dos dados;
- análise exploratória;
- construção do dashboard do MVP 1;
- criação do score de priorização no MVP 2;
- seleção de variáveis para Machine Learning no MVP 3.

---

## 2. Variável principal do projeto

A variável principal do projeto é:

| Coluna | Tipo esperado | Significado | Uso no projeto | Relação com conversão |
|---|---|---|---|---|
| Convertido | Numérico / binário | Indica se o lead converteu ou não | Variável alvo do projeto | Relação direta. `1` representa lead convertido e `0` representa lead não convertido |

Nesta base:

| Valor | Significado |
|---|---|
| 0 | Lead não convertido |
| 1 | Lead convertido |

---

## 3. Dicionário das colunas

| Coluna | Tipo esperado | Significado | Possível uso no projeto | Relação com conversão |
|---|---|---|---|---|
| ID do Prospect | Texto | Identificador único do lead/prospect | Manter apenas como identificação | Não deve ser usado em gráficos, pois cada lead possui um ID único |
| Número do Lead | Numérico | Código numérico de identificação do lead | Identificação técnica do registro | Não deve ser usado como variável explicativa |
| Origem do Lead | Categórico | Indica a origem pela qual o lead entrou na base | Análise de volume e conversão por origem | Pode ajudar a identificar quais origens geram mais conversões |
| Fonte do Lead | Categórico | Canal ou fonte específica de aquisição do lead | Análise de canais de marketing | Pode indicar quais canais trazem leads mais qualificados |
| Não Enviar E-mail | Categórico / binário | Indica se o lead não deve receber e-mail | Análise operacional e restrição de contato | Pode impactar ações de nutrição e relacionamento |
| Não Ligar | Categórico / binário | Indica se o lead não deve receber ligações | Análise operacional e restrição comercial | Pode limitar abordagem do time comercial |
| Convertido | Numérico / binário | Indica se o lead realizou conversão | Indicador principal e variável alvo | É a variável central do projeto |
| Total de Visitas | Numérico | Quantidade total de visitas realizadas pelo lead | Análise de engajamento | Leads com mais visitas podem ter maior interesse |
| Tempo Total no Site | Numérico | Tempo total gasto pelo lead no site | Análise de comportamento e intenção | Maior tempo no site pode indicar maior interesse |
| Visualizações de Página por Visita | Numérico | Média de páginas visualizadas por visita | Análise de engajamento | Pode indicar profundidade de navegação e interesse |
| Última Atividade | Categórico | Última atividade registrada do lead | Análise de comportamento recente | Algumas atividades podem estar mais associadas à conversão |
| País | Categórico | País informado pelo lead | Análise geográfica | Pode ter uso limitado se houver muitos nulos ou concentração em uma região |
| Especialização | Categórico | Área de interesse ou especialização do lead | Análise de interesse por área/curso | Pode indicar quais áreas atraem leads com maior conversão |
| Como Soube da X Education | Categórico | Canal declarado pelo lead sobre como conheceu a empresa | Análise de aquisição declarada | Pode complementar análise de canais, mas exige cuidado com `Não informado` |
| Ocupação Atual | Categórico | Situação profissional atual do lead | Análise de perfil do público | Pode indicar perfis com maior propensão à conversão |
| O que Mais Importa na Escolha do Curso | Categórico | Principal motivação declarada para escolher um curso | Análise de motivação | Pode ajudar a entender fatores de decisão |
| Busca | Categórico / binário | Indica se o lead veio ou interagiu por busca | Análise de canal/comportamento | Pode ter baixo valor se houver poucos casos `Sim` |
| Revista | Categórico / binário | Indica origem ou interação relacionada a revista | Avaliação de canal | Baixo valor analítico se possuir apenas uma categoria |
| Artigo de Jornal | Categórico / binário | Indica origem ou interação relacionada a artigo de jornal | Avaliação de canal | Pode ter baixo impacto se houver poucos casos positivos |
| Fóruns da X Education | Categórico / binário | Indica interação com fóruns da empresa | Análise de engajamento | Pode ter baixo impacto se houver poucos casos positivos |
| Jornal | Categórico / binário | Indica origem ou interação relacionada a jornal | Avaliação de canal | Pode ter baixo valor se quase todos os registros forem iguais |
| Anúncio Digital | Categórico / binário | Indica interação com anúncio digital | Análise de marketing | Pode ser útil se houver volume suficiente de casos positivos |
| Por Recomendações | Categórico / binário | Indica se o lead veio por recomendação | Análise de indicação | Pode ser relevante, mas depende do volume de registros `Sim` |
| Receber Mais Atualizações Sobre Nossos Cursos | Categórico / binário | Indica interesse em receber atualizações | Análise de preferência de comunicação | Baixo valor se todos os registros forem iguais |
| Tags | Categórico | Classificação ou status atribuído ao lead | Análise de status comercial/funil | Usar com cuidado, pois pode conter informação posterior à conversão |
| Qualidade do Lead | Categórico | Classificação qualitativa do lead | Análise de qualificação e futuro score | Pode ser muito relevante para priorização comercial |
| Atualizar Sobre Conteúdo de Supply Chain | Categórico / binário | Indica interesse em conteúdo de Supply Chain | Análise de interesse específico | Baixo valor se todos os registros forem iguais |
| Receber Atualizações Sobre Conteúdo de Marketing Digital | Categórico / binário | Indica interesse em conteúdo de Marketing Digital | Análise de interesse específico | Baixo valor se todos os registros forem iguais |
| Perfil do Lead | Categórico | Perfil ou classificação do lead | Análise de segmentação | Pode indicar grupos com maior ou menor conversão |
| Cidade | Categórico | Cidade informada pelo lead | Análise geográfica | Pode ser útil, mas exige cuidado com `Não informado` |
| Índice de Atividade Assimétrica | Categórico | Classificação de atividade do lead em níveis | Análise de engajamento | Pode indicar intensidade de interação |
| Índice de Perfil Assimétrico | Categórico | Classificação do perfil do lead em níveis | Análise de perfil | Pode ajudar a diferenciar grupos de maior potencial |
| Pontuação de Atividade Assimétrica | Numérico | Pontuação associada à atividade do lead | Análise de score/engajamento | Pode ser útil no MVP 2, mas precisa tratar nulos |
| Pontuação de Perfil Assimétrico | Numérico | Pontuação associada ao perfil do lead | Análise de score/perfil | Pode ser útil no MVP 2, mas precisa tratar nulos |
| Concordo em Pagar o Valor por Cheque | Categórico / binário | Indica concordância com pagamento por cheque | Análise operacional | Baixo valor se todos os registros forem iguais |
| Cópia Gratuita de Mastering The Interview | Categórico / binário | Indica se o lead solicitou ou recebeu material gratuito | Análise de interesse/engajamento | Pode indicar maior intenção ou interação com conteúdo |
| Última Atividade Relevante | Categórico | Última atividade relevante registrada do lead | Análise de comportamento recente | Pode ajudar a identificar ações mais próximas da conversão |

---

## 4. Colunas prioritárias para o MVP 1

Com base no entendimento inicial da base, as colunas com maior potencial para análise e dashboard são:

| Coluna | Motivo |
|---|---|
| Convertido | Variável principal do projeto |
| Origem do Lead | Permite analisar conversão por origem |
| Fonte do Lead | Permite avaliar canais de aquisição |
| Última Atividade | Ajuda a entender comportamento recente |
| Última Atividade Relevante | Ajuda a entender interações importantes antes da conversão |
| Total de Visitas | Mede engajamento |
| Tempo Total no Site | Mede interesse e profundidade de navegação |
| Visualizações de Página por Visita | Mede comportamento de navegação |
| Especialização | Ajuda a entender áreas de interesse |
| Ocupação Atual | Ajuda a analisar perfil profissional |
| Qualidade do Lead | Pode apoiar análise e score futuro |
| Perfil do Lead | Ajuda na segmentação |
| Cidade | Pode apoiar análise geográfica, com cuidado |
| Índice de Atividade Assimétrica | Pode indicar nível de engajamento |
| Índice de Perfil Assimétrico | Pode indicar qualidade do perfil |
| Cópia Gratuita de Mastering The Interview | Pode indicar interesse em conteúdo gratuito |

---

## 5. Colunas com baixo valor inicial para o dashboard

Algumas colunas possuem baixa variação ou predominância quase total de uma única resposta. Por isso, não serão priorizadas no dashboard inicial.

| Coluna | Motivo |
|---|---|
| Revista | Predominância de uma única resposta |
| Receber Mais Atualizações Sobre Nossos Cursos | Predominância de uma única resposta |
| Atualizar Sobre Conteúdo de Supply Chain | Predominância de uma única resposta |
| Receber Atualizações Sobre Conteúdo de Marketing Digital | Predominância de uma única resposta |
| Concordo em Pagar o Valor por Cheque | Predominância de uma única resposta |
| Busca | Poucos registros positivos |
| Artigo de Jornal | Poucos registros positivos |
| Fóruns da X Education | Poucos registros positivos |
| Jornal | Poucos registros positivos |
| Anúncio Digital | Poucos registros positivos |
| Por Recomendações | Poucos registros positivos |
| Não Ligar | Poucos registros positivos |

Essas colunas serão mantidas na base neste momento, mas não serão priorizadas na primeira versão do dashboard.

---

## 6. Cuidados importantes

Algumas colunas exigem atenção nas próximas etapas:

| Coluna | Cuidado |
|---|---|
| Tags | Pode conter informação posterior à conversão. Deve ser usada com cuidado em Machine Learning para evitar vazamento de informação |
| Perfil do Lead | Possui muitos registros como `Não informado` |
| Especialização | Possui muitos registros como `Não informado` |
| Cidade | Possui muitos registros como `Não informado` |
| País | Possui valores ausentes e pode ter baixa utilidade no contexto do dashboard |
| Pontuação de Atividade Assimétrica | Possui valores nulos e precisa de tratamento |
| Pontuação de Perfil Assimétrico | Possui valores nulos e precisa de tratamento |

---

## 7. Relação com os MVPs

| MVP | Como o dicionário será usado |
|---|---|
| MVP 1 — Dashboard | Apoiar a escolha das variáveis para gráficos, indicadores e filtros |
| MVP 2 — Score de Priorização | Ajudar a selecionar variáveis explicáveis para criar regras de pontuação |
| MVP 3 — Machine Learning | Apoiar a seleção de features e a exclusão de colunas com risco de vazamento |

---

## 8. Status

Status: versão inicial concluída.

Este dicionário poderá ser atualizado nas próximas etapas, principalmente após a limpeza dos dados, análise exploratória e validação das variáveis mais relevantes para conversão.
