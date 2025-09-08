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

############################################################################################################
Para replicar os resultados da pesquisa, siga os passos abaixo. O notebook foi testado no Google Colab, garantindo um ambiente com todas as bibliotecas e recursos de hardware necessários.

1.  Faça o download ou clone o repositório.**
      git clone [https://github.com/Binho-do-Boa/Artigo-Final-UFMT]
2.  Acesse o Google Colab.
3.  Faça o upload dos arquivos `Cod_Artigo_Final_Com_Graficos_Novo.ipynb` e `nvdcve-1.1-recent.json` para o seu Google Drive.
4.  Abra o notebook `Cod_Artigo_Final_Com_Graficos_Novo.ipynb` no Google Colab.
5.  Conecte seu Google Drive no notebook.
6.  Execute todas as células do notebook. As dependências necessárias (como `transformers` e `gensim`) serão instaladas automaticamente, descomentar as linhas.
O notebook irá gerar as tabelas e os gráficos comparativos, reproduzindo todos os resultados da pesquisa.

👨‍💻 Autor
Fábio José do Nascimento
Pós-graduação em Gestão e Ciências de Dados – UFMT
