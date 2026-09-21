# Tarefa 33 — Página pessoal com DaisyUI

Página pessoal desenvolvida para a disciplina de Design Web do IFRN - Zona Norte, utilizando os componentes do DaisyUI e classes utilitárias do Tailwind CSS. A proposta foi criar um layout funcional que refletisse meus interesses reais (como vôlei, animes e jogos no PC) sem perder o foco na estrutura exigida pela atividade.

## 📦 Lista dos Componentes DaisyUI Utilizados

- **`navbar`**: Utilizada no cabeçalho fixo (`header`) para criar a área de navegação superior.
- **`hero`**: Utilizado na Seção 2 (Apresentação) para criar um bloco de impacto visual grande, dividindo a tela entre meu avatar (a letra "L") e a minha descrição pessoal.
- **`badge`**: Utilizados na Seção de Apresentação para listar quem eu sou e meus hobbies (ex: `badge-primary` para "Estudante de TI", `badge-secondary` para "Jogadora de Vôlei", etc).
- **`card`**: Aplicado na grade de **Projetos** (contendo `card-body`, `card-title` e `card-actions`) e também para estruturar visualmente o formulário de contato.
- **`btn`**: Distribuído pela página com diversas variações para ações (`btn-primary`, `btn-secondary`, `btn-outline`, `btn-ghost`, `btn-circle`).
- **`alert`**: Utilizado na seção de Contato (`alert-info`) para destacar uma mensagem receptiva sobre recomendações de animes e sushi.
- **`form-control`, `input`, `textarea`, `select`, `label`**: Usados na construção do formulário. O `select` foi uma adição legal para criar um menu suspenso de assuntos (como marcar um vôlei ou falar do IFRN).
- **`theme-controller` (swap)**: Utilizado no cabeçalho para alternar os temas de forma interativa.
- **`footer`**: Utilizado para o rodapé padronizado.

## 🤔 Justificativa de Escolha (Hero vs Navbar)

Optei por utilizar **ambos** na mesma página, pois cumprem funções diferentes:
1. A **`navbar`** foi configurada para ficar fixa no topo (`fixed top-0`). Isso garante que, mesmo rolando a página até o final, o usuário tenha acesso rápido ao botão de trocar o tema e ao botão de contato.
2. O **`hero`** foi usado como a "vitrine" inicial. Ele é perfeito para alinhar o conteúdo em duas colunas de forma simples (`flex-col lg:flex-row-reverse`), garantindo que no celular o texto fique embaixo da imagem automaticamente.

## 🛠️ Pontos de Ajuste com Tailwind (Tailwind Puro)

Embora o DaisyUI facilite muito, usei o Tailwind puro para organizar a estrutura principal do layout. Dois exemplos importantes:

1. **Grade dos Projetos:** O DaisyUI não diz como os cards devem se alinhar. Usei `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8` para garantir que fiquem lado a lado no monitor e um embaixo do outro no celular.
2. **Alinhamento e Limites:** Usei `max-w-7xl mx-auto px-4` em várias seções para limitar a largura do conteúdo, evitando que os textos fiquem esticados demais em telas grandes e garantindo margens seguras no celular.

## 🎨 Reflexão sobre Temas (Winter vs Night)

Configurei a página para iniciar no tema `winter` e alternar para o `night`. 

Achei que a página ficou muito mais interessante no tema **`night`**. O contraste escuro combina mais com a vibe de quem gosta de jogar no PC, e as cores secundárias do tema dão um destaque neon muito legal para os botões e para as badges de hobbies, sem cansar a visão na hora de ler a seção de projetos.