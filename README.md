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
🛠️ Instalação

Clone o repositório:
```bash
git clone https://github.com/seu-usuario/vulnerability-scanner-hibrido.git
cd vulnerability-scanner-hibrido

###########################################################################################################
👨‍💻 Autor
Fábio José do Nascimento
Pós-graduação em Gestão e Ciências de Dados – UFMT
