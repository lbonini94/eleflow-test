## Qual a diferença entre um aprendizado de máquina supervisionado e um não supervisionado? Dê exemplos de algorítimos para cada um.

Aprendizado supervisionado depende de uma base histórica de dados e resultados conhecidos para tentar prever resultados futuros a partir de novos dados. Ex:

- Previsão de vendas
- Classificação de plantas

Exemplos de algoritimos são: Support Vector Machines (SVM), KNN e Decision Tree.

Aprendizado não supervisionado utiliza-se de uma base histórica onde não se tem um resultado específico. Ex:

- Clusterização para segmentação de clientes

Exemplos de algoritimos são: KMeans, Mean Shift e DBSCAN

---
## Após a execução de dois algorítimos diferentes de machine learning foram resultadas as seguintes matrizes de confusão:

```
MatrizModelo1
[5740,  519]
[1119, 9413]

MatrizModelo2
[6751,  705]
[2005, 7330]
```

## Analisando apenas essas matrizes qual modelo você considera o melhor para ser utilizado? Justifique sua resposta

```
Total de registros = 16791

Acurácia = (VP + FN) / (VP + VN + FP + FN)
Precisão = VP / (VP+FP)
Recall = VP / (VP+FN)

P1 = 5740 / (5740 + 1119) = 0,836856685
R1 = 5740 / (5740 + 519)  = 0,917079406
A1 = (5740 + 519) / 16791 = 0,372759216

P2 = 6751 / (6751 + 2005) = 0,771014162
R2 = 6751 / (6751 + 705)  = 0,905445279
A2 = (6751 + 705) / 16791 = 0,444047406
```
Utilizado para que?
Sem entender o contexto de utilização é um pouco complicado determinar qual modelo utilizar. O modelo 2 parece ter uma melhor acurácia porém, ao considerar os pesos de cada erro (Tipo I e Tipo II) em uma situação onde o propósito seja 'detectar' alguma coisa, a história pode mudar pois o modelo 1 tem um melhor recall e precisão.


