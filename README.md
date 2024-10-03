# Segmentação de Clientes para Marketing (Power BI + Python)

Este projeto foi desenvolvido durante o curso **"Microsoft Power BI Para Business Intelligence e Data Science"** da Data Science Academy (DSA). O objetivo foi criar um modelo de **segmentação de clientes** para a área de marketing, utilizando **Python** para a criação do modelo de machine learning e o **Power BI** para a visualização dos dados.

## Funcionalidades

- **Segmentação de Clientes**: O sistema realiza a segmentação de clientes com base em dados de marketing, utilizando algoritmos de machine learning.
- **Visualização Interativa**: O Power BI foi utilizado para criar um dashboard interativo, permitindo a análise visual das diferentes segmentações de clientes.
- **Integração com Python**: A integração entre Python e Power BI foi utilizada para criar o modelo de machine learning que segmenta os clientes.

## Tecnologias Utilizadas

- **Power BI**: Ferramenta utilizada para construção do dashboard e visualização dos dados.
- **Python**: Utilizado para a criação do modelo de machine learning.
- **Bibliotecas Python**: Foram utilizadas bibliotecas como `pandas`, `scikit-learn`, entre outras, para manipulação e análise dos dados.

## Pré-requisitos

Antes de executar este projeto, certifique-se de ter instalado:

- [Power BI Desktop](https://powerbi.microsoft.com/pt-br/desktop/)
- [Python](https://www.python.org/downloads/) (versão 3.7 ou superior)
- [Pacotes Python](https://pypi.org/) necessários como `pandas`, `scikit-learn`, `matplotlib`, entre outros.

## Instruções para Execução

### 1. Criando o Modelo de Machine Learning com Python

A primeira etapa do projeto foi criar o modelo de segmentação de clientes em Python. O código foi escrito em um ambiente Python (como o Jupyter Notebook ou VSCode) para treinar o modelo utilizando dados de marketing.

![Criando o machine learning em Python](https://github.com/luanalamonica/Machine-Learning/blob/main/primeira%20tela.png)

#### Código Exemplo em Python

```python
# Importando bibliotecas
import pandas as pd
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt

# Carregando os dados
dados = pd.read_csv('clientes.csv')

# Criando o modelo de segmentação
modelo = KMeans(n_clusters=4)
modelo.fit(dados)

# Adicionando os rótulos de segmentação aos dados
dados['Segmento'] = modelo.labels_

# Visualizando os segmentos
plt.scatter(dados['Renda'], dados['Idade'], c=dados['Segmento'])
plt.xlabel('Renda')
plt.ylabel('Idade')
plt.show()
```

## 2. Criando o Dashboard no Power BI

Com o modelo de machine learning criado em Python, a segunda etapa foi a construção de um **dashboard no Power BI**, onde os dados segmentados são visualizados de forma interativa.

### Passos para Importar o Script Python no Power BI:

1. Abra o **Power BI Desktop**.
2. Vá até a aba **Visualizações** e selecione **Visual Python Script**.
3. Copie e cole o código Python no editor de script do Power BI.
4. Execute o script e visualize os resultados diretamente no dashboard do Power BI.
5. Personalize o dashboard com gráficos adicionais e filtros conforme necessário.

## Como Executar o Projeto

1. Clone este repositório:

    ```bash
    git clone https://github.com/luanalamonica/Machine-Learning.git
    ```

2. Abra o código Python em um ambiente de desenvolvimento como **Jupyter Notebook** ou **VSCode**, e execute o script para gerar o modelo de segmentação.

3. No Power BI, importe o script Python e configure os gráficos interativos no dashboard.

4. Explore o dashboard para visualizar os segmentos de clientes criados pelo modelo.

## Estrutura do Projeto

- **Python Scripts**: Contém os scripts Python usados para criar o modelo de machine learning.
- **Dashboard Power BI**: Dashboard interativo criado no Power BI, visualizando as segmentações geradas pelo modelo.

## Melhorias Futuras

- Implementar outros algoritmos de segmentação para comparação de resultados.
- Adicionar mais variáveis para refinar as segmentações dos clientes.
- Criar uma análise preditiva para estimar o comportamento de diferentes segmentos.
- Incluir notificações automáticas no Power BI para alertar mudanças nos segmentos de clientes.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para adicionar novas funcionalidades, melhorar o código ou ajustar o dashboard. Para contribuir:

1. Faça um _fork_ deste repositório.
2. Crie uma _branch_ com a nova funcionalidade (`git checkout -b feature/nova-funcionalidade`).
3. Envie suas alterações para o repositório (`git push origin feature/nova-funcionalidade`).
4. Abra um _pull request_ para revisão.
