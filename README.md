# Clube do Livro Técnico - Repositório de Conteúdo

Este repositório atua como um sistema de gerenciamento de conteúdo (CMS) baseado em arquivos para os sites de divulgação do **Clube do Livro Técnico**.

<p align="center">
  <img src="assets/capa-clube-do-livro.png" alt="Logo do Clube do Livro" width="400"/>
</p>

## 🎯 Objetivo

O objetivo central deste repositório é centralizar e organizar todos os documentos, resumos, quizzes e ativos visuais dos encontros do clube. A estrutura foi projetada para facilitar o consumo desses dados via **GitHub API**, permitindo que sites externos exibam dinamicamente as informações sobre os livros lidos e os debates realizados.

## 📂 Estrutura do Repositório

*   **`assets/`**: Contém as capas dos livros e imagens promocionais utilizadas nos sites.
*   **`encontros/`**: Organizado por pastas datadas (`MM-DD.MM.YY`), cada uma contendo:
    *   **Resumos (`*-Summary-*.md`)**: Documentação dos principais pontos discutidos em cada capítulo.
    *   **Quizzes (`*-Quiz-*.json`)**: Testes de conhecimento em formato JSON para integração com componentes interativos.
    *   **Diagramas (`*.excalidraw`)**: Desenhos e mapas mentais criados durante as discussões.

## 🚀 Integração

Os dados podem ser recuperados utilizando os endpoints de conteúdo da API do GitHub:
`https://api.github.com/repos/{owner}/{repo}/contents/encontros`

Isso permite a criação de front-ends modernos e estáticos que se mantêm atualizados conforme novos commits são realizados neste repositório.

## Exemplo de Site
- https://clube-do-livro-tecnico.vercel.app/

*Se você criar um site nos avise que o colocamos aqui 😄*

---

## Sobre o Clube do Livro
- **Frequência:** Realizamos encontros **semanais** para discutir os capítulos designados.
- **Comunicação:** Nossa principal plataforma de comunicação é o canal [**Clube do Livro Técnico no Discord**](https://discord.com/channels/1370535949313773620/1435761943372763368).
- **Discussões:** As reuniões ocorrem em um canal de voz da comunidade Berolab no Discord.
- **Dinâmica:** Os integrantes devem ter ler o conteúdo especificado para a reunião. (Se você não tiver lido, pode ir para a reunião também, mas o seu aproveitamento do Clube será melhor se tiver lido).
- **Duração do encontro:** 1 hora.

---
*Mantido pelos membros do Clube do Livro Técnico.*
