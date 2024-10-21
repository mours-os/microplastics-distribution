##  Predição da Concentração de Microplásticos na costa marítima brasileira
1. Poluição por microplásticos

Este projeto visa prever a distribuição da concentração de microplásticos ao longo da costa marítima brasileira utilizando técnicas de geoprocessamento e aprendizado de máquina.
O projeto integrará dados geoespaciais e ambientais, como correntes oceânicas, uso da terra e fontes de poluição, com modelos preditivos para gerar mapas de concentração de microplásticos.



2. Coleta e organização de Dados
    - Será utilizado diversas fontes de dados geoespaciais e ambientais para obter informações sobre correntes oceânicas, batimetria, uso da terra, entre outros.
    - Bases de dados:
      - Copernicus Marine Environment Monitoring Service (CMEMS)
        (https://marine.copernicus.eu/)
        
        Formatos disponíveis: netCDF e GeoTIFF
        
      - NOAA Global Marine Debris Database
        (https://marinedebris.noaa.gov/)
        
        Formato: NetCDF, CSV, ou JSON.
  
      - GEBCO - General Bathymetric Chart of the Oceans
        (https://www.gebco.net/)
        
        Formato: GEoTIFF ou NetCDF.
        
      - INPE - Instituto Nacional de Pesquisas Espaciais
        (http://www.inpe.br/)
        
        Formato: Shapefiles ou GeoTIFF.
        
      - IBGE Geoportal
        (https://www.ibge.gov.br/geociencias/)
        
        Formato: Shapefiles ou GeoTIFF.
        
        
    Os dados coletados serão organizados da seguinte forma:
   
        ├── satelite/
        ├── batimetria/
        ├── poluicao/
        └── uso_terra/
   
3. Documentação da metodologia

    - Será utilizado ferramentas de geoprocessamento como QGIS (https://qgis.org/) para processar os dados obtidos. O processamento seguirá: 
      - Limpeza e normalização dos dados;
      - Interpolação de dados geoespaciais (IDW, Kriging) quando necessário;
      - Integração de camadas de dados para gerar um conjunto de dados consolidado.
    
    Ferramentas:
    - QGIS para geoprocessamento.
    - Python (geopandas) para processamento de dados.

3. Modelagem de Aprendizado de Máquina
    - Será utilizado bibliotecas de aprendizado de máquina, como scikit-learn, XGBoost e TensorFlow, para construir modelos preditivos com base em fatores ambientais,
  correntes oceânicas e dados de concentração de microplásticos.
    - Modelos como: 
      - Random Forest
      - Regressão Linear
      - Redes Neurais (ANNs, CNNs)

4. Validação dos Modelos
    - A validação dos modelos será feita utilizando cross-validation e técnicas como MAE (Erro Médio Absoluto) e RMSE (Raiz do Erro Quadrático Médio) para verificar a precisão.
    - os dados serão dividos conjuntos de treino e teste para evitar overfitting.

5. Visualização e Relatório
    - Geração de mapas preditivos da distribuição de microplásticos no QGIS.
    - O relatório final deverá documentar a metodologia, resultados e interpretações.
   

## Estrutura de Arquivos

A estrutura de arquivos do projeto segue um formato modular para facilitar a organização e o desenvolvimento:

```bash
/
├── README.md               # Este documento
├── data/                   # Diretório com os dados brutos e processados
│   ├── raw/                # Dados brutos não processados
│   ├── processed/          # Dados processados 
├── notebooks/              # Jupyter notebooks para exploração de dados e modelagem
├── src/                    # Scripts de processamento de dados e modelos
│   ├── preprocessing.py    # Script de pré-processamento de dados
│   ├── train_model.py      # Script para treinar o modelo de aprendizado de máquina
│   └── evaluation.py       # Script para avaliação dos modelos
├── models/                 # Diretório onde os modelos treinados serão armazenados
└── results/                # Resultados das predições e visualizações (mapas, gráficos)

```
## Requisitos
Para reproduzir os resultados deste projeto, você precisará das seguintes ferramentas e bibliotecas instaladas:

### Ferramentas de Geoprocessamento
- **QGIS** 
- [Google Earth Engine](https://earthengine.google.com/) (opcional, para manipulação de grandes volumes de dados)

### Bibliotecas Python
- **Python 3.x**
- **Geopandas**: `pip install geopandas`
- **Rasterio**: `pip install rasterio`
- **Scikit-learn**: `pip install scikit-learn`
- **XGBoost**: `pip install xgboost`
- **TensorFlow** (opcional, se usar redes neurais): `pip install tensorflow`
- **Matplotlib/Seaborn**: Para visualização de dados.
