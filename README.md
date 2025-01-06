# Atividade Final - Pipeline de Dados, CI/CD, Streaming (PDS)

Este repositório contém a documentação e exemplos de implementação para arquiteturas com pipelines de dados, processamento em batch/micro-batch, e abordagens Lambda e Kappa. Abaixo estão descritos os principais tópicos abordados no projeto.

## 1. Criação de Pipeline ETL para Fontes de Dados

O pipeline ETL (Extract, Transform, Load) é projetado para integrar dados de diferentes fontes em um sistema centralizado.

### Etapas do Processo:
1. **Extract:** Conexão com fontes de dados (bancos relacionais, NoSQL, APIs, arquivos, etc.).
2. **Transform:** Aplicação de transformações para limpeza, enriquecimento e formatação dos dados.
3. **Load:** Armazenamento dos dados transformados em um Data Lake ou Data Warehouse.

### Ferramentas Recomendadas:
- **Orquestração:** Apache Airflow.
- **Ingestão e transporte em tempo real:** Apache Kafka.
- **Transformação:** Apache Spark ou Apache Flink.
- **Armazenamento:** Amazon Redshift, Google BigQuery ou Snowflake.

## 2. Projeto de Arquitetura com Batch e Micro-Batch

### Batch Processing
- **Definição:** Processamento de grandes volumes de dados em intervalos fixos.
- **Vantagens:** Eficiência para grandes volumes e custos reduzidos.
- **Ferramentas:** Apache Hadoop, Apache Spark.

### Micro-Batch Processing
- **Definição:** Processamento em pequenos lotes com baixa latência.
- **Vantagens:** Combina velocidade e escalabilidade.
- **Ferramentas:** Apache Spark Streaming, Apache Flink.

## 3. Implementação das Arquiteturas Lambda e Kappa

### Arquitetura Lambda
- **Componentes:**
  - Batch layer: Processa dados históricos.
  - Speed layer: Processa dados em tempo real.
  - Serving layer: Combina os resultados das duas camadas.
- **Ferramentas:** Apache Spark para batch, Apache Kafka ou Flink para streaming.
- **Vantagens:** Resiliência e escalabilidade.
- **Desvantagens:** Complexidade e custos mais elevados.

### Arquitetura Kappa
- **Definição:** Processamento exclusivo em tempo real, sem camada de batch.
- **Componentes:**
  - Stream processing layer: Processa todos os dados em tempo real.
  - Storage: Armazena dados brutos.
- **Ferramentas:** Apache Flink, Apache Kafka Streams.
- **Vantagens:** Simplicidade e baixa latência.
- **Desvantagens:** Menor eficiência para dados históricos completos.

## Conclusão

### Recomendação de Ferramentas:
- **ETL Pipeline:** Use Apache Airflow para orquestração, Apache Kafka para ingestão e Spark/Flink para processamento.
- **Batch e Micro-Batch:** Hadoop ou Spark para batch; Spark Streaming ou Flink para micro-batch.
- **Lambda vs Kappa:**
  - Lambda: Melhor para cenários que exigem resiliência e escalabilidade.
  - Kappa: Ideal para arquiteturas simplificadas com foco total em streaming.

Esta documentação oferece uma base sólida para implementar arquiteturas flexíveis e escaláveis, fornecendo insights rápidos e precisos para melhorar decisões baseadas em dados.
