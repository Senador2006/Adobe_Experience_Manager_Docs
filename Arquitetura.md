# Arquitetura de Serviço da ferramenta
- A estrutura de serviços do AEM pode ser separado em duas segmentações: Gestão de conteudo e Entrega de experiencia
´´´
Image
´´´
- Separamos a criação de conteudo em 2 partes, representadas como fontes de conteudo:
    - O nível de criação do AEM:
        Fornece uma interface baseada na Web (com APIs associadas) para o gerenciamento de conteúdo da Web. Isso funciona para ambas as abordagens:
        - Headful - pelo editor de páginas e pelo editor universal
        - Headless - por meio do editor de fragmento de conteúdo
    
    - O nível de criação baseado em documentos:
        Permite criar conteúdo usando aplicativos padrão, como:
        - Microsoft Word e Excel - via SharePoint
        - Google Docs e Sheets - via Google Drive

- Para a entrega de experiencia tambem separamos em 2 partes:
    - O nivel de publicação do AEM
        - Esse é o fornecimento basico, utilizando de farms de editores e dispatchers permitindo renderizar e atualizar as paginas e aplicações Web alem do conteudo de APIs (GraphQL, banco de dados em grafos)
        - Funciona na base logica do aplicativo do servidor e acaba sendo mais complexo e lento que a outra opção

    - O nivel de publicação do Edge Delivery
        - A renderização das aplicações, como paginas web e conteudos API é muito mais simples e eficiente, utilizando varias fontes como o proprio nivel de criação do AEM e o nivel de criação baseado em documentos como renderizador.
        - É baseado na logica de aplicativos do lado do cliente e projetado para desenpenho maximo.

- Alem desses temos serviços adjacentes como:
    - O nivel do Edge Delivery Assets
        - Para entrega de items e midias do proprio AEM Assets
    - A camada de Visualização do AEM e a camada de Visualização do Edge Delivery Services:
        - Permitem que os autores possam visualizar o conteudo criado e seu contexto antes que seja levado a operações de publicação
    - Serviço de repositorio de conteudo
        - Usado no nivel de criação AEM
        - Baseados em armazenamento na nuvem e compativeis com JCR
    - CI/CD
    - Serviço de teste
        Geralmente funciona baseado no pipeline do proprio projeto, entao eles podem variar para mais ou menos testes.
        - Testes funcionais
        - Testes de interface (baseados em scripts de Selenium ou Cypress)
        - Testes de auditoria (Lighthouse scores)
    - Serviço de dados
        - Responsavel por expor dados do cliente como metricas e relatorios
        - Utilizam meios como APIs e sao expostos diretamente na interface
    - Serviço de Telemetria Operacional
        - Responsavel pela coleta das metricas e dados do cliente
    - Identity Management Service(IMS)
        - Responsavel pelo gerenciamento e autentificação dos usuarios determinados pelo Adobe Experience Cloud

# Arquitetura do sistema
