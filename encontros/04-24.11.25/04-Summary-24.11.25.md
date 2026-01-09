---
{
  "date": "24/11/2025",
  "book": "Entendendo Algoritmos",
  "topic": "Capítulo 8: Algoritmos Gulosos"
}
---

# Resumo: Entendendo Algoritmos - Capítulo 8
## Algoritmos Gulosos (Greedy Algorithms)

Este capítulo explora uma classe de algoritmos simples e intuitivos, ideais para problemas onde encontrar a solução perfeita é muito demorado.

### Tópicos Principais

#### 1. O que é um Algoritmo Guloso?
- A estratégia é simples: a cada etapa, escolha a opção que parece ser a melhor naquele momento (o "ótimo local").
- A esperança é que, ao fazer escolhas ótimas locais, você acabe chegando a um "ótimo global".
- **Vantagem:** São fáceis de implementar e geralmente rápidos.
- **Desvantagem:** Nem sempre encontram a melhor solução possível, mas muitas vezes encontram uma solução "boa o suficiente".

#### 2. Problemas NP-Completos
O capítulo introduz problemas que são impossíveis de resolver perfeitamente em tempo razoável conforme a entrada cresce.
- **Exemplo Clássico:** O Problema do Caixeiro Viajante (Traveling Salesperson) e o Problema da Cobertura de Conjuntos.
- **Como identificar:**
  - Envolve testar "todas as combinações".
  - O problema fica lento muito rápido com poucos itens a mais.
  - Não há uma fórmula simples; você tem que calcular "X vs Y" para tudo.

#### 3. Algoritmos de Aproximação
Quando nos deparamos com problemas NP-Completos, não precisamos da solução perfeita, apenas de uma solução boa.
- Os algoritmos gulosos brilham aqui como **algoritmos de aproximação**.
- Exemplo do problema das estações de rádio (Cobertura de Conjuntos):
  - Solução exata: O(2ⁿ) - Impossível para muitos estados.
  - Solução gulosa: O(n²) - Escolher a estação que cobre mais estados não cobertos a cada passo.

### Conclusão do Capítulo
Algoritmos gulosos são uma ferramenta essencial no cinto de utilidades do programador. Eles ensinam a negociar a perfeição pela velocidade quando o problema é complexo demais (NP-Completo). Saber identificar quando "bom o suficiente" é a meta correta é uma habilidade crucial.
