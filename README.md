# Projeto de ETL Cenipa

Este projeto de ETL (Extract, Transform, Load) e análise foi desenvolvido utilizando a biblioteca Pandas em conjunto com o Pandera. O objetivo é explorar a base de dados do CENIPA (Centro de Investigação e Prevenção de Acidentes Aeronáuticos), disponível publicamente em um link específico.

## Pré-Requisitos

Antes de executar o projeto, é necessário instalar as seguintes bibliotecas:

```bash
pip install pandas pandera
```

## Importação das Bibliotecas

```python
import pandas as pd
import pandera as pa
```

## Extração dos Dados

Os dados são extraídos de arquivos CSV disponíveis em um repositório público. São utilizados cinco DataFrames: `df`, `df1`, `df2`, `df3` e `df4`.

## Tratamento Inicial dos Dados

Em seguida, é realizado um tratamento inicial dos dados, que inclui:

- Remoção de colunas repetidas e não utilizadas no DataFrame `df`.
- Transformação do tipo de dados da coluna `dia` em datetime.
- Tratamento de valores inconsistentes nas colunas `aerodromo`, `fator_condicionante`, `aeronave_pais_fabricante`, `aero_tipo_icao` e `status_recomend` nos respectivos DataFrames.
- Remoção de colunas que não serão utilizadas no DataFrame `df4`.

## Validação dos Dados

Cada DataFrame passa por um processo de validação utilizando o Pandera. São criados esquemas de validação para garantir que as colunas tenham os tipos de dados esperados.

## Merge dos DataFrames

Os DataFrames são unidos por meio de merges, resultando em um DataFrame final chamado `dff4`.

## Análises

São realizadas algumas análises no DataFrame `dff4`, utilizando filtros para extrair informações específicas. Por exemplo, são criados DataFrames com ocorrências classificadas como "INCIDENTE" no ano de 2020 na região Centro-Oeste e com ocorrências do tipo "FALHA DO MOTOR EM VOO" no ano de 2021 na mesma região.

## Conclusão

Esse projeto de ETL e análise proporciona uma visão exploratória dos dados do CENIPA, permitindo a extração de informações relevantes sobre as ocorrências aeronáuticas. É possível adaptar e expandir as análises de acordo com as necessidades do projeto ou da pesquisa em questão.

## Autor
O projeto foi desenvolvido por [Giovana de Brito Silva](https://github.com/giobritos).
