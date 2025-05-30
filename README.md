# 🔍 Classificação de Avaliações Yelp com Big Data e Machine Learning

Este projeto foi desenvolvido como trabalho final da disciplina de Big Data, com foco em **classificação de avaliações (reviews)** da base de dados do **Yelp**, utilizando técnicas de **Processamento de Linguagem Natural (NLP)** e **aprendizado de máquina** sobre um ambiente simulado de **cluster com Apache Hadoop e Spark via Docker**.

---

## 📦 Dataset

Utilizamos o [Yelp Dataset](https://www.kaggle.com/datasets/yelp-dataset/yelp-dataset), que contém milhões de avaliações reais de usuários sobre estabelecimentos comerciais.

Para fins de desempenho e foco, trabalhamos com o arquivo:

- `yelp_academic_dataset_review.json`

E filtramos apenas avaliações com notas **1, 3 e 5 estrelas**, representando respectivamente:

- **1 estrela:** Avaliações negativas
- **3 estrelas:** Avaliações neutras
- **5 estrelas:** Avaliações positivas

---

## ⚙️ Ambiente Big Data

Simulamos um ambiente Big Data com Docker, incluindo:

- **Apache Hadoop**
- **Apache Hive**
- **Apache Spark**

### Principais etapas:
- Criação do cluster via `docker-compose`
- Armazenamento do dataset no HDFS
- Acesso via Hive e Spark para leitura e análise distribuída dos dados

---

## 📊 Análise Exploratória de Dados (EDA)

Realizamos uma análise exploratória completa com PySpark, incluindo:

- Distribuição de notas (1, 3, 5)
- Volume de avaliações por ano
- Comprimento do texto das avaliações
- Verificação de outliers, nulos e duplicatas

---

## 🧪 Pré-processamento

O pré-processamento dos textos envolveu:

- **Tokenização:** Separação das palavras em cada review
- **Remoção de stopwords:** Palavras irrelevantes como “o”, “a”, “de”
- **TF-IDF:** Vetorização dos textos com base na frequência e relevância de cada termo
- **Oversampling:** Técnica para balancear as classes, evitando viés nos modelos

---

## 🤖 Modelos de Classificação

Aplicamos dois modelos supervisionados de classificação com PySpark MLlib:

1. **Regressão Logística**  
2. **Naive Bayes**

### Resultados:

| Modelo              | Acurácia |
|---------------------|----------|
| Regressão Logística | 86,7%    |
| Naive Bayes         | 6,2%     |

---

## 🧠 Conclusões

- A Regressão Logística apresentou excelente desempenho, pois lida bem com dados vetorizados por TF-IDF.
- O Naive Bayes teve desempenho ruim devido à suposição de independência entre palavras, o que não reflete bem a linguagem natural.
- O projeto demonstrou como aplicar técnicas de Big Data para treinar modelos preditivos em grande escala com textos reais.

---

## 💡 Aplicações Reais

- Monitoramento de reputação em tempo real
- Filtragem automática de reviews incoerentes
- Suporte à tomada de decisão em negócios
- Classificação de sentimentos em atendimentos e SACs

---

## 🛠️ Tecnologias Utilizadas

- Python (Google Colab)
- PySpark
- Docker + Docker Compose
- Apache Hadoop
- Apache Hive
- Apache Spark
- Kaggle API

---

## 👨‍🏫 Projeto Acadêmico

Trabalho final da disciplina de Big Data – Curso de Engenharia de Computação - Facens

Professor: Fabrício Torquato

Alunos: Caio Reis Despontin, João Pedro Santos Batista, Vinicius Gonçalves Angelo, Vinicius Ribeiro Silva

Ano: 2025

---

## 📎 Licença

Este projeto é apenas para fins acadêmicos e de demonstração.
