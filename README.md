# Maximização de rendimento agrícola por algoritmos genéticos
*Grupo:* Emelyn Alves, João O. de A. Nascimento, Kayllany L. da S. Oliveira
<br>
*Instituição:* Ilum - Escola de Ciência 
<br>
*Professor:* Daniel R. Cassar
<br>
*Disciplina:* Redes Neurais e Algoritmos Genéticos

## Apresentação 
Como segundo projeto final da disciplina propusemos o uso de algoritmos genéticos para maximização de rendimento agrícola previsto por aprendizado de máquina (redes neurais e floresta aleatória) utilizando dados sintéticos.

**Para o leitor curioso:** verifique o primeiro projeto da disciplina [Previsão de rendimento agrícola por redes neurais tipo MLP](https://github.com/Joao-otavio04/Projeto_Final_Redes_Neurais/blob/main/README.md). 

## Importância 
O uso de algoritmos genéticos para maximização de um rendimento agrícola previsto pode ser uma ferramenta para busca de melhores condições de plantio de uma cultura. Além disso, levando em consideração situações socio-ambientais e econômicas, como: alto crescimento populacional, mudanças climáticas e aumento do custo de produção e comércio de alimentos; a busca pelo aumento do rendimento agrícola se faz cada vez mais necessária, como forma de implementação de uma agricultura mais sustentável e eficiente. 

Para saber mais sobre o rendimento agrícola verifique [`Brevíssimas considerações sobre rendimento agrícola`](https://github.com/Joao-otavio04/Projeto_Final_Redes_Neurais/blob/main/README.md#brev%C3%ADssimas-considera%C3%A7%C3%B5es-sobre-rendimento-agr%C3%ADcola). 

## Dataset 
O conjunto de dados escolhido [Synthetic Agricultural Yield Prediction Dataset](https://www.kaggle.com/datasets/blueloki/synthetic-agricultural-yield-prediction-dataset/data) foi retirado do site [Kaggle](https://www.kaggle.com/) e apresenta as seguintes características: 

1. Dados sintéticos, ou seja, não reais.
2. Conjunto com split treino-teste aplicado:
   * `agricultural_yield_train.csv` (treino; 16000 linhas x 7 solunas) - arquivo `.csv` com dados de treino. 
   * `agricultural_yield_test.csv`(teste; 4000 linhas x 7 colunas). - arquivo `.csv` com dados de teste. 
3. 7 atributos:
   * `Soil_Quality` - Índice de qualidade do solo, variando de 50 a 100.
   * `Seed_Variety` -  Indicador binário de variedade de semente, onde 1 representa uma variedade de alto rendimento.
   * `Fertilizer_Amount_kg_per_hectare`- A quantidade de fertilizante utilizada em quilogramas por hectare.
   * `Sunny_Days` - O número de dias ensolarados durante a estação de crescimento.
   * `Precipitação_mm` - Precipitação total recebida durante a estação de crescimento em milímetros.
   * `Irrigation_Schedule` - O número de irrigações durante a estação de crescimento.
   * `Yield_kg_per_hectare` - O rendimento agrícola em quilogramas por hectare, servindo como variável alvo para previsão. [1] (texto traduzido pelo Google Translator)
4. Target (para aprendizado de máquina): `Yield_kg_per_hectare` - Rendimento agrícola (kg/hec)
   
## Repositório 
* `Projeto Final GA - Floresta Aleatória.ipynb` - Jupyter notebook em python que apresenta a maximização por algoritmos genéticos do rendimento previsto por floresta aleatória;
* `Projeto Final GA - Rede Neural.ipynb` - Jupyter notebook em python que apresenta a maximização por algoritmos genéticos do rendimento previsto por redes neurais tipo MLP (_Multi Layer Perceptron_). Saiba mais em: [Previsão de rendimento agrícola por redes neurais tipo MLP](https://github.com/Joao-otavio04/Projeto_Final_Redes_Neurais/blob/main/README.md);
* `README.md` - Arquivo que contém as informações gerais sobre o projeto. Você está aqui! :)
* `agricultural_yield_test.csv` - Conjunto de dados de teste sintéticos;
* `agricultural_yield_train.csv` - Conjunto de dados de treino sintéticos.

Todos os arquivos acima estão no `main branch` do repositório.
Os arquivos `.ipynb` apresentam textos entre células de código que auxiliam seu entendimento. 

### Como navegar?
1. Baixe os arquivos `.csv`;
2. Baixe os arquivos `.ipynb`;
3. Mantenha todos os arquivos (`.csv` e `.ipynb`) no mesmo ambiente; 
4. Execute os códigos no JupyterLab.

## Requisitos 
1. Python instalado;
2. JupyterLab habilitado;
3. Obter arquivos `.csv` e `.ipynb` do repositório;
4. Python configurado para importar bibliotecas e módulos necessários.

## Bibliotecas/Módulos e suas funções (no projeto)
* `pandas` - importar e tratar dados;
* `random` - aleatorizar a escolha dos parâmetros de plantio;
* `matplotlib` - plotar gráfico de curva de aprendizado;
* `scipy ` - calcular a distância Manhattan entre valores previstos e valores reais;
* `sklearn` - calcular o RMSE, aplicar o modelo de floresta aleatória, normalização e realizar split de dados;
* `numpy` - cálculos gerais (média, desvio padrão, mínimo e máximo) e remodelação dos dados;
* `torch` - conversão de dados em tensores;
* `pytorch lighting` - criar e treinar a rede neural;
* `pickle` - módulo que serializa e salva o estado do modelo treinado, no caso, a rede neural [2];
* `deap` - módulo que auxilia na construção do algoritmo genético.

## Conclusão 
As maximizações por algoritmos genéticos do rendimento previsto por floresta aleatória e redes neurais tipo MLP retornaram rendimentos de aproximadamente 1351.9 kg/hec e 1905.6 kg/hec, respectivamente. A partir disso, verificamos que o algoritmo genético funcionou, ou seja, buscou maior rendimento agrícola.  

Os indivíduos vencedores foram: 
* Floresta Aleatória - [70.2 1.0 292.7 115.8 165.8 14.0]
* Redes Neurais tipo MLP - [53.5 0 68.6 107.8 710.5 10]
(os valores de cada gene foram bruscamente aproximados, verifique os valores reais obtidos em: [`Projeto Final GA - Floresta Aleatória.ipynb`](https://github.com/emelyn23017/projeto.final_alg.geneticos/blob/main/Projeto%20Final%20GA%20-%20Floresta%20Aleat%C3%B3ria.ipynb) e [`Projeto Final GA - Redes Neurais.ipynb`](https://github.com/emelyn23017/projeto.final_alg.geneticos/blob/main/Projeto%20Final%20GA%20-%20Rede%20Neural.ipynb))

## Referências 

**README:**

[1] [Conjunto de dados sintéticos de previsão de rendimento agrícola - "Synthetic Agricultural Yield Prediction Dataset"](https://www.kaggle.com/datasets/blueloki/synthetic-agricultural-yield-prediction-dataset/data)
<br>
[2] [pickle — Python object serialization](https://docs.python.org/3/library/pickle.html)
<br>
**Notebooks:**

[Correção dos comentários pelo chat gpt](https://chatgpt.com/share/10d26082-5f91-4ba4-a995-a28e0dd37d2e)
<br>
[Evolutionary Tools — DEAP 1.4.1 documentation](https://deap.readthedocs.io/en/master/api/tools.html#deap.tools.cxUniform)
