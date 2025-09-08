Análise de Vulnerabilidades em Softwares com Técnicas de Inteligência Artificial
Este repositório contém o código, dataset e experimentos desenvolvidos no âmbito do artigo científico “Análise de Vulnerabilidades em Softwares Utilizando Técnicas de Inteligência Artificial (IA)”, apresentado como requisito para conclusão da pós-graduação em Gestão e Ciências de Dados (UFMT).

📌 Objetivo
Investigar técnicas de mineração de dados e aprendizado de máquina na análise de vulnerabilidades de software, utilizando o dataset público NVD Recent (National Vulnerability Database).

O trabalho compara diferentes formas de representação textual (Bag of Words, TF-IDF + PCA, Word2Vec e BERT) aplicadas a dois algoritmos amplamente utilizados:
Random Forest → Classificação supervisionada (vulnerabilidade crítica vs. não crítica).
K-means → Clusterização não supervisionada de descrições de vulnerabilidade.

⚙️ Tecnologias Utilizadas
Linguagem: Python 3.9
Bibliotecas principais:
pandas, numpy, matplotlib, scikit-learn
gensim (para Word2Vec)
torch, transformers (para BERT/DistilBERT)

📊 Metodologia
Coleta de Dados: NVD Recent (NIST, 2025).
Pré-processamento: limpeza, tokenização e vetorização textual.
Modelagem:
Random Forest (classificação).
K-means (clusterização).
Representações testadas:
Bag of Words (baseline).
TF-IDF + PCA.
Word2Vec (média de embeddings).
BERT (vetor [CLS]).
Avaliação: métricas padrão (Acurácia, F1-score, Silhouette Score).

👨‍💻 Autor
Fábio José do Nascimento
Pós-graduação em Gestão e Ciências de Dados – UFMT
