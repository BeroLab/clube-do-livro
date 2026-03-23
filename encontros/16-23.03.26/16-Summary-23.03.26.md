---
{
  "date": "23/03/2026",
  "book": "O Programador Pragmatico",
  "topic": "Capítulo 6 - Enquanto Você Está Codificando"
}
---

# Resumo: O Programador Pragmático

## Enquanto Você Está Codificando

Neste encontro, discutimos como a codificação não é uma tarefa mecânica, mas sim um processo de decisões constantes que exigem ponderação e julgamento. Exploramos como evitar a sorte no desenvolvimento, como estimar o desempenho de algoritmos, a importância da refatoração contínua, a criação de código testável e os perigos do uso cego de ferramentas de geração automática.

Os principais conceitos são:

### 1. Programação Baseada no Acaso

Muitos desenvolvedores programam confiando na sorte ou em sucessos acidentais. O código funciona, mas eles não sabem exatamente por quê. Isso cria um "campo minado" de falsas conclusões.

- **Acidentes de Implementação**: Confiar em comportamentos não documentados ou condições limítrofes acidentais. Se a biblioteca mudar, o código quebra.
- **Acidentes de Contexto**: Suposições implícitas sobre o ambiente (como assumir que sempre haverá uma GUI ou que o usuário fala português).
- **Como Programar Deliberadamente**:
  - Estar sempre consciente do que se está fazendo.
  - Não codificar às cegas (conhecer a tecnologia e o plano).
  - Confiar apenas em coisas confiáveis e documentar suposições.
  - Testar as suposições com asserções.
- **Dica 44: Não programe por coincidência**: Evite confiar na sorte; se você não sabe por que funciona, não sabe por que vai falhar.

### 2. Velocidade do Algoritmo

Estimamos os recursos que os algoritmos consomem (tempo, memória, processador) usando a notação do "grande O" (O()).

- **Notação O()**: Define um limite superior para o crescimento do tempo ou memória em relação ao tamanho da entrada (n).
- **Categorias Comuns**: O(1) constante, O(lg(n)) logarítmica, O(n) linear, O(n lg(n)) pior que linear, O(n²) lei do quadrado, e O(2ⁿ) exponencial.
- **Estimativa por Bom Senso**: Identificar loops simples como O(n), loops aninhados como O(n²) e divisões binárias como O(lg(n)).
- **Dica 45: Estime a ordem de seus algoritmos**: Antes de codificar, tenha uma ideia de como o sistema escalará.
- **Dica 46: Teste suas estimativas**: O tempo real em produção é o que importa. Use geradores de perfil para validar suas teorias.

### 3. Refatoração

O software é mais parecido com jardinagem do que com construção civil. Ele é orgânico e precisa ser "podado" e reorganizado constantemente.

- **Quando Refatorar**: Sempre que houver duplicação (DRY), projeto não ortogonal, conhecimento desatualizado ou necessidade de melhor desempenho.
- **Gerenciamento da Angústia**: Não adie a refatoração por falta de tempo. Um "tumor" pequeno é mais fácil de remover agora do que um grande depois.
- **Como Refatorar com Segurança**:
  1. Não misture refatoração com novas funcionalidades.
  2. Tenha bons testes de regressão antes de começar.
  3. Dê passos curtos e deliberados.
- **Dica 47: Refatore cedo, refatore sempre**: Mantenha o código limpo e adequado às mudanças de requisitos.

### 4. Código que Seja Fácil de Testar

Assim como circuitos integrados têm pinos de teste, o software deve ser projetado para ser testável desde o início.

- **Teste de Unidade**: Testar cada módulo isoladamente para verificar se ele honra seu contrato (pré-condições e pós-condições).
- **Cultura de Teste**: Os testes devem ser fáceis de encontrar e executar. Embutir testes no próprio módulo ou em subdiretórios próximos ajuda na adesão.
- **Ferramentais de Teste (Harnesses)**: Use frameworks (como xUnit/JUnit) para padronizar a execução, análise de resultados e limpeza.
- **Dica 48: Projete para testar**: Comece a pensar no teste antes mesmo de escrever o código.
- **Dica 49: Teste seu software ou seus usuários testarão**: A prevenção custa menos do que o suporte técnico e a correção de bugs em produção.

### 5. Assistentes do Mal

Ferramentas que geram código automaticamente (Wizards) podem ser úteis, mas são perigosas se o desenvolvedor não entender o que foi gerado.

- **O Perigo da Perda de Controle**: O código gerado se mistura ao seu e você se torna responsável por ele. Se você não o entende, está programando por coincidência.
- **Dica 50: Não use um código de assistente que você não entender**: Entenda cada linha produzida em seu nome para manter o controle total do aplicativo.
