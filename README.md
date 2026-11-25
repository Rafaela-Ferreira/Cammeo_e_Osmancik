# Projeto de Aprendizado de Máquina
## Classificação de variedades de arroz: Cammeo e Osmancik

**Grupo:** 8 - D3

**Integrante:** Rafaela Ferreira dos Santos - CP3026353

**Disciplina:** Introdução ao Aprendizado de Máquina

**Professor:** Everton Meyer da Silva

## 1. Sobre o projeto

Este projeto tem como objetivo utilizar técnicas de aprendizado de máquina para classificar grãos de arroz em duas variedades: **Cammeo** e **Osmancik**.

Para realizar a classificação, foram utilizadas características físicas dos grãos, como área, perímetro, comprimento dos eixos, excentricidade, área convexa e extensão.

O trabalho foi desenvolvido utilizando Python e bibliotecas de análise de dados e aprendizado de máquina.

## 2. Base de dados

A base utilizada contém informações sobre características físicas de grãos de arroz.

Os arquivos foram disponibilizados pelo professor e estão divididos em dois conjuntos:

- `rice_train.csv`: dados utilizados no treinamento e na validação dos modelos.
- `rice_test.csv`: dados utilizados na avaliação final.

**Quantidade de registros:**

| Conjunto | Registros |
|---|---:|
| Treinamento | 3.048 |
| Teste | 762 |
| **Total** | **3.810** |

**Fonte dos dados:**

[Dataset Rice Cammeo e Osmancik - GitHub](https://github.com/evertonjs/cmpinam-introducao-aprendizado-maquina/tree/main/projeto/datasets/CMPINAM_Dataset_03_Rice_Cammeo_Osmancik)

## 3. Tecnologias e bibliotecas

O projeto foi desenvolvido em Python, utilizando as seguintes bibliotecas:

- **Pandas:** leitura e organização dos dados.
- **NumPy:** operações numéricas.
- **Matplotlib:** criação de gráficos.
- **Seaborn:** visualização e análise dos dados.
- **Scikit-learn:** criação, treinamento e avaliação dos modelos de aprendizado de máquina.

## 4. Etapas do projeto

O projeto foi dividido nas seguintes etapas:

### 4.1 Preparação dos dados

- Verificação das dimensões da base.
- Análise dos tipos de dados.
- Verificação de valores ausentes e duplicados.
- Identificação de valores inválidos.
- Análise de possíveis outliers.

### 4.2 Análise exploratória dos dados (EDA)

Foram realizadas análises para entender melhor as características dos grãos e identificar diferenças entre as duas variedades.

Foram utilizadas tabelas e gráficos para observar a distribuição dos dados, comparar as características físicas e analisar as correlações entre as variáveis.

### 4.3 Modelagem

Foram testados quatro modelos de aprendizado de máquina:

- Dummy Classifier
- Decision Tree
- Random Forest
- SVM (Support Vector Machine)

Os modelos foram comparados utilizando as métricas de acurácia, precisão, recall e F1-score.

Também foi utilizada validação cruzada estratificada com cinco divisões.

### 4.4 Ajuste de hiperparâmetros

Após a comparação inicial, o SVM foi escolhido para o ajuste de hiperparâmetros.

Foi utilizado o GridSearchCV para testar diferentes combinações de parâmetros e encontrar a configuração com melhor resultado.

### 4.5 Avaliação final

O modelo ajustado foi avaliado utilizando os dados de teste, que permaneceram separados durante o treinamento.

Foram analisadas as métricas de classificação e a matriz de confusão.

## 5. Resultados

Na comparação inicial, o SVM apresentou o melhor resultado entre os quatro modelos.

| Modelo | Acurácia | F1-score |
|---|---:|---:|
| Dummy Classifier | 57,22% | 36,39% |
| Decision Tree | 88,68% | 88,44% |
| Random Forest | 92,22% | 92,05% |
| SVM | 93,24% | 93,10% |

Após o ajuste de hiperparâmetros, a melhor configuração encontrada para o SVM foi:

- **C:** 10
- **Kernel:** linear
- **Gamma:** scale

O F1-score obtido na validação cruzada foi de aproximadamente **93,27%**.

Na avaliação final com os dados de teste, os resultados foram:

| Métrica | Resultado |
|---|---:|
| Acurácia | 91,86% |
| Precisão | 91,93% |
| Recall | 91,42% |
| F1-score | 91,64% |

O modelo apresentou F1-score de 90% para Cammeo e 93% para Osmancik.

## 6. Conclusão

Com o desenvolvimento do projeto, foi possível observar que as características físicas dos grãos podem ajudar na identificação das variedades Cammeo e Osmancik.

Entre os modelos testados, o SVM apresentou o melhor desempenho na comparação inicial e também obteve bons resultados na avaliação final.

O modelo alcançou 91,86% de acurácia e 91,64% de F1-score nos dados de teste.

Como melhoria, poderiam ser testados outros modelos e diferentes configurações para tentar aumentar o desempenho da classificação.

## 7. Como executar o projeto

O notebook pode ser executado pelo Google Colab.

1. Baixe ou clone este repositório.
2. Abra o arquivo `Projeto_Aprendizado_Maquina.ipynb` no Google Colab.
3. Faça o upload dos arquivos `rice_train.csv` e `rice_test.csv`.
4. Confira se os caminhos dos arquivos CSV estão corretos.
5. Execute as células do notebook na ordem.

## 8. Estrutura do projeto

```text
Projeto-Aprendizado-de-Maquina/
│
├── Projeto_Aprendizado_Maquina.ipynb
├── rice_train.csv
├── rice_test.csv
└── README.md
```

---

**Projeto desenvolvido para a disciplina de Introdução ao Aprendizado de Máquina - 2º semestre de 2026.**