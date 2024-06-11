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

**Para o leitor curioso:** verifique o primeiro projeto da disciplina: [Previsão de rendimento agrícola por redes neurais tipo MLP](https://github.com/Joao-otavio04/Projeto_Final_Redes_Neurais/blob/main/README.md). 

## Importância 
O uso de algoritmos genéticos para maximização de um rendimento agrícola previsto pode ser uma ferramenta para busca de melhores condições de plantio. Além disso, levando em consideração situações socio-ambientais e econômicas, como: alto crescimento populacional, mudanças climáticas e aumento do custo de produção e comércio de alimentos; a busca pelo aumento do rendimento agrícola se faz cada vez mais necessária, como forma de implementação de uma agricultura mais sustentável e eficiente. 

Para saber mais sobre o rendimento agrícola verifique a sessão `Brevíssimas considerações sobre rendimento agrícola` em [Previsão de rendimento agrícola por redes neurais tipo MLP](https://github.com/Joao-otavio04/Projeto_Final_Redes_Neurais/blob/main/README.md). 

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
   * `Precipitação_mm` - precipitação total recebida durante a estação de crescimento em milímetros.
   * `Irrigation_Schedule` - O número de irrigações durante a estação de crescimento.
   * `Yield_kg_per_hectare` - O rendimento agrícola em quilogramas por hectare, servindo como variável alvo para previsão. [2] (texto traduzido pelo Google Translator)
4. Target (para aprendizado de máquina): `Yield_kg_per_hectare` - Rendimento agrícola (kg/hec)
   
## Repositório 
* `Projeto Final GA - Floresta Aleatória.ipynb` - Jupyter notebook em python que apresenta a maximação por algoritmos genéticos do rendimento previsto por floresta aleatória.
* `Projeto Final GA - Rede Neural.ipynb` - Jupyter notebook em python que apresenta a maximação por algoritmos genéticos do rendimento previsto por redes neurais tipo MLP (_Multi Layer Perceptron_). Saiba mais em: [Previsão de rendimento agrícola por redes neurais tipo MLP](https://github.com/Joao-otavio04/Projeto_Final_Redes_Neurais/blob/main/README.md)
* `README.md` - Arquivo que contém as informações gerais sobre o projeto. Você está aqui! :)
* `agricultural_yield_test.csv` - conjunto de dados de teste sintéticos
* `agricultural_yield_train.csv` -conjunto de dados de treino sintéticos

Todos os arquivos acima se encontram no main branch do repositório.
Os arquivos `.ipynb` apresentam textos entre células de código que auxiliam seu entendimento. 

### Como navegar?
1. Baixe os arquivos `.csv`;
2. Baixe os arquivos `.ipynb`;
3. Mantenha todos os arquivos (`.csv` e `.ipynb`) no mesmo ambiente; 
4. Execute os códigos no JupyterLab.

## Requisitos 
1. Python instalado;
2. JupyterLab habilitado;
3. Obter arquivos .csv e .ipynb do repositório;
4. Python configurado para importar bibliotecas e módulos necessários.

## Bibliotecas/Módulos e suas funções (no projeto)
* `pandas` - importar e tratar dados;
* `random` - aleatorizar a escolha dos parâmetros de plantio;
* `matplotlib` - plotar gráfico de curva de aprendizado;
* `scipy ` - calcular a distância Manhattan entre valores previstos e valores reais;
* `sklearn` - calcular o RMSE e aplicar o modelo de floresta aleatória;
* `numpy` - cálculos gerais (média, desvio padrão, mínimo e máximo) e remodelação dos dados;
* `deap` - módulo que auxilia na construção do algoritmo genético.

## Considerações teóricas 

## Conclusão 

## Referências 
https://deap.readthedocs.io/en/master/api/tools.html#deap.tools.cxUniform
Evolutionary Tools — DEAP 1.4.1 documentation
