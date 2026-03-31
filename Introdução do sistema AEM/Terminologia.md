# Terminologia do AEM (versão simples)

Este arquivo resume os termos mais usados no **AEM as a Cloud Service** em linguagem direta.

## 1) Produtos

| Produto | Explicação simples |
|---|---|
| AEM as a Cloud Service | Versão do AEM que já nasce para rodar na nuvem. |
| AEM Assets as a Cloud Service | Parte do AEM focada em ativos digitais (imagens, vídeos, documentos), com recursos para organizar, processar e distribuir arquivos. |
| AEM Sites as a Cloud Service | Parte do AEM focada em criação e publicação de sites. |

## 2) Ambientes e pipeline

| Item | Explicação simples |
|---|---|
| Nível de criação (Author) | Ambiente onde o time cria e edita conteúdo. |
| Nível de pré-visualização (Preview) | Ambiente para validar como o conteúdo ficará antes de publicar. |
| Nível de publicação (Publish) | Ambiente público, acessado pelos usuários finais. |
| Adobe Pipeline | Fluxo automatizado que ajuda a levar mudanças entre os ambientes com controle e segurança. |

## 3) Termos importantes

| Termo | Explicação simples |
|---|---|
| Imagem do AEM | Pacote implantável com o código do produto AEM + código do cliente. |
| Microsserviços de ativos | Serviços em nuvem para processar ativos (ex.: gerar variações de imagem, extrair texto, processar PDF). |
| Repositório Git do Cloud Manager | Local onde o código e configurações do projeto ficam versionados. |
| Provedor de nuvem | Infraestrutura onde o AEM roda (ex.: Azure ou AWS), gerenciada pela Adobe. |
| CDN (Rede de Entrega de Conteúdo) | Rede que entrega conteúdo mais rápido para o usuário final, usando cache em pontos próximos do usuário. |
| Repositório de conteúdo | Banco/repositório onde o conteúdo do AEM é armazenado. |
| Isolamento corporativo | Cada ambiente/instância de cliente fica isolado de outros clientes. |
| Golden Master | Referência do ambiente de publicação estável. |
| Mecanismo de orquestração | Sistema que ajusta automaticamente os serviços (escala) conforme a necessidade. |

## 4) Resumo rápido

Pense no AEM Cloud assim:
- **Author**: cria conteúdo  
- **Preview**: revisa conteúdo  
- **Publish**: entrega conteúdo  
- **Pipeline + Orquestração**: automatizam e escalam todo o processo

