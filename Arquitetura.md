# Arquitetura de serviços da plataforma

A arquitetura de serviços do AEM pode ser entendida em **duas grandes áreas**:

- **Gestão de conteúdo** (onde o conteúdo é criado e organizado);
- **Entrega de experiência** (onde o conteúdo é publicado e consumido).

## 1) Gestão de conteúdo (Authoring)

A criação de conteúdo pode vir de duas fontes principais.

### 1.1 Nível de criação no AEM
É o ambiente de autoria tradicional do AEM, com interface web e APIs.

Suporta dois modelos:

- **Headful**: criação visual com editor de páginas e Editor Universal;
- **Headless**: criação estruturada via Fragmentos de Conteúdo para consumo por APIs.

### 1.2 Nível de criação baseado em documentos
Permite que equipes criem conteúdo em ferramentas já conhecidas e publiquem no ecossistema AEM.

Exemplos:

- Microsoft Word/Excel via SharePoint;
- Google Docs/Sheets via Google Drive.

Esse modelo costuma acelerar produção de conteúdo para times não técnicos.

## 2) Entrega de experiência (Publishing/Delivery)

A publicação também pode acontecer por dois caminhos.

### 2.1 Publicação no AEM
É o modelo clássico de entrega com infraestrutura de publicação do AEM.

Características:

- uso de instâncias de publish e dispatcher;
- renderização no lado do servidor;
- entrega de páginas e APIs (incluindo GraphQL).

É robusto e completo, mas pode ter maior complexidade operacional.

### 2.2 Publicação com Edge Delivery Services
Modelo de entrega focado em simplicidade e performance.

Características:

- renderização otimizada para web moderna;
- consumo de múltiplas fontes de conteúdo (AEM e documentos);
- foco em tempo de carregamento e experiência do usuário.

## 3) Serviços adjacentes

Além dos blocos principais, a arquitetura inclui serviços de apoio.

### Edge Delivery Assets
Camada para entrega eficiente de imagens e mídias gerenciadas no AEM Assets.

### Camadas de visualização (Preview)
Ambientes de pré-visualização permitem validar conteúdo e contexto antes da publicação oficial.

### Repositório de conteúdo
Camada de armazenamento usada na autoria do AEM, compatível com o modelo JCR e executada em infraestrutura em nuvem.

### CI/CD
Pipelines automatizados para build, validação e publicação de código/configurações.

### Serviços de teste
Podem variar por projeto e pipeline, mas normalmente incluem:

- testes funcionais;
- testes de interface (por exemplo: Selenium ou Cypress);
- auditorias de qualidade/performance (por exemplo: Lighthouse).

### Serviço de dados
Responsável por expor métricas e relatórios para acompanhamento do negócio e operação, geralmente via APIs e painéis.

### Telemetria operacional
Responsável por coletar indicadores técnicos da plataforma (disponibilidade, erros, latência, etc.).

### Identity Management Service (IMS)
Serviço de identidade da Adobe Experience Cloud para autenticação e gestão de usuários.

## Arquitetura do sistema
