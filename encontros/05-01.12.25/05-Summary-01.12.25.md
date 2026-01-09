---
{
  "date": "01/12/2025",
  "book": "Entendendo Algoritmos",
  "topic": "Capítulo 9: Programação Dinâmica"
}
---

# Resumo: Entendendo Algoritmos - Capítulo 9
## Programação Dinâmica

Este capítulo apresenta a **Programação Dinâmica**, uma técnica para resolver problemas complexos que podem ser divididos em subproblemas que se sobrepõem.

### Tópicos Principais

#### 1. O que é Programação Dinâmica?
- É uma técnica que resolve subproblemas e armazena os resultados para uso posterior (geralmente em uma tabela/grade).
- Diferente da estratégia "Dividir para Conquistar" (que divide o problema em partes independentes), a Programação Dinâmica é usada quando os subproblemas dependem uns dos outros.

#### 2. O Problema da Mochila (Knapsack Problem)
- O capítulo usa o exemplo de um ladrão que quer maximizar o valor dos itens em sua mochila com capacidade limitada.
- Mostra por que uma abordagem gulosa falha e como a grade de programação dinâmica encontra a solução ótima testando todas as combinações de forma eficiente.

#### 3. Quando Usar?
- Quando você está tentando otimizar algo em relação a um limite (como o peso da mochila).
- Quando o problema pode ser dividido em subproblemas discretos.
- **Dica:** Se o problema envolve uma grade, ele provavelmente pode ser resolvido com programação dinâmica.

#### 4. Maior Substring Comum vs. Maior Subsequência Comum
- **Substring Comum:** Foca em caracteres consecutivos (ex: "hish" e "fish" -> "ish").
- **Subsequência Comum:** Foca no número de letras compartilhadas, mesmo que não estejam juntas (ex: "fosh" e "fish" -> "fsh").
- Essas técnicas são usadas em corretores ortográficos e para comparar fitas de DNA.

### Conclusão do Capítulo
A programação dinâmica é poderosa, mas difícil de dominar. Ela ensina que, às vezes, para resolver um problema grande, precisamos construir uma tabela de soluções para problemas pequenos e usá-los como blocos de construção. Não existe uma fórmula única para a grade; cada problema exige uma lógica de preenchimento diferente.
