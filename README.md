🛡️ Scanner Híbrido de Vulnerabilidades (SAST + IA Semântica)

Este Jupyter Notebook implementa um scanner experimental híbrido de vulnerabilidades que combina:

    Teste Estático de Segurança de Aplicações (SAST) com Rastreamento de Dados (Taint Tracking) baseado em AST

    Busca semântica de vulnerabilidades reais usando GraphCodeBERT + Base de Dados NVD CVE

🚀 Funcionalidades
1. Análise Estática + Rastreamento de Dados

    Parseia código Python em uma Árvore Sintática Abstrata (AST)

    Identifica fontes de dados contaminados (ex: input, raw_input)

    Detecta funções perigosas:

        Injeção de comando (os.system, subprocess.call, etc.)

        Injeção de código (eval, exec)

        Desserialização insegura (pickle.loads)

2. Busca Semântica de CVEs (com IA)

    Baixa CVEs recentes da API do NVD

    Gera embeddings para cada descrição de CVE usando microsoft/graphcodebert-base

    Compara o código fornecido com a matriz de embeddings das CVEs

    Retorna as 5 CVEs mais similares (similaridade > 0.75)

3. Relatório Híbrido

    Alertas estáticos + fluxo de dados contaminados

    Referências reais de CVE com:

        ID da CVE

        Severidade (Crítico, Alto, Médio, Baixo)

        Pontuações de Explorabilidade e Impacto

        Score de similaridade

        Classificação CWE

###########################################################################################################
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
