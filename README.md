# 🩺 Health Analytics: Monitoramento de Sinistralidade e Auditoria de Custos

Este projeto apresenta uma solução de Business Intelligence ponta a ponta, desenvolvida para o setor de saúde suplementar. O foco principal é a **gestão de sinistralidade**, permitindo que gestores identifiquem ofensores de custos e realizem auditorias detalhadas de utilização.

---

## 🛠️ Camadas Técnicas do Projeto

### 1. Inteligência de Dados (SQL Server)
A fundação do projeto foi construída diretamente no banco de dados. Utilizei queries para realizar a extração e a agregação prévia dos dados, garantindo que as regras de negócio fossem aplicadas na fonte.
* **Destaque Técnico:** Uso de `DATEDIFF` e `CASE WHEN` para criação dinâmica de faixas etárias e `FORMAT` para validação de métricas financeiras.
![Extração SQL](./ETL_Analise_Sinistralidade_SQL.png)

### 2. Arquitetura e Modelagem (Star Schema)
Para garantir a performance analítica e a integridade dos filtros, apliquei a modelagem multidimensional **Star Schema (Esquema Estrela)**.
* **Destaque Técnico:** Separação clara entre tabelas Fato (`fSinistros`) e Dimensões (`dCalendario`, `dBeneficiarios`, `dProcedimentos`), com relacionamentos de integridade referencial.
![Modelagem de Dados](./Modelagem_Dados_Star_Schema.png)

### 3. Tratamento e ETL (Power Query)
Nesta fase, realizei a limpeza e tipagem dos dados, além da criação da tabela Calendário para análises temporais precisas.
![Power Query](./ETL_Power_Query_Saude_Analitica.png)

### 4. Visualização e UX Design (Power BI)
O dashboard foi dividido em duas camadas lógicas para atender diferentes níveis de decisão:

* **Página 1 - Visão Estratégica:** Acompanhamento de KPIs globais (Ticket Médio, Custo Total, Economia de Coparticipação) e tendências mensais de custos.
* **Página 2 - Visão de Auditoria:** Detalhamento granular por beneficiário e procedimento, permitindo a investigação de "causa raiz" de gastos elevados.
* **Recursos de UX:** Navegação via Sidebar (menu lateral), botões de reset de filtros e indicadores (Bookmarks) para uma experiência de "aplicativo".

![Dashboard Pagina 1](./Projeto%20Saude_page-0001.jpg)
![Dashboard Pagina 2](./Projeto%20Saude_page-0002.jpg)

---

## 📈 Resultados de Negócio
- **Redução no tempo de análise:** Automação de relatórios que antes eram manuais.
- **Identificação de Ofensores:** Facilidade em encontrar os beneficiários e procedimentos com maior impacto no sinistro.
- **Auditoria Facilitada:** Cruzamento rápido entre custo hospitalar e tipo de atendimento.

---

## 🔧 Ferramentas Utilizadas
- **SQL Server:** Extração e Agregação.
- **Power BI:** Modelagem, DAX e Visualização.
- **Power Query:** ETL.
