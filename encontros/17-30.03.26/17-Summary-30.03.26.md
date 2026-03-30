---
{
  "date": "30/03/2026",
  "book": "O Programador Pragmatico",
  "topic": "Capítulo 7 - Antes do Projeto",
}
---

# Resumo: O Programador Pragmático

## Antes do Projeto

Neste encontro, discutimos o que acontece antes de uma linha de código ser escrita. Exploramos como coletar requisitos de verdade (e não apenas colhê-los na superfície), como resolver problemas aparentemente impossíveis identificando restrições reais, quando confiar nos instintos antes de começar, os perigos de especificar em excesso e os riscos de seguir cegamente metodologias formais.

Os principais conceitos são:

### 1. O Abismo dos Requisitos

Requisitos raramente estão na superfície — estão enterrados sob suposições, concepções erradas e política. O trabalho do desenvolvedor é cavá-los, não apenas coletá-los.

- **Requisitos vs. Política**: A política de negócio muda com frequência; o requisito deve capturar a necessidade abstrata. Em vez de "só o departamento de pessoal pode ver registros", o requisito correto é "só usuários autorizados podem acessar um registro". A política vira metadado.
- **Tornar-se um usuário**: A melhor forma de entender requisitos é trabalhar junto ao usuário no dia a dia. Isso também constrói empatia e confiança.
- **Documentação com casos de uso**: Casos de uso (como o modelo de Cockburn) ajudam a capturar cenários de sucesso, extensões, variações e questões em aberto sem se prender à interface.
- **Especificar em excesso é um perigo**: Bons documentos de requisitos permanecem abstratos. Requisitos descrevem necessidades, não arquitetura, projeto ou interface.
- **Rastrear o crescimento de requisitos**: Cada novo recurso tem impacto no cronograma. Rastrear quem pediu o quê e quando evita surpresas tardias.
- **Glossário do projeto**: Manter um glossário compartilhado garante que todos falem a mesma língua — usuários e desenvolvedores.
- **Dica 51: Não colete requisitos — cave-os**
- **Dica 52: Trabalhe com um usuário para pensar como um usuário**
- **Dica 53: Abstrações têm vida mais longa do que detalhes**
- **Dica 54: Use um glossário do projeto**

### 2. Resolvendo Problemas Impossíveis

Quando um problema parece impossível, o segredo está em identificar quais restrições são reais e quais são apenas noções pré-concebidas.

- **Restrições absolutas vs. aparentes**: Algumas restrições devem ser respeitadas; outras existem só na cabeça do desenvolvedor. Questionar cada uma é essencial.
- **Encontre a caixa**: "Pensar fora da caixa" não é suficiente. O verdadeiro desafio é encontrar onde a caixa está — ou seja, mapear com precisão os graus de liberdade reais do problema.
- **Perguntas-chave**: Diante de um impasse, pergunte: Há um caminho mais fácil? Por que isso é um problema? Precisa ser feito dessa maneira? Precisa mesmo ser feito?
- **Dica 55: Não pense fora da caixa — encontre a caixa**

### 3. Não Antes de Você Estar Pronto

Profissionais experientes sabem quando começar e quando esperar. Uma dúvida insistente antes de iniciar merece atenção.

- **Instinto como ferramenta**: Anos de experiência acumulam-se no subconsciente. Quando há relutância antes de começar, provavelmente há um motivo válido.
- **Bom senso ou procrastinação?**: Para distinguir os dois, comece um protótipo. Se a relutância some logo, era procrastinação. Se o protótipo revela um problema de premissa, os instintos estavam certos.
- **Cuidado com o protótipo que vira produto**: Ao criar um protótipo para investigar uma dúvida, não perca de vista que é um protótipo — não deixe ele evoluir para o código de produção sem intenção.
- **Dica 56: Só comece quando estiver pronto**

### 4. A Armadilha das Especificações

Especificar é necessário, mas especificar demais é um erro. Há um ponto além do qual mais detalhes geram mais problemas do que resolvem.

- **Idioma natural é impreciso**: Nenhuma especificação captura todos os detalhes de um sistema. Contratos jurídicos tentam ser precisos e ainda assim são ambíguos.
- **A camisa de força**: Especificações excessivamente prescritivas eliminam a habilidade e o julgamento do programador durante a implementação — justamente quando oportunidades de melhoria aparecem.
- **Especificação e implementação são facetas do mesmo processo**: Devem fluir uma para a outra sem fronteiras artificiais. O feedback da implementação alimenta a especificação.
- **Cuidado com especificações em cascata**: Construir especificações em cima de especificações sem protótipos intermediários leva a sistemas que não podem ser construídos.
- **Dica 57: Algumas coisas são fáceis de fazer, mas não de descrever**

### 5. Círculos e Setas

Metodologias formais são ferramentas, não dogmas. Adotá-las cegamente é tão perigoso quanto ignorá-las.

- **História das metodologias**: Programação estruturada, equipes do programador-chefe, CASE, cascata, espiral, OMT, UML — cada método teve seu momento de popularidade e foi substituído. Só a programação estruturada sobreviveu por mais tempo.
- **Problemas dos métodos formais**:
  - Diagramas ainda dependem de interpretação humana — não há verificação real pelo usuário final.
  - Tendem a gerar especialização e silos (modelo de dados vs. arquitetura vs. requisitos), prejudicando a comunicação.
  - Favorecem modelos estáticos, dificultando sistemas dinâmicos e baseados em metadados.
- **Custo de adoção**: Toda nova metodologia gera queda de produtividade antes de gerar ganhos. Nunca subestime esse custo.
- **Ferramentas caras não garantem projetos melhores**: O valor está no julgamento de quem as usa, não no preço ou no volume de diagramas produzidos.
- **Dica 58: Não seja escravo dos métodos formais**
- **Dica 59: Ferramentas caras não produzem projetos melhores**
