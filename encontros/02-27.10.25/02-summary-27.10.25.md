---
{
  "date": "27/10/2025",
  "book": "Entendendo Algoritmos",
  "topic": "Capítulos 5 e 6: Tabelas Hash e Pesquisa em Largura"
}
---

# Resumo: Entendendo Algoritmos - Capítulos 5 e 6

Neste resumo, abordamos duas estruturas de dados fundamentais e um algoritmo essencial para grafos.

## Capítulo 5: Tabelas Hash

As tabelas hash são estruturas de dados que permitem acesso extremamente rápido aos dados. Elas combinam uma função hash com um array.

### Conceitos Chave

1.  **Funções Hash:**
    - Uma função que mapeia uma string (ou outro dado) para um número (índice).
    - Deve ser consistente: a mesma entrada sempre gera a mesma saída.
    - Diferentes entradas devem, idealmente, gerar saídas diferentes.

2.  **Performance:**
    - **Caso Médio:** O(1) - Tempo constante para inserção, busca e remoção. É instantâneo, independentemente do tamanho da lista.
    - **Pior Caso:** O(n) - Tempo linear (se ocorrerem muitas colisões e todos os itens ficarem na mesma posição).

3.  **Colisões:**
    - Ocorrem quando duas chaves diferentes são mapeadas para o mesmo índice.
    - Solução comum: Criar uma lista encadeada nesse índice.
    - Para evitar colisões frequentes, é necessário um bom fator de carga e uma boa função hash.

4.  **Casos de Uso:**
    - Modelagem de relacionamentos (ex: agenda telefônica).
    - Filtragem de duplicatas.
    - Caching (memorização de dados para acesso rápido).

---

## Capítulo 6: Pesquisa em Largura (Breadth-First Search - BFS)

Este capítulo introduz grafos e como encontrar o "caminho mínimo" em situações não ponderadas.

### Conceitos Chave

1.  **Grafos:**
    - Modelam conexões.
    - Compostos por **Vértices** (nós) e **Arestas** (linhas que conectam os nós).
    - **Direcionados (Dígrafos):** A relação tem sentido (A -> B).
    - **Não Direcionados:** A relação é mútua (A - B).

2.  **Pesquisa em Largura (BFS):**
    - Responde a duas perguntas:
        1. Existe um caminho de A para B?
        2. Qual é o caminho mais curto (menor número de arestas)?
    - Explora o grafo em camadas: primeiro vizinhos diretos (1º grau), depois vizinhos dos vizinhos (2º grau), e assim por diante.

3.  **Filas (Queues):**
    - Estrutura de dados **FIFO** (First In, First Out).
    - Essencial para a implementação da BFS para garantir a ordem de verificação camada por camada.

4.  **Complexidade:**
    - **O(V + A)**, onde V é o número de vértices e A é o número de arestas.

### Exemplos Práticos
- Corretor ortográfico (menor número de edições).
- Encontrar o médico mais próximo na sua rede de contatos.
- Calcular a rota com menos conexões em um voo.