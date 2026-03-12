# 🩺 Health Analytics: Inteligência de Dados na Gestão de Sinistralidade

> **Status do Projeto:** Concluído ✅
> 
> Este projeto consiste em uma solução de Business Intelligence ponta a ponta para o setor de Saúde Suplementar. O objetivo central é transformar dados brutos de utilização hospitalar em insights estratégicos para o controle de custos assistenciais e auditoria de beneficiários.

---

## 🎯 O Problema de Negócio
Empresas de saúde enfrentam o desafio constante do aumento da sinistralidade. Sem uma visão clara, é impossível identificar se o aumento de custos vem de procedimentos específicos, de uma faixa etária específica ou de um grupo reduzido de beneficiários (ofensores). 

Este dashboard foi desenvolvido para responder:
* Qual o ticket médio por plano e faixa etária?
* Onde estão concentrados os maiores gastos (Cirurgias, Exames ou Consultas)?
* Quem são os beneficiários que mais impactam o custo total e por quê?

---

## 🛠️ Desenvolvimento Técnico

### 1. Engenharia de Dados com SQL Server
A fundação do projeto foi construída com foco em performance. Em vez de sobrecarregar o Power BI, a inteligência de agrupamento foi feita na extração.
* **Técnicas utilizadas:** Joins complexos, funções de data (`DATEDIFF`) para cálculos de idade em tempo real e formatação de métricas financeiras.
![Inteligência em SQL](./01_extracao_sql.png)

### 2. Modelagem de Dados (Star Schema)
Utilizei a metodologia de **Kimball** para estruturar um modelo em estrela. Isso garante que os filtros sejam rápidos e que as métricas (DAX) não apresentem erros de contexto.
* **Tabelas Dimensão:** Beneficiários, Procedimentos e Calendário.
* **Tabela Fato:** Sinistros.
![Arquitetura de Dados](./02_modelagem_star_schema.png)

### 3. ETL e Refinamento (Power Query)
Processo de limpeza de dados, padronização de nomes e criação de colunas auxiliares para otimização visual.
![Processamento de Dados](./03_etl_power_query.png)

### 4. Experiência do Usuário (UX/UI Design)
O design foi pensado para ser um "aplicativo de análise".
* **Navegação Lateral:** Menu intuitivo para troca de páginas.
* **Drill-down e Filtros:** Capacidade de sair do macro (Custo Total) para o micro (Histórico do Beneficiário) em um clique.
* **Botão Reset:** Função de "limpar filtros" via Bookmarks para facilitar a exploração dos dados.

![Visão Executiva](./04_dashboard_visao_geral.png)
![Visão de Auditoria](./05_dashboard_detalhamento.png)

---

## ⚙️ Tecnologias
* **SQL Server** (Processamento de Dados)
* **Power BI** (Visualização e DAX)
* **Power Query** (M - ETL)

---

## 👤 Autor
**Alex** - Analista de Dados em formação | Gestão Financeira | Logística
