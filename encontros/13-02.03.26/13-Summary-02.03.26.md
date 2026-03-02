---
{
  "date": "02/03/2026",
  "book": "O Programador Pragmatico",
  "topic": "Capítulo 4: De 'Projeto por Contrato' até 'Quando usar exceções'"
}
---

# Resumo: O Programador Pragmático - Capítulo 4 (Parte 1)

## Pragmatic Paranoia - de 'Projeto por Contrato' até 'Quando usar exceções'

Este encontro explorou a primeira parte do Capítulo 4, que introduz o conceito de "Paranoia Pragmática". A premissa central é que, como ninguém escreve software perfeito, devemos construir sistemas que se protejam de nossos próprios erros e dos erros dos outros.

Os principais conceitos discutidos foram:

- **Projeto por Contrato (Design by Contract - DbC)**: Desenvolvido por Bertrand Meyer, o DbC é uma técnica para documentar e garantir as expectativas e responsabilidades de módulos de software. Um contrato define os direitos e deveres de quem chama (cliente) e de quem é chamado (fornecedor).
  - **Os Três Pilares do Contrato**:
    - **Pré-condições**: O que o cliente deve garantir antes de chamar a rotina (ex: um parâmetro não pode ser nulo). Se a pré-condição não for atendida, a rotina nunca deve ser executada. O ônus da prova é do cliente.
    - **Pós-condições**: O que a rotina garante que será verdade após sua execução (o resultado final e o estado do mundo).
    - **Invariantes de Classe**: Condições que devem ser sempre verdadeiras do ponto de vista do cliente. O método pode alterá-las internamente, mas ao terminar, o objeto deve estar em um estado consistente.
  - **A Filosofia "Preguiçosa"**: O DbC promove um código mais limpo porque o fornecedor pode ser "preguiçoso". Ele não precisa validar dados que o contrato já diz que o cliente deve garantir. Se o contrato diz "não aceite nulo", o código interno não precisa de um `if (x == null)`. Isso é o oposto da **Programação Defensiva**, onde todos desconfiam de todos, gerando redundância e ocultando erros de lógica.
  - **DbC e Herança (Liskov)**: O livro destaca que, ao usar polimorfismo, as subclasses devem respeitar o contrato da classe base. A regra de ouro é: uma subclasse pode **enfraquecer as pré-condições** (ser mais aceitante que o pai) e **fortalecer as pós-condições** (prometer mais ou ser mais específica que o pai), mas nunca o contrário.
  - **Benefícios Práticos**:
    - **Falha na Fonte**: Se um contrato é violado, o programa trava exatamente onde o erro de lógica ocorreu, facilitando imensamente a depuração.
    - **Documentação Viva**: O contrato é uma especificação técnica que pode ser verificada em tempo de execução, ao contrário de comentários que ficam obsoletos.

- **Programas Mortos Não Contam Mentiras (Dead Programs Tell No Lies)**: Este princípio defende que é muito mais seguro para um sistema ser interrompido do que continuar executando em um estado corrompido ou desconhecido.
  - **O Perigo do "Programa Aleijado"**: Um programa que ignora erros catastróficos e tenta "seguir em frente" pode causar danos muito maiores (como corrupção de banco de dados ou exclusão indevida de arquivos) do que um que simplesmente encerra. Um programa morto causa menos dano do que um programa operando incorretamente.
  - **Falhe Cedo (Fail Fast)**: A detecção imediata de um erro "impossível" permite que você pare o sistema exatamente no ponto da falha. Isso facilita a depuração, pois o rastro do erro ainda está fresco e não foi obscurecido por execuções subsequentes.
  - **O "Crash" é um Favor**: Não devemos ver o encerramento abrupto como algo a ser evitado a todo custo através de `try-catch` genéricos. Se o ambiente está instável ou o estado lógico é inválido, o crash é a coisa mais honesta e útil que o programa pode fazer pelo desenvolvedor.
  - **Não enterre exceções**: O livro critica a prática de "abafar" erros apenas para manter o programa rodando. Se você não pode tratar o erro de forma a garantir que o sistema voltou a um estado 100% seguro e conhecido, deixe-o falhar.
  - **A Filosofia "Let it Crash"**: Menciona-se como linguagens como Erlang e Elixir levaram esse conceito ao extremo, onde o sistema é projetado para que partes dele morram e sejam reiniciadas por supervisores, mantendo a robustez geral sem tentar salvar processos individuais condenados.

- **Programação Assertiva (Assertive Programming)**: Baseia-se na premissa de que "se algo não pode acontecer, use uma asserção para garantir isso". É uma ferramenta para validar suposições fundamentais sobre o estado do programa.
  - **O Instinto "Isso nunca vai acontecer"**: Sempre que você se pegar pensando ou comentando no código que uma determinada condição é impossível, esse é o lugar exato onde uma asserção deve ser inserida. Ela transforma um comentário passivo em uma verificação ativa.
  - **Validando o "Impossível"**: Asserções servem para verificar condições que você acredita serem logicamente impossíveis (ex: "esta lista nunca estará vazia aqui" ou "o resultado deste cálculo deve ser sempre positivo"). Se a asserção falha, o programa para imediatamente, provando que sua compreensão do código estava errada.
  - **Asserções vs. Tratamento de Erros**: É crucial distinguir os dois. Asserções lidam com situações que **nunca** deveriam ocorrer se o código estiver correto (bugs de lógica). O tratamento de erros lida com situações esperadas do mundo real (falha de rede, arquivo não encontrado). **Nunca use asserções para validar dados de entrada do usuário ou de APIs externas**; esses dados devem ser validados por código de tratamento de erros normal.
  - **Evitando "Heisenbugs"**: Uma asserção nunca deve ter efeitos colaterais. Se a chamada dentro do `assert` alterar o estado do sistema, o bug pode desaparecer quando você ativar a depuração e reaparecer quando desativar (um "Heisenbug"). O código `assert(status = get_status())` é um erro clássico.
  - **Mantenha as Asserções Ligadas**: O livro refuta o mito de que asserções devem ser removidas em produção. Elas são sua sentinela contra a "bit rot" (deterioração de software) e bugs que só aparecem sob carga real. Se a performance for uma preocupação real, identifique os pontos críticos, mas mantenha o restante ativo.
  - **Documentação Ativa e Viva**: Asserções descrevem as intenções do desenvolvedor de forma muito mais confiável que comentários, pois são verificadas em cada execução. Elas dizem: "Eu, o autor, garanto que neste ponto a variável X tem o valor Y".

- **Quando usar Exceções**: Exceções devem ser reservadas para eventos inesperados e verdadeiramente excepcionais.
  - **O Erro não é uma Exceção**: Se um erro faz parte do fluxo normal do programa (como um usuário digitando uma senha errada), ele deve ser tratado com fluxos de controle normais, não com exceções.
  - **O Custo das Exceções**: Exceções costumam ser caras em termos de performance e podem tornar o fluxo do código difícil de seguir ("GOTO disfarçado").
  - **Regra de Ouro**: Se você remover todos os tratadores de exceção e o programa ainda conseguir realizar a lógica básica (mesmo que falhe em casos de erro), então você está usando exceções corretamente.
