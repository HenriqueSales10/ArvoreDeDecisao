# Arvore de decisão
Este projeto implementa um classificador de árvore de decisão utilizando o conjunto de dados Iris, um dos mais populares datasets de classificação em machine learning. O objetivo é explorar a acurácia e o desempenho do modelo ao ajustar diferentes parâmetros, como a profundidade máxima da árvore (max_depth) e o critério de divisão (gini ou entropy).

#Visão Geral
O conjunto de dados Iris contém 150 amostras de flores de íris, classificadas em três classes:
- Setosa
- Versicolor
- Virginica
  
Cada amostra contém 4 características:
- Comprimento da sépala
- Largura da sépala
- Comprimento da pétala
- Largura da pétala
O objetivo é treinar um modelo de árvore de decisão para prever a espécie de uma flor com base nessas características.

#Análise dos Resultados
O código realizará o treinamento e a avaliação do modelo, gerando as seguintes saídas:

Acurácia: A precisão do modelo nos dados de teste.
Matriz de Confusão: Mostra a performance de classificação em termos de verdadeiros positivos e negativos.
Relatório de Classificação: Inclui métricas como precisão, recall e f1-score.
Além disso, o script gerará uma visualização gráfica da árvore de decisão, que será exibida automaticamente após o treinamento.

#Testes e Análises
O script permite testar diferentes configurações de profundidade máxima (max_depth) e critérios de divisão (gini e entropy). Esses parâmetros podem ser alterados no código e comparados os resultados.

Exemplos de Parâmetros:
max_depth = 2, 3, 5, 10: podem ser utilizadas diferentes profundidades para observar o impacto na acurácia e na matriz de confusão.
criterion = 'gini', 'entropy': Compare os critérios de divisão para verificar qual oferece melhor desempenho.

Exemplo de Saída (com max_depth=10, criterion='entropy'):

![image](https://github.com/user-attachments/assets/e44f4491-a5f1-4da9-b1b2-bfbe16df7f20)

Árvore gerada:

![image](https://github.com/user-attachments/assets/d41d9ed7-21ae-4dac-aab6-c100a8f44003)


Exemplo de Saída (com max_depth=3, criterion='gini'):

![image](https://github.com/user-attachments/assets/c3cf3a18-7591-4c26-968a-2edcbaf94d39)

Árvore gerada:

![image](https://github.com/user-attachments/assets/c85e4a6f-3043-44b8-b850-178450bbe07c)

Ao comparar com outro critério de divisão, como criterion='entropy', os resultados foram bem parecidos:

criterion='entropy'

Árvore gerada:

![image](https://github.com/user-attachments/assets/edbb113c-46c6-4aa6-9db1-e9ab2078f9c6)

Avaliação do modelo:

![image](https://github.com/user-attachments/assets/53a6ad99-0df6-4602-b1a0-a6cab8793c06)

criterion='gini'

Árvore gerada:

![image](https://github.com/user-attachments/assets/36c65da7-37f5-4882-871e-33458a905ffe)

Avaliação do modelo:

![image](https://github.com/user-attachments/assets/e7e8ca72-c43d-4754-be32-a5becc82479c)

Conclusão dos testes alterando o max_depth:
Reduzir a profundidade máxima (max_depth) da árvore para pode ajudar a evitar overfitting e tornar o modelo mais simples e rápido, mas isso vem ao custo de não capturar todas as nuances dos dados. No caso do Iris Dataset, conseguimos uma árvore bem interpretável, mas, dependendo do conjunto de dados e do problema, uma profundidade maior pode ser necessária para garantir uma boa performance.

Alterar o max_depth para 10 por exemplo, vai permitir que a árvore faça mais divisões e se ajuste mais aos dados de treino, o que pode aumentar a acurácia, mas com um risco maior de overfitting. Dependendo da natureza dos dados, pode ser benéfico ajustar esse parâmetro com cautela e realizar validação cruzada para encontrar o equilíbrio ideal entre a capacidade do modelo e a generalização.

Conclusão alterando o 'criterion':
Ambos os critérios (gini e entropy) resultaram em árvores de decisão que conseguiram classificar perfeitamente os dados de teste. Visualmente, as árvores são quase idênticas em termos das decisões tomadas, pois utilizaram os mesmos atributos para as divisões principais.

Impacto dos parâmetros no desempenho:
A variação entre gini e entropy em termos de estrutura da árvore foi mínima, o que indica que para este dataset específico, ambos os critérios têm um desempenho equivalente. Isso pode ser devido à simplicidade e ao equilíbrio do dataset Iris.
