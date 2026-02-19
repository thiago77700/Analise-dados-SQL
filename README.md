# 📊 Projeto de Análise de Dados – Vendas no Varejo

---

## 📌 Principais Resultados

- **Faturamento total:** $456.000  
- **Ticket médio:** $456  
- **Categoria líder:** Electronics (34,41%)  
- **Maior volume:** Clothing  

---

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo analisar dados de vendas de uma empresa do setor varejista, transformando dados brutos em **insights estratégicos para tomada de decisão**.

As análises buscaram responder:

- Qual o faturamento total?
- Qual o ticket médio?
- Qual categoria é mais rentável?
- Qual categoria vende mais?
- Como está distribuída a receita?
- Volume alto significa maior rentabilidade?

---

## 🗂️ Estrutura do Projeto



## 🗂️ Estrutura do Projeto

📁 /sql → Queries utilizadas nas análises
📁 /excel → Tabelas dinâmicas e análises exploratórias
📁 /dashboard → Visualização no Power BI
📄 README.md → Documentação do projeto


---

# 🗄️ Parte 1 – Análise em SQL

## 🔎 1. Validação da Base

```sql
SELECT COUNT(*) 
FROM base;

💰 2. Faturamento Total

SELECT SUM(`Total Amount`) AS faturamento_total 
FROM base;
✔ Faturamento total: $456.000,00

📅 3. Faturamento Mensal

SELECT 
    DATE_FORMAT(`Date`, '%Y-%m') AS mes, 
    SUM(`Total Amount`) AS faturamento_mensal 
FROM base 
GROUP BY mes 
ORDER BY mes;

✔ Análise de evolução temporal do faturamento.

🏆 4. Faturamento por Categoria

SELECT 
    `Product Category` AS categoria, 
    SUM(`Total Amount`) AS faturamento 
FROM base 
GROUP BY `Product Category` 
ORDER BY faturamento DESC;

Categoria	Faturamento
Electronics	$156.905,00
Clothing	 $155.580,00
Beauty	   $143.515,00
Total Geral	$456.000,00

✔ Electronics lidera o faturamento.

👤 5. Ticket Médio por Cliente
SELECT 
    `Customer ID`, 
    SUM(`Total Amount`) AS total_cliente 
FROM base 
GROUP BY `Customer ID`;

📉 6. Análise de Variação (Função de Janela)

SELECT 
    mes,
    faturamento,
    faturamento - LAG(faturamento) OVER (ORDER BY mes) AS variacao
FROM (
    SELECT 
        DATE_FORMAT(`Date`, '%Y-%m') AS mes,
        SUM(`Total Amount`) AS faturamento
    FROM base
    GROUP BY mes
) t;

✔ Uso de função de janela (LAG) para identificar crescimento ou queda mensal.

📊 Parte 2 – Análise em Excel (Tabelas Dinâmicas)
💰 Ticket Médio por Categoria
Categoria Faturamento	   Ticket Médio
Beauty	   $143.515,00	    $467,48
Clothing	 $155.580,00   	$443,25
Electronics	 $156.905,00	$458,79
Total Geral	 $456.000,00	$456,00

🔎 Insight:
Beauty apresenta o maior ticket médio.

🛒 Quantidade de Vendas por Categoria
Categoria	Nº Transações
Beauty	      307
Clothing	    351
Electronics  	342
Total Geral	  1.000

🔎 Insight:
Clothing possui maior volume de vendas.

📊 Participação no Faturamento (%)
Categoria	  Participação
Beauty	      31,47%
Clothing	    34,12%
Electronics	   34,41%
Total Geral	    100%

🔎 Insight:
Electronics representa aproximadamente 34% do faturamento.

🔄 Análise de Mix (Volume x Rentabilidade)
Categoria	   Quantidade Vendida	        Ticket Médio
Beauty	           307	                 $467,48
Clothing        	 351	                 $443,25
Electronics        342	                 $458,79
Total Geral     	 1000	                 $456,00

🎯 Insight:

Clothing possui maior volume

Beauty possui maior ticket médio

Electronics equilibra volume e rentabilidade

➡ Categoria com maior volume nem sempre é a mais rentável.

---
# 🎥 Demonstração do Projeto

Vídeo demonstrando a navegação pelo dashboard desenvolvido no Power BI.

🔗 Assista no YouTube:  
https://youtu.be/F8_ZbqfIAtQ

---

# 📬 Contato

🔗 **LinkedIn:**  
[Luís Thiago da Silva Xavier](https://www.linkedin.com/in/luis-thiago-da-silva-xavier-a684303aa)

📧 Email:luiz.tiagosilva700@gmail.com

