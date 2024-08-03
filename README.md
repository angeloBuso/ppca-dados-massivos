# Análise de Dados Massivos utilizando Apache Spark

## Descrição
Este repositório contém notebooks que documentam o desenvolvimento de pipelines de processamento de dados utilizando Apache Spark. O objetivo principal é manipular e analisar grandes volumes de dados provenientes da Receita Federal do Brasil (RFB) e da Procuradoria-Geral da Fazenda Nacional (PGFN), identificando padrões e anomalias entre sócios, empresas e dívidas.

### Notebooks Incluídos:
1. **[pgfn]pipeline-spark-mdm-ppca.ipynb**
   - Análise de dados de Pessoas Jurídicas (PJ) e Pessoas Físicas (PF) da PGFN.
   - Identificação e agregação de dívidas.
   - Persistência dos dados processados no Google Cloud Storage.

2. **[rfb]pipeline-spark-mdm-ppca.ipynb**
   - Análise de sócios e empresas com base nos dados da RFB.
   - Identificação de sócios com múltiplas empresas e diversas qualificações.
   - Análise de faixa etária dos sócios.
   - Persistência dos dados processados no Google Cloud Storage.

## Estrutura do Projeto

### 1. Importação de Bibliotecas
Configuração inicial e importação das bibliotecas necessárias.

### 2. Configurações de Conexão e Leitura dos Dados
- Leitura dos dados a partir do Google Cloud Storage.
- Configuração do SparkSession para processamento.

### 3. Transformações Iniciais
- Filtragem dos dados para remoção de registros indesejados.
- Criação de DataFrames específicos para análise de sócios, empresas e dívidas.

### 4. Análises Específicas
- Identificação de sócios com múltiplas empresas e diversas qualificações.
- Análise de faixa etária dos sócios.
- Agrupamento e cálculo de somas e médias das dívidas.

### 5. Persistência dos Dados
- Salvamento dos DataFrames processados em formato CSV no Google Cloud Storage.

## Como Executar

### Pré-requisitos
- Apache Spark instalado.
- Acesso ao Google Cloud Storage com permissões adequadas.
- Python 3.6+.

### Passos
1. Clone este repositório:
    ```bash
    git clone https://github.com/angeloBuso/ppca-dados-massivos.git
    ```
2. Configure seu ambiente de execução com as credenciais do Google Cloud.
3. Execute os notebooks utilizando Jupyter:
    ```bash
    jupyter notebook [pgfn]pipeline-spark-mdm-ppca.ipynb
    jupyter notebook [rfb]pipeline-spark-mdm-ppca.ipynb
    ```

## Contribuições
Sinta-se à vontade para contribuir com melhorias para estes pipelines. Faça um fork do repositório e envie suas sugestões via pull request.

## Licença
Este projeto está licenciado sob os termos da MIT License.

