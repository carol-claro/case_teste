Para esse case, optei por utilizar a nuvem do Azure para hospedar os CSVs. Notei que alguns CSVs necessitavam de transformações antes do carregamento, como colunas deslocadas,
ou não formatadas. 

1) Configurei o meu ambiente Azure, crianto uma Storage Account e um container no Azure Blob Service;
2) Configurei uma Azure Key Vault e ajustei as permissões, bem como o Secret, para poder conectar no ambiente sem a necessidade de expor as chaves no código;
3) No código, fiz a instalação do azure CLI e configuração para login no ambiente Azure e permissão;
4) Extrai os arquivos CSV do Blob Storage, transformando-os como necessário. Tentei ajustar os dados sensíveis com hashs para não serem expostos.
5) Executei as tabelas, para entender quais visões podiam ser extraídas. Achei interessante trazer uma visão por região de clientes e funcionários, analisando as
regiões com possiblidades de crescimento;
6) Decidi plotar alguns gráficos para ter uma visibilidade melhor das estatísticas.

7) Realizei todo o código no ambiente do Google Colab, por isso utilizei Pandas e as bibliotecas de plotagem. Com dados maiores, e um ambiente para execução com clusters gerenciados
 como o Databricks, utilizaria o PySpark para fazer os particionamentos das tabelas.

Link do Ambiente Google Colab: https://colab.research.google.com/drive/1RgjLx3m9yqrkgohNEHE-AEK-wf6A7mL1?authuser=1#scrollTo=TsyxOo0I-dG9

