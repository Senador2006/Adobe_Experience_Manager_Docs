# Adobe Experience Manager (AEM)

## Fundamentos e conceitos basicos

### O que é?
- O AEM é um CMS enterprise da Adobe, ela é responsavel pela criação, gerenciamento e entrega de experiencias digitais (apps, sites, landing pages, assets) em grande escala. Alem do CMS ela utiliza do DAM para as mesmas responsabilidades dos assets.

### O que é o CMS?
- O CMS ou Content Management System é uma aplicação de software que permite que o criador possa criar, manejar e modificar uma aplicação Web sem conhecimento especializado, tais como WordPress, Drupal, Wix e ate mesmo o proprio AEM.

### O que é o DAM?
- DAM ou Digital Asset Management é o sistema que organiza, versiona, busca e distribui arquivos digitais (PDFs, Logos, videos e etc). O DAM utiliza de tags automaticas, Metadados e nomes para ajudar na localização e segurança dos dados presentes.

## Arquitetura Logica da ferramenta

### Como que é estruturado a ferramenta da AEM?
- O AEM é composto por soluções de alto nivel, utilizando sistemas de AEM Sites (CMS), AEM Assets (DAM), AEM Forms e AEM Edge Delivery. O sistema é baseado em Java e utiliza frameworks como: Apache Sling (Requisisões HTTP), OSGi (Modularização) e JCR ou Java Content Repository (Banco de conteudo)

### Ambientes dentro do AEM
#### AEM Sites
- O AEM Sites é a ferramenta base que utiliza o CMS, a plataforma apresenta ser mais Low-code à No-code utilizando para criação de paginas: drag & drop, componentes reutilizaveis (tipo React, mas server-side), templates e controle de idioma do conteudo.
#### AEM Assets
- O sistema do AEM Assets é mais uma ferramenta para trabalhar junto ao AEM Sites do que um sistema que trabalha sozinho propriamente. O sistema utiliza de tags automaticas com IA, vercionamento de dados e distribuição para multiplos canais tudo para ajudar na localização e separação de assets.
#### AEM Forms
- Esse sistema é fundamental para a coleta de dados, automação de documentos e workflows. O sistema pode: criar formularios inteligentes e dinamicos, gerar PDFs automaticos, automatizar processos (cadastro, onboarding, contratos) e pode ser integrado com sistemas backend (APIs, Banco de dados)
#### AEM Edge Delivery
- Esse sistema é fundamental para a entrega de dados entre sistema e usuario, processando dados como forms e docs para HTMls otimizados e js leves e CSS enxutos para que tenha uma entrega mais eficiente e simplificada, aumentando sua performace e simplificando a complexidade do sistema básico.


