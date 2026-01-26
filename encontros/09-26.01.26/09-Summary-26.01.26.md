---
{
  "date": "26/01/2026",
  "book": "O Programador Pragmatico",
  "topic": "Capítulo 2: De 'Os males da duplicação' até 'Projéteis Luminosos'"
}
---

# Resumo: O Programador Pragmático - Capítulo 2 (Parte 1)
## Uma Abordagem Pragmática - de 'Os males da duplicação' até 'Projéteis Luminosos'

O encontro aborda os primeiros tópicos do Capítulo 2, que trata de princípios fundamentais para o desenvolvimento de software de alta qualidade e fácil manutenção. O tema central é a importância de criar software que seja "fácil de mudar" (ETC), com os programadores assumindo a responsabilidade por isso.

Os principais conceitos discutidos hoje são:

*   **Os Males da Duplicação (DRY - Don't Repeat Yourself)**: Este princípio enfatiza que **cada pedaço de conhecimento deve ter uma representação única, inequívoca e autoritária** dentro de um sistema. A duplicação é um problema sério porque torna a manutenção um pesadelo. Se uma regra de negócio (ex: "juros de 5% ao mês") está escrita em múltiplos lugares, uma mudança nela exigirá encontrar e atualizar todas as suas ocorrências. Esquecer de atualizar apenas uma leva a inconsistências e bugs difíceis de rastrear.
    *   **Exemplo Prático**: Imagine uma regra de validação de senha que exige 8 caracteres. Se essa lógica estiver duplicada na interface do usuário (JavaScript) e no servidor (API), e o requisito mudar para 10 caracteres, é preciso lembrar de alterar em ambos. Se o desenvolvedor só alterar no servidor, a interface dará um feedback incorreto ao usuário, criando uma péssima experiência. A solução DRY seria ter essa regra definida em um único lugar, como uma constante ou configuração compartilhada.
    *   **Tipos de duplicação**:
        *   **Duplicação imposta:** Desenvolvedores sentem que não têm escolha (ex: ter que escrever código semelhante para diferentes frameworks).
        *   **Duplicação inadvertida:** Desenvolvedores não percebem que estão duplicando informações.
        *   **Duplicação impaciente:** Desenvolvedores duplicam por preguiça, pois parece mais fácil no curto prazo.
        *   **Duplicação entre desenvolvedores:** Múltiplas pessoas ou equipes duplicam uma informação por falta de comunicação.

*   **Ortogonalidade**: Refere-se ao design de componentes desacoplados e independentes. Em um sistema ortogonal, você pode alterar um componente sem causar efeitos colaterais nos outros. Isso aumenta a produtividade e reduz o risco.
    *   **Analogia**: Pense nos sistemas de um carro. O sistema de som é ortogonal ao sistema do motor. Você pode trocar o rádio por um modelo mais moderno sem que o carro pare de funcionar.
    *   **Benefícios**:
        *   **Produtividade**: Mudanças são localizadas, permitindo que equipes trabalhem em paralelo com menos conflitos.
        *   **Testes**: É muito mais fácil testar componentes isolados do que um sistema "emaranhado".
        *   **Redução de Risco**: Corrige-se um bug em um módulo com a confiança de que não se está quebrando outro. Um sistema não-ortogonal é frágil; uma pequena mudança pode causar uma cascata de erros.

*   **Reversibilidade**: Decisões importantes de projeto não devem ser escritas em pedra, mas na areia. O futuro é incerto, e os requisitos mudam. Um design flexível permite que o sistema se adapte a novas tecnologias, fornecedores ou requisitos sem a necessidade de uma reescrita completa.
    *   **Exemplo Prático**: Em vez de espalhar queries SQL nativas de um banco de dados específico (ex: Oracle) por todo o código, use um padrão de repositório ou um ORM. Essa camada de abstração isola o código da implementação do banco de dados. Se um dia for necessário migrar para o PostgreSQL, a maior parte da mudança ocorrerá nessa camada de abstração, em vez de em centenas de arquivos. Outro exemplo é encapsular chamadas a uma API de terceiro (ex: para pagamentos) em um módulo próprio. Se você decidir trocar de fornecedor, só precisará reescrever esse módulo.

*   **Tracer Bullets (Projéteis Luminosos)**: Em vez de criar um protótipo para depois jogá-lo fora, a abordagem dos projéteis luminosos consiste em construir um "esqueleto" do sistema que seja funcional de ponta a ponta. O objetivo é obter feedback rápido sobre a arquitetura, a integração entre as camadas (UI, lógica, banco de dados) e a viabilidade geral.
    *   **Diferença de Protótipos**: Um protótipo é usado para aprender algo e depois é descartado (ex: um mockup de UI para validar um fluxo com o usuário). Já o código de um projétil luminoso é mantido e evoluído.
    *   **Exemplo**: Para um novo site de e-commerce, o "tracer bullet" poderia ser um fluxo simples: exibir um único produto na tela, permitir adicioná-lo ao carrinho e navegar para uma página de checkout (ainda sem integração de pagamento). Embora mínimo, esse fluxo prova que o front-end, o back-end e o banco de dados estão conectados e funcionando. A partir daí, o esqueleto é "encorpado" com mais funcionalidades.

Em suma, esta primeira parte do Capítulo 2 orienta os desenvolvedores a adotar uma abordagem pragmática que prioriza a adaptabilidade, a responsabilidade e a criação de sistemas flexíveis e eficientes, focando nos conceitos de DRY, Ortogonalidade, Reversibilidade e Tracer Bullets.
