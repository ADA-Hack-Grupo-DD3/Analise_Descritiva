# Analise_Descritiva
Repositório com o *script* e saída da análise descritiva dos dados tratados

> O *Script* foi realizado por [Amanda Souza](https://www.linkedin.com/in/amanda-rs/) para o Ada Hack 2024.


## Descrição
Este *script* foi desenvolvido para realizar uma análise descritiva dos dados de diversidade da empresa **Corp Solutions**. O *script* foi realizado em [Python](https://www.get-python.org/) e conta com algumas funções, incluindo a limpeza e formatação dos dados, a geração de gráficos e mapas, e a exportação desses gráficos e mapas para uso posterior.

## Dependências
O *script* depende das seguintes bibliotecas Python:

- **[Pandas](https://pandas.pydata.org/)**: É uma biblioteca de código aberto que fornece estruturas de dados de alto desempenho e fáceis de usar, e ferramentas de análise de dados para a linguagem de programação Python. Ela é usada principalmente para manipulação e análise de dados e suporta muitos tipos de dados, incluindo dados tabulares com colunas heterogêneas, séries temporais, entre outros.

- **[Matplotlib](https://matplotlib.org/)**: É uma biblioteca de plotagem 2D em Python que produz figuras de qualidade de publicação em uma variedade de formatos impressos e ambientes interativos em todas as plataformas. Matplotlib pode ser usado em scripts Python, shells Python e IPython, servidores de aplicativos da web e várias interfaces de usuário gráficas.

- **[Seaborn](https://seaborn.pydata.org/)**: É uma biblioteca de visualização de dados Python baseada em Matplotlib. Ela fornece uma interface de alto nível para desenhar gráficos estatísticos atraentes e informativos. ``Seaborn`` ajuda a explorar e entender seus dados, e suas funções de plotagem operam em dataframes e arrays contendo conjuntos de dados inteiros.

- **[Geopandas](https://pypi.org/project/geopandas/)**: É um projeto de código aberto para tornar o trabalho com dados geoespaciais em python mais fácil. ``GeoPandas`` estende os ``datatypes`` usados pelo pandas para permitir operações espaciais em tipos geométricos. Ele combina as capacidades de pandas e *shapely*, fornecendo operações geoespaciais em pandas e uma interface de alto nível para múltiplas geometrias para *shapely*.

## Funções
O *script* contém as seguintes funções:

- `ajustes_nomes(data)`: Realiza ajustes em variáveis para melhor exibição dos resultados.
- `analise_base(data)`: Informa na tela informações sobre a qualidade dos dados.
- `graf_barra(data, x, y, eixo)`: Faz e estiliza um gráfico de barras.
- `export_plot(plot, file_path, format='png')`: Exporta um gráfico matplotlib ou seaborn para um arquivo.
- `const_export_graficos(data)`: Agrupa as construções e exportações dos gráficos de Gênero, Senioridade, Raça e Formação.
- `mapa_funcionarios(data)`: Constroi o mapa da distribuição de funcionários por estados.
- `const_export_mapa(data)`: Constrói e exporta o mapa de funcionários.

## Uso
Para usar este script, você deve primeiro carregar o conjunto de dados. Em seguida, você pode chamar as funções conforme necessário para realizar a análise desejada. Por exemplo:

```python
# Carregar o conjunto de dados
file_path = "Data_Base\\Dados_filtrados\\base_dados_filtrados.csv"
data = pd.read_csv(file_path)

# Ajustes dos nomes para as saídas de dados
data = ajustes_nomes(data)

# Análise da qualidade do banco de dados
analise_base(data)

# Exportação dos gráficos
const_export_graficos(data)

# Exportação do mapa
const_export_mapa(data)
```

Este script é uma ferramenta para entender a a base de dados de diversidade da Corp Solutions. Ele fornece insights visuais e quantitativos que podem ajudar análise de diversidae da empresa.