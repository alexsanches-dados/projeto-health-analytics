# 🩺 Health Analytics: Inteligência de Dados na Gestão de Sinistralidade

> **Status do Projeto:** Concluído ✅
> 
> Este projeto apresenta uma solução de Business Intelligence ponta a ponta para o setor de Saúde Suplementar. O objetivo central é transformar dados brutos de utilização hospitalar em insights estratégicos para o controle de custos assistenciais e auditoria de beneficiários.

---

## 🎯 O Problema de Negócio
Empresas de saúde enfrentam o desafio constante do aumento da sinistralidade. Sem uma visão clara, é impossível identificar se o aumento de custos vem de procedimentos específicos, de uma faixa etária específica ou de um grupo reduzido de beneficiários (ofensores). 

Este dashboard foi desenvolvido para responder:
* Qual o ticket médio por plano e faixa etária?
* Onde estão concentrados os maiores gastos (Cirurgias, Internações ou Exames)?
* Quem são os beneficiários que mais impactam o custo total?

---

## 🛠️ Desenvolvimento Técnico

### 1. Engenharia de Dados com SQL Server
A inteligência do projeto começa na extração. Utilizei SQL para preparar os dados, garantindo performance e integridade antes da carga no Power BI.
* **Técnicas:** Joins entre tabelas de sinistros e beneficiários, cálculos de idade em tempo real e métricas de agregação financeira.
![Inteligência em SQL](./01_extracao_sql.png)

### 2. Modelagem de Dados (Star Schema)
Estruturação de um modelo multidimensional para garantir que os filtros sejam rápidos e as métricas DAX precisas.
* **Arquitetura:** Separação clara entre Tabelas Dimensão e Tabela Fato, permitindo uma análise granular e performática.
![Arquitetura de Dados](./02_modelagem_star_schema.png)

### 3. ETL e Refinamento (Power Query)
Processo de limpeza, padronização de tipos de dados e criação de colunas auxiliares para otimização do relatório.
![Processamento de Dados](./03_etl_power_query.png)

### 4. Experiência do Usuário (UX/UI Design)
O design foi desenvolvido com foco em usabilidade corporativa:
* **Navegação Lateral:** Menu intuitivo para alternar entre as visões do dashboard.
* **Análise Granular:** Capacidade de navegar do macro (Custo Total) para o micro (Detalhes por Beneficiário).
* **Funcionalidades:** Botão de reset de filtros e indicadores para uma navegação fluida.

![Visão Executiva](./04_dashboard_visao_geral.png)
![Visão de Auditoria](./05_dashboard_detalhamento.png)

---

## ⚙️ Tecnologias
* **SQL Server** (Processamento de Dados)
* **Power BI** (Visualização e DAX)
* **Power Query** (M - ETL)

---

## 👤 Autor
**Alex Sanches** 🔗 [LinkedIn](https://www.linkedin.com/in/alexsanches-dados) | Analista de Dados 
