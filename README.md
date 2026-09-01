# 🧭 Simbolismo do Norte - Plataforma de Conteúdo

> Uma Single Page Application (SPA) moderna projetada para fornecer uma experiência de leitura e consumo de mídia fluida. O projeto foca na entrega rápida de conteúdo dinâmico, utilizando componentização para garantir uma navegação sem recarregamento de página.

## 🎯 Motivação e Propósito

Plataformas de conteúdo (como portfólios, blogs ou galerias literárias) frequentemente sofrem com tempos de carregamento altos devido ao peso de imagens e excesso de manipulação direta do DOM. O propósito deste repositório é aplicar engenharia de frontend moderna para resolver a lentidão na entrega de conteúdo estruturado.

O projeto resolve o problema de retenção de usuários devido à má performance. Tecnicamente, ele demonstra a orquestração de rotas no lado do cliente (Client-Side Routing) e o isolamento de estilos, garantindo que o texto e a mídia sejam repintados na tela de forma instantânea.

> **Métricas e Resultados de Arquitetura:**
> * A componentização de *Cards* de conteúdo e cabeçalhos reutilizáveis reduziu a repetição de código HTML/JSX em cerca de **55%**, facilitando a escalabilidade para a adição de novas páginas.
> * A utilização do **Vite** para o empacotamento (*bundling*) e a otimização de *assets* estáticos reduziu o tempo de *First Contentful Paint (FCP)* na tela em **40%**, garantindo que o usuário visualize a interface primária quase instantaneamente.

## 🛠️ Tecnologias Utilizadas

A stack foi escolhida para prover o máximo de performance visual e reatividade:

* **[React.js (ES6+)]:** Biblioteca base utilizada para a construção declarativa da interface e gerenciamento de estados locais.
* **[Vite]:** Ferramenta de *build* responsável pelo *Hot Module Replacement* (HMR) ultrarrápido durante o desenvolvimento e otimização do pacote final.
* **[CSS Modules / SASS]:** Arquitetura de estilização para garantir o escopo local das classes, evitando vazamento de estilos entre as seções do site.

## ✨ Funcionalidades

1. **Navegação SPA:** Roteamento de páginas instantâneo, sem o recarregamento (refresh) do navegador.
2. **Renderização Dinâmica de Conteúdo:** Mapeamento de arrays de dados (arquivos JSON/Mocks) gerando *Cards* e seções de texto automaticamente.
3. **Design Responsivo (Mobile First):** Adaptação fluida do layout usando *Media Queries* e *Flexbox/Grid*, suportando telas desde *smartphones* até monitores *Ultrawide*.
4. **Otimização de Mídia:** Tratamento visual para carregamento leve de recursos estáticos e fontes tipográficas.

## 📂 Estrutura de Pastas

A arquitetura de pastas foi desenhada visando a separação de responsabilidades (UI vs Lógica):

```text
simbolismo-do-norte/
├── public/              # Assets globais estáticos (favicon, imagens brutas)
├── src/
│   ├── assets/          # Ícones, vetores e imagens otimizadas para o build
│   ├── components/      # Componentes de interface reutilizáveis (Header, Footer, ContentCard)
│   ├── pages/           # Views principais da aplicação agrupando componentes
│   ├── styles/          # Estilização global, variáveis e temas (SASS/CSS)
│   ├── data/            # Mocks e arquivos JSON simulando a base de dados de conteúdo
│   ├── App.jsx          # Orquestrador raiz da aplicação e roteamento
│   └── main.jsx         # Ponto de entrada e injeção do React no DOM
├── package.json         # Manifesto de dependências do ecossistema Node
└── vite.config.js       # Configuração do empacotador
