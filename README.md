# Análise de Issues do Jira

## 1. Descrição do projeto
Este projeto faz uma análise de issues extraídas do Jira, com foco em:
- Normalização de status e resolução de problemas.
- Filtragem por prioridades urgentes/importantes.
- Criação de métricas e dashboards no Power BI.

## 2. Dataset
O conjunto de dados **não está incluído neste repositório** por questões de tamanho, mas pode ser baixado diretamente em:  
➡️ [Jira Issue Reports v1 (Kaggle)](https://www.kaggle.com/datasets/antonyjr/jira-issue-reports-v1)

Após o download:
1. Salve o arquivo CSV na pasta `data/`.
2. Execute o notebook Jupyter (`jira.ipynb`) para realizar o pré-processamento e gerar os CSVs limpos usados no Power BI.

## 3. Código Python
O notebook `jira.ipynb` realiza:
1. Carregamento do CSV original.
2. Limpeza de dados.
3. Normalização de status e resolution.
4. Filtragem por prioridades urgentes (`Major`, `Critical`, `Blocker`).
5. Exportação do CSV final:
   - `jira_issues_opened.csv` – dataset limpo e normalizado.

## 4. Dashboard Power BI
O arquivo `Jira_issues_BI.pbix` contém:
- **KPIs (cartões de destaque)**:
  - **Problemas em aberto:** total atual de issues sem resolução.
  - **Tempo médio aberto (anos):** média de tempo que os problemas permanecem abertos.
  - **Críticos e bloqueadores (%):** proporção de problemas críticos e bloqueadores em relação ao total.
- **Gráfico de barras por prioridade:** distribuição do número de issues por prioridade.
- **Tendência temporal (linha):** evolução mensal da criação de issues ao longo do tempo.
- **Matriz prioridade x responsável (assignee):** visão cruzada das prioridades atribuídas a cada responsável, incluindo totais gerais.
- **Segmentadores (filtros interativos):** permitem refinar a matriz por prioridade, status ou responsável.

### Observação:
- Todos os gráficos usam o CSV gerado pelo notebook.

## 5. Como usar
1. Baixe o dataset original e coloque na pasta `data/`.
2. Abra e execute o notebook `jira.ipynb`.
3. Abra o Power BI Desktop e carregue o arquivo `Jira_issues_BI.pbix`.
4. Os gráficos e KPIs já estarão configurados para visualização.

---