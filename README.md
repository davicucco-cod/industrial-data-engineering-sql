# Industrial Data Engineering: SQL Pipeline

## O Problema
Na indústria, dados críticos frequentemente ficam fragmentados em planilhas CSV ou sofrem com falhas de sensores (ruído). Isso impede a aplicação confiável de Inteligência Artificial.
Este projeto foca na **Engenharia de Dados**, criando uma estrutura robusta de armazenamento e limpeza.

## Arquitetura do Projeto
Utilizando **Python (SQLite)** e **Pandas**, simulei o ambiente de TI de uma fábrica:

* **Modelagem de Dados:** Criação de esquema relacional (Tabelas `Maquinas` e `Historico_Sensores`).
* **ETL (Extract, Transform, Load):** Pipeline de ingestão de dados.
* **Data Quality:** Tratamento de *Outliers* (ex: temperatura negativa impossível) e *Missing Values* (NULLs) diretamente na query SQL.

## Principais Queries Desenvolvidas
1.  **Relatório de KPIs:** Uso de `GROUP BY` para calcular média de temperatura e vibração máxima por equipamento.
2.  **Monitoramento de Críticos:** Uso de `HAVING` para filtrar apenas máquinas operando fora dos parâmetros normais.
3.  **Sanitização:** Uso de `CASE WHEN` e `COALESCE` para corrigir falhas de sensores em tempo real.

## Stack
* **Language:** SQL (Structured Query Language) & Python.
* **Database:** SQLite.
* **Library:** Pandas (para leitura e visualização de queries).

---
*Desenvolvido por Davi Duarte Cucco | [LinkedIn](https://www.linkedin.com/in/davi-duarte-cucco-8b272a238/)*
