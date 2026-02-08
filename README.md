# 📊 Data Insights: Performance de Vendas e Comportamento do Cliente

## 🎯 Objetivo do Projeto
Este projeto utiliza SQL para realizar uma análise diagnóstica de uma operação de E-commerce. O foco foi transformar registros brutos em indicadores de desempenho (KPIs) para otimização de estoque, estratégia de marketing e saneamento de base de dados.

---

##  Stack Técnica
* **Banco de Dados:** MySQL
* **Principais Comandos:** `INNER JOIN`, `GROUP BY`, `ORDER BY` e Funções de Agregação (`SUM`, `AVG`, `COUNT`).

---

## 📈 Análise Detalhada (Insights)

### 1. Saneamento e Qualidade da Base
Antes de qualquer análise financeira, validei a integridade da base.
![Qualidade de Dados]<img width="855" height="189" alt="Image" src="https://github.com/user-attachments/assets/d891ca46-1af2-405f-b607-3fd36afdbc08" />
* **Insight:** Identifiquei clientes com campos de contato (telefone) nulos. Isso impacta diretamente em campanhas de retenção (CRM). Manter esses dados limpos economiza recursos em disparos de marketing ineficientes.

### 2. Visão 360° da Operação
Monitoramento constante das três entidades principais:
<p align="center">
  
  <img width="1124" height="483" alt="Image" src="https://github.com/user-attachments/assets/21bcce4e-5e57-4538-abe8-3fe48141396e" />
<img width="1035" height="423" alt="Image" src="https://github.com/user-attachments/assets/c42fc241-f748-4850-8510-e84c75df939c" />
 <img width="1050" height="499" alt="Image" src="https://github.com/user-attachments/assets/690c26fd-9b21-45ea-8890-7b92e741074c" />
</p>
* **Insight:** A organização tabular permite rastrear desde o perfil sociodemográfico do cliente até o custo unitário de cada produto, garantindo que a margem de lucro seja monitorada em tempo real.

### 3. Performance de Faturamento por Marca
Utilizei `INNER JOIN` para cruzar vendas com o catálogo de produtos.
![Receita por Marca]<img width="537" height="354" alt="Image" src="https://github.com/user-attachments/assets/57e53e7f-918e-4f7d-90bf-a3720d68f898" />
* **Insight:** O gráfico de resultados revela quais marcas dominam o faturamento. Note que marcas como **SONY** apresentam um volume financeiro significativamente superior, o que sugere uma priorização em negociações com fornecedores ou destaque em vitrines digitais.

### 4. Inteligência de Catálogo e Precificação
Aplicação de métricas estatísticas sobre o portfólio de produtos.
![Métricas de Preço]<img width="896" height="348" alt="Image" src="https://github.com/user-attachments/assets/e2f40d9c-2c02-4239-b61b-fa193e6b5e0d" />
* **Insight:** Com o `AVG` (Média), identificamos o ticket médio do catálogo (~1.788). Saber que o produto mais barato custa 280 e o mais caro 4.200 ajuda a definir a faixa de público-alvo (Classe A/B) e a criar estratégias de "upselling".

### 5. Segmentação de Público Ativo
Análise volumétrica por gênero.
![Vendas por Gênero]<img width="515" height="263" alt="Image" src="https://github.com/user-attachments/assets/e53b34cb-0a47-448d-9d88-d1260dcb2326" />
* **Insight:** A base está equilibrada, com uma leve predominância feminina (52%). Esse dado é crucial para o time de redação e design criar comunicações visualmente alinhadas à maioria do público.

---

## 🚀 Conclusão
As consultas desenvolvidas permitem que a empresa saia do "achismo" e tome decisões baseadas em dados reais. A automação desses scripts pode gerar dashboards diários de performance e saúde do negócio.

---
**Desenvolvido por:** [Luis thiago da silva Xavier]  
[LinkedIn: www.linkedin.com/in/luis-thiago-da-silva-xavier-a684303aa] | [📧 Envie um e-mail: luiz.tiagosilva200@gmail.com]
