# Análise de Saúde Financeira - Lojas Highway

## 1. Visão Geral do Projeto

Este projeto foi desenvolvido com o objetivo de analisar dados financeiros de quatro lojas da franquia de fast-food "Highway" do franqueado Lorenzzo Lopez.

O principal resultado do projeto é um **Índice de Saúde Financeira (ISF)**, uma métrica criada para avaliar e comparar a performance das lojas a partir de variáveis chaves. Além disso, foi construído um dashboard interativo no Looker Studio para que o franqueado possa explorar os dados de forma mais amigável.

## 2. Ferramentas Utilizadas

* **Linguagem:** Python 3.11
* **Ambiente:** Jupyter Notebook (ou Google Colab)
* **Bibliotecas Utilizadas:**
    * `pandas`: Para manipulação e estruturação dos dados.
    * `duckdb`: Para a execução de queries SQL diretamente nos arquivos CSV.
    * `scikit-learn`: Para a normalização dos dados (MinMaxScaler) na construção do índice.
* **Ferramenta de BI:** Looker Studio para a criação do dashboard interativo.

## 3. Como Reproduzir o Projeto

Siga os passos abaixo para executar a análise e visualizar os resultados.

### Pré-requisitos

* Ter o Python 3.11+ instalado.
* Acesso a um ambiente que execute arquivos .ipynb.

### Passos

1.  **Clone o Repositório:**
    ```bash
    git clone [URL_DO_SEU_REPOSITORIO]
    cd [NOME_DO_SEU_REPOSITORIO]
    ```

2.  **Crie um Ambiente Virtual e Instale as Dependências:**
    Recomendo criar um ambiente virtual para isolar as dependências do projeto.
    ```bash
    # Criar ambiente virtual
    python -m venv venv

    # Ativar o ambiente (Windows)
    .\venv\Scripts\activate

    # Ativar o ambiente (Linux/Mac)
    source venv/bin/activate

    # Instalar as bibliotecas necessárias
    pip install pandas duckdb scikit-learn jupyterlab
    ```

3.  **Estrutura dos Dados:**
    Este projeto espera que os arquivos de dados dentro da pasta `data` (`receipts-000000000000.csv`, `items-000000000000.csv`, `discounts-000000000000.csv`, `payments-000000000000.csv` e `torque.csv`) estejam disponíveis. Para que o notebook funcione, verifique os caminhos dos arquivos na vairável `files_to_analyze`.

4.  **Execute o Notebook de Análise:**
    Abra e execute o notebook `highway_analysis.ipynb`. Execute todas as células
    ```bash
    jupyter lab
    ```
    Esse notebook irá processar os dados, realizar algumas análises e, ao final, irá ter como saída um arquivo chamado `daily_financial_health.csv`, com os dados limpos e agregados para serem utilizados no dashboard.

5.  **Acesse o Dashboard Interativo:**
    O dashboard foi criado no Looker Studio e permite a exploração dos resultados de forma visual e interativa.

    **Link:** https://lookerstudio.google.com/reporting/436c6f32-9082-4d4a-a8f6-e3c37598c93f

## 4. Estrutura do Repositório

* `/`: Raiz do projeto.
* `/data`: Pasta com os dados a serem analisados.
* `highway_analysis.ipynb`: Jupyter Notebook com todo o código.
* `daily_financial_health.csv`: Arquivo de saída gerado pelo notebook.
* `README.md`: Este arquivo.
* `relatorio.md`: O relatório com insights e recomendações para o negócio.