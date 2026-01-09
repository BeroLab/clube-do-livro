---
{
  "date": "08/12/2025",
  "book": "Entendendo Algoritmos",
  "topic": "Capítulo 10: K-vizinhos Mais Próximos"
}
---

# Resumo: Entendendo Algoritmos - Capítulo 10
## K-vizinhos Mais Próximos (k-Nearest Neighbors - KNN)

Este capítulo apresenta o algoritmo KNN, uma técnica fundamental para sistemas de classificação e regressão.

### Tópicos Principais

#### 1. Como funciona o KNN?
- O algoritmo baseia-se na ideia de que "pássaros da mesma plumagem voam juntos". 
- Se você quer classificar algo, olha para os "vizinhos" mais próximos dele em um gráfico.
- **K:** É o número de vizinhos que você vai consultar (geralmente um número ímpar para evitar empates).

#### 2. Extração de Características (Feature Extraction)
- Para comparar dois itens, você precisa transformá-los em números. 
- Exemplo de recomendação de filmes: você avalia filmes por categorias (Comédia, Ação, Drama) em uma escala de 1 a 5.
- Essas notas tornam-se coordenadas em um gráfico multidimensional.

#### 3. Calculando a Distância
- O livro utiliza a **Fórmula de Pitágoras (Distância Euclidiana)** para medir o quão longe um ponto está do outro: 
  `√( (x1-x2)² + (y1-y2)² + ... )`
- Quanto menor a distância, mais parecidos são os itens.

#### 4. Classificação vs. Regressão
- **Classificação:** Prever uma categoria (Ex: "Este e-mail é spam ou não?").
- **Regressão:** Prever um número (Ex: "Quantos pães esta padaria vai vender amanhã baseado no clima e no dia da semana?").

### Conclusão do Capítulo
O KNN é a porta de entrada para o aprendizado de máquina (Machine Learning). Ele mostra que, com os dados certos e uma forma de medir similaridade, podemos fazer previsões surpreendentemente precisas. O segredo do sucesso do KNN está em escolher as **características certas** para comparar.
