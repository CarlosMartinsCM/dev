# Conda
Environment management

## Análise de dados
Environment para análise de dados:

> criar ambiente:
```bash
conda create -n dataview python=3.7
conda activate dataview
```

> instalar dependências:
```bash
conda install -c anaconda mysql-connector-python -y
conda install -c conda-forge notebook -y
conda install -c anaconda pymongo -y
conda install pandas scikit-learn matplotlib -y
pip install wget
```
