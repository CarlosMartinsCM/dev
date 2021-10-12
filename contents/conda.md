# Conda
Environment management

## Análise de dados
Environment para análise de dados:

> criar ambiente:
```bash
conda create -n dataenv python=3.8
conda activate dataenv
```

> instalar dependências:
```bash
conda install pandas scikit-learn matplotlib seaborn -y
conda install -c conda-forge notebook -y
conda install -c anaconda pymongo -y
conda install -c anaconda mysql-connector-python -y
pip install wget
```
