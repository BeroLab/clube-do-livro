---
{
  "date": "17/11/2025",
  "book": "Entendendo Algoritmos",
  "topic": "Capítulo 7: Algoritmo de Dijkstra"
}
---

# Resumo: Entendendo Algoritmos - Capítulo 7
## Algoritmo de Dijkstra

Este capítulo apresenta o **Algoritmo de Dijkstra**, utilizado para encontrar o caminho mais rápido (ou mais barato) em grafos ponderados.

### Tópicos Principais

#### 1. BFS vs. Dijkstra
- **Pesquisa em Largura (BFS):** Encontra o caminho com o *menor número de arestas*. Ideal para grafos não ponderados (onde todas as conexões são iguais).
- **Algoritmo de Dijkstra:** Encontra o caminho com o *menor peso total*. Ideal para grafos ponderados (onde as conexões têm custos, como tempo, distância ou valor).

#### 2. Como Funciona
O algoritmo opera em quatro passos principais:
1.  Encontre o vértice mais "barato" (menor custo) que ainda não foi processado.
2.  Atualize os custos dos vizinhos desse vértice. Se você encontrou um caminho mais barato para um vizinho, atualize o custo dele.
3.  Repita o processo até que todos os vértices tenham sido processados.
4.  Calcule o caminho final.

#### 3. Conceitos Importantes
- **Grafos Ponderados:** Grafos onde as arestas têm pesos (números associados).
- **Ciclos:** O algoritmo de Dijkstra funciona apenas em Grafos Acíclicos Dirigidos (DAGs) ou grafos com ciclos de peso positivo.
- **Pesos Negativos:** O algoritmo de Dijkstra **não funciona** com arestas de peso negativo. Para esses casos, utiliza-se o algoritmo de **Bellman-Ford**.

### Exemplo Prático
O autor utiliza o exemplo de uma troca de instrumentos musicais (piano) para ilustrar como encontrar o "caminho" de trocas que resulta no menor custo financeiro.

### Conclusão do Capítulo
Enquanto a BFS é ótima para encontrar o caminho com menos paradas, o Algoritmo de Dijkstra é a ferramenta certa quando as conexões têm custos diferentes. É amplamente utilizado em sistemas de GPS e roteamento de rede.
